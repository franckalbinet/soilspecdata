# Release notes

<!-- do not remove -->

## 0.2.0

### Breaking Changes

- Remove the names deprecated in 0.1.0: `get_ossl`, `get_mir`, `get_visnir`, `get_aligned_data`, `get_properties`, `OSSLData`, `SpectraData` and `properties_cols` ([#10](https://github.com/franckalbinet/soilspecdata/issues/10))


## 0.1.0

### Breaking Changes

- Sample IDs are now the unique OSSL `id.layer_uuid_txt`, and `ossl.df` is indexed by sample ID ([#1](https://github.com/franckalbinet/soilspecdata/issues/1))

### New Features

- Add a `dev` extra with nbdev and twine ([#9](https://github.com/franckalbinet/soilspecdata/issues/9))
- Rename `OSSLData`, `SpectraData` and `properties_cols` to `OSSL`, `Spectra` and `meta_cols`, and replace `get_properties` with `ossl[cols]` ([#8](https://github.com/franckalbinet/soilspecdata/issues/8))
- Select samples with pandas conditions, as in `ossl[mask]` ([#7](https://github.com/franckalbinet/soilspecdata/issues/7))
- New API `load_ossl`, `ossl.mir()`, `ossl.visnir()` and `spectra.xy()` replaces `get_ossl`, `get_mir`, `get_visnir` and `get_aligned_data` ([#6](https://github.com/franckalbinet/soilspecdata/issues/6))
- Choose OSSL data level `L0` or `L1` with `load_ossl(level=...)` ([#5](https://github.com/franckalbinet/soilspecdata/issues/5))

### Bugs Squashed

- VISNIR wavenumbers were truncated instead of rounded ([#4](https://github.com/franckalbinet/soilspecdata/issues/4))
- `get_ossl` read a cached file from a different URL, because the cache file name ignored the URL ([#3](https://github.com/franckalbinet/soilspecdata/issues/3))
- `get_aligned_data` paired spectra and targets of different samples when a local ID repeated across source datasets ([#2](https://github.com/franckalbinet/soilspecdata/issues/2))
