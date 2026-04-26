# intrinsic_source_catalogs

This dataset contains catalogs of **intrinsic (unlensed) gravitational-wave (GW) source parameters** for LISA-band binaries. Each row typically represents one compact-binary source and stores physical properties used for population studies, rate modeling, and detectability forecasts.

| Parameter | Meaning | Unit |
|---|---|---|
| `m1`  | Primary component mass of the binary in the source frame. | `M_sun` |
| `m2`  | Secondary component mass of the binary in the source frame. | `M_sun` |
| `a1` | Dimensionless spin magnitude of the primary object. | dimensionless |
| `a2` | Dimensionless spin magnitude of the secondary object. | dimensionless |
| `z_merger` (`redshift`) | Source redshift at merger/emission epoch. | dimensionless |
| `Dl_s` (`luminosity_distance`) | Luminosity distance to the GW source. | Mpc |
| `duration_time` | Effective signal duration in the detector band / observation window. | day |
| `Mean_SNR`  | Average signal-to-noise ratio . | dimensionless |
| `d2N_dzdt` | Differential merger/event-rate density with respect to redshift and time. | model-dependent (typically events per redshift per time) |

# Lensed_gw_catalogs

This dataset provides catalogs of **strongly lensed gravitational-wave (GW) events for LISA-band sources**. Each catalog typically includes the intrinsic binary parameters, together with lensing observables for multiple images, such as magnification factors and time delays. These quantities are designed to facilitate studies of lensing selection effects and the identification of multi-image GW signals.

The catalog files follow the naming convention **{model\_name\}\_\{i\}.csv**, where model\_name denotes the adopted formation model, including **HSnodnoSN**, **HSnodSN**, **HSnodhighaccr**, **PopIIId**, **Q3d**, and **Q3nod**, and {i} represents the index of the random realization used to generate the catalog.

| Parameter  | Meaning | Unit |
|---|---|---|
| `mu_list` | List of image magnification factors for all lensed images of an event. | dimensionless |
| `td_list` | List of relative arrival-time delays between lensed images. | s |
| `n_list` (`image_index`) | Morse-type ordering for individual images. | dimensionless|
| `idx` | Event identifier linking lensed entries to the unlensed source catalogs. | index |
| `m1`  | Primary component mass of the source binary. | `M_sun` |
| `m2` | Secondary component mass of the source binary. | `M_sun` |
| `a1` | Primary spin magnitude. | dimensionless |
| `a2` | Secondary spin magnitude. | dimensionless |
| `z_merge` (`redshift`) | Source redshift of the lensed GW event. | dimensionless |
| `Dl_s` (`luminosity_distance`) | Source luminosity distance. | Mpc |
| `duration_time` | In-band duration / observable duration of the signal. | day |
| `Mean_SNR`  | Average unlensed signal-to-noise ratio. | dimensionless |
| `Signal_1` ... `Signal_5` | SNR of each signal in the lensing system after considering the overlap. (when there's no signal, store "0.0" as placeholder)|dimensionless |
| `z_lens_sbh` | Lens redshift for the sub-halo lens component. (when the lensing process are not effected by the subhalo, store "-1" as placeholder) | dimensionless |
| `z_lens_hh` | Lens redshift for the host-halo lens component. | dimensionless |




