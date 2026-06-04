# Gravitational Waves–Lensing Mock Catalog of Space-borne Detectors (GW-LMC-Space)

## Overview

This repository provides mock catalogs of gravitational-wave (GW) sources for space-based detectors, including LISA and DECIGO. This catalog employs a multi-scale Halo Model approach, unifying lensing predictions across galaxy, group, and cluster scales while explicitly incorporating dark matter subhalos.

---

## Key Features

* Multiple source types of stellar-mass compact binary systems, as well as formation models of supermassive black holes, are included.
* Lensing effects are modeled across a wide range of scales, from galaxies to clusters.
* The original SNR distributions are provided.

---

## Repository Structure

```text
GW-LMC-Space/
├── LISA/
│   ├── Intrinsic_source_catalogs/
│   ├── Original_lensing_parameters/
│   ├── Lensed_gw_catalogs/
│   ├── LISA.md
├── DECIGO/
│   ├── Intrinsic_source_catalogs/
│   ├── Original_lensing_parameters/
│   ├── Lensed_gw_catalogs/
│   ├── DECIGO.md
└── README.md
```

---

## Data Description

The catalogs are stored in CSV format.

## File Description

* Intrinsic_source_catalogs: Stores the intrinsic source parameters, including masses, redshifts, etc.
* Original_lensing_parameters: Stores the full set of lensing parameters, including halo mass, lens redshift, etc.
* Lensed_gw_catalogs: Final catalogs of lensed GW events, including Morse index, event index, etc.

More details can be found in the `.md` files within each directory.

---

## Version

Current version: <<< v2.0 >>>

### Changelog

* v1.0: Full mock catalogs of lensed events.
* v2.0: Modified the catalogs of DECIGO decetor, consider the confusion nosie into the calculation of SNR, make the calculation more reliable.

---

## Citation

If you use this catalog, please cite:
ongoing~

---

## License

MIT License

---

## Contact

[astrowhu@gmail.com](mailto:astrowhu@gmail.com)

