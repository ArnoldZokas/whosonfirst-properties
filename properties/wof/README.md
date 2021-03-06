# wof

`wof` stands for Who's On First

## abbreviation

A two-letter country code from ISO 3166.

**IMPORTANT: THIS PROPERTY HAS BEEN DEPRECATED.** It will not be removed in the short-term but nor will it be updated to added to any new or existing records. Please use `shortcode` or [label:{lang}_x_preferred_shortcode](labels.md#lang_x_preferred_shortcode) instead.

## belongsto

The (unique) set of all ancestors, as an array (list) of WOF IDs.

## brand_id

A unique identifier that represents a Mapzen brand, as found in [https://github.com/whosonfirst-data/whosonfirst-brands](https://github.com/whosonfirst-data/whosonfirst-brands).,

## breaches

Records of the same placetype that intersect the current record, as an array (list) of WOF IDs.

## capital

A list property used to link country or dependency records to their administrative, judicial, and/or legislative capitals. The values are equal to the `wof:id` of each capital. Capital records have a `wof:placetype` of `locality`.

## capital_of

A string property used to link administrative, judicial, and/or legislative capitals to their parent country or dependency. The values are equal to the `wof:id` of the parent country or dependency.

## concordances

A hash containing identifiers from other data sources. See also: [other people's concordances](https://github.com/whosonfirst/tools-other-peoples-concordances)

## concordances_alt

A dictionary of lists, used if a record has more than one identifier for a single data source. Contains identifiers not present in the `wof:concordances` property.

## controlled

A list of Who's On First properties that should be assumed to have been edited by an actual human and should not be updated by automated processes. For example:

```
    "wof:controlled":[
        "wof:hierachy",
        "wof:parent_id"
    ]
```

## coterminous

Links two or more records with overlapping or identical geometries that serve separate functions, but are essentially the same "place" - see [Cuidad de México](https://whosonfirst.mapzen.com/spelunker/id/85686515/#9/19.3228/-99.1530). Think "city-state".

## country

A two-letter country code from ISO 3166.

## country_alpha3

The three-letter country code from ISO 3166-1 for a given country or dependency record.

## created

An auto-generated, non-editable Unix epoch timestamp integer.

## fullname

A property used for timezone records. The value is a more robust version of the wof:name and includes the country or continent name that the timezone geometry falls within.

## geomhash

An auto-generated, non-editable MD5 string of the geometry JSON.

## hierarchy

A list of hashes, where each object is the list of ancestors.

## id

The record's unique numeric integer identifier that are typically derived from [Brooklyn Integers](https://www.brooklynintegers.com).

## label

A string value used to populated labels for map displays.

## lang

An [ISO-639-3](http://www.i18nguy.com/unicode/language-identifiers.html) language identifiers. These represent the common, or preferred, languages spoken in the location of the corresponding WOF record.

**IMPORTANT: THIS PROPERTY HAS BEEN DEPRECATED.** It will not be removed in the short-term but nor will it be updated to added to any new or existing records.

## lang_x_official

One or more [ISO-639-3](http://www.i18nguy.com/unicode/language-identifiers.html) language identifiers. These represent the officially recognized languages of the location of the corresponding WOF record.

## lang_x_spoken

One or more [ISO-639-3](http://www.i18nguy.com/unicode/language-identifiers.html) language identifiers. These represent the languages, inclusive of official languages, spoken in the location of the corresponding WOF record.

## lastmodified

A Unix epoch timestamp integer.

## megacity

This is used to signify the world's most populated cities. A record represents a megacity if a value of 1 is given.

## name

An English UTF-7 transliterated representation of the name. See also: [whosonfirst-names](https://github.com/whosonfirst/whosonfirst-names)

## parent_id

An integer WOF ID of the direct parent record. If a record has more than one parent, the following values should be used:

- **-1** (unknown parent, record needs review)
- **-2** (shrug, this feature is complicated)
- **-3** (contested, but not disputed.. used for placetypes below the locality level)
- **-4** (multiple "legal" parents.. used for placetypes at the locality level or above)

## population

An integer value to represent the most current, known population of a place. (related: `src:population`)

## population_rank

An aggregated integer, 0 to 18, where the values represent the following ranges:

    18: Over 1b
    17: 100m to 1b
    16: 50m to 100m
    15: 20m to 50m
    14: 10m to 20m
    13: 5m to 10m
    12: 1m to 5m
    11: 500k to 1m
    10: 200k to 500k
    9: 100k to 200k
    8: 50k to 100k
    7: 20k to 50k
    6: 10k to 20k
    5: 5k to 10k
    4: 2k to 5k
    3: 1k to 2k
    2: 200 to 1k
    1: Less than 200
    0: Locale (no population) / places that only are visible at 50k scale or larger (but not neighbourhoods)

## placetype

A string [placetype](https://github.com/whosonfirst/whosonfirst-placetypes).

## placetype_alt

A list of string [placetypes](https://github.com/whosonfirst/whosonfirst-placetypes) denoting alternate representations of a place. For details please consult [whosonfirst-data issue #538](https://github.com/whosonfirst-data/whosonfirst-data/issues/538).

## placetype_local

What locals consider the placetype to be (string value).

## scale

A weighted value to represent the size of a given record. The smaller the value, the larger the record's scale.

## shortcode

A short alphabetic code, preferring 3-characters for `country` (e.g. **USA**), 2-characters for `region` (e.g. **CA**), and either 3-characer or 2-character for `county` (e.g. **HUM** or **HU**) placetypes. Other placetypes like `venue` can also have shortcodes but their length is not standardized, and they may contain alphanumeric values.

This property replaces the earlier `abbreviation` and is localized via [label:{lang}_x_preferred_shortcode](labels.md#lang_x_preferred_shortcode).

## statistical_gore

An optional boolean value that, when true, represents an “area” of unincorporated status without self-governance.

## subdivision

The value represents a concatenated identifier from the UN/LOCODE, a two-character country code and three-character feature code with a deliminator and names.

## superseded_by

An array (a list) of WOF IDs that have superseded the WOF record.

## supersedes

An array (a list) of WOF IDs that the record supersedes.

## tags

An array (a list) of tags.
