# Crop field Extension Specification

- **Title:** Crop field
- **Identifier:** <https://fiboa.github.io/crop-extension/v0.1.0/schema.yaml>
- **Property Name Prefix:** crop
- **Extension Maturity Classification:** Proposal
- **Owner**: @ivorbosloper

This document explains the Crop field Extension to the
[Field Boundaries for Agriculture (fiboa) Specification](https://github.com/fiboa/specification).

Many published crop field datasets use a crop code list to identify the crop on each crop field. This extension
harmonizes the columns to describe a coding list, a crop code and a crop name.

A `code_list` should be an url with a csv with at least fields `original_code`, `original_name`, `translated_name`.
Examples of usable code_lists are the [EuroCrops code lists](https://github.com/maja601/EuroCrops/blob/main/csvs/country_mappings/).
A valid value for `crop:code_list` would be `https://github.com/maja601/EuroCrops/blob/main/csvs/country_mappings/dk_2019.csv`

- Examples:
  - [GeoJSON](examples/geojson/)
  - [GeoParquet](examples/geoparquet/)
- [Schema](schema/schema.yaml)
- [Changelog](./CHANGELOG.md)

## Properties

The properties in the table below can be used in these parts of fiboa documents:

- [ ] Collection
- [x] Feature Properties

| Property Name  | Type   | Description                                      |
|----------------| ------ |--------------------------------------------------|
| crop:code_list | string | A link to the coding list                        |
| crop:code      | string | **REQUIRED** The crop code                       |
| crop:name      | string | **REQUIRED** Crop name in the original language. |
| crop:name_en   | string | **optional** Crop name in English                |

## Contributing

See the [contributing guideline](CONTRIBUTING.md) for more details.
