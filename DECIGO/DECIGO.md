# intrinsic_source_catalogs

This dataset contains catalogs of **intrinsic (unlensed) gravitational-wave (GW) source parameters** for DECIGO-band compact binaries (e.g., BNS and NSBH). Each row typically represents one compact-binary source and stores physical properties used for population studies, parameter inference, and detectability forecasts.

| Parameter | Meaning | Unit |
|---|---|---|
| `m1_source` | Primary component mass of the binary in the source frame. | `M_sun` |
| `m2_source` | Secondary component mass of the binary in the source frame. | `M_sun` |
| `luminosity_distance` | Luminosity distance to the GW source. | Mpc |
| `phase` | GW phase at the chosen reference frequency/time. | rad |
| `a1` | Dimensionless spin magnitude of the primary object. | dimensionless |
| `a2` | Dimensionless spin magnitude of the secondary object. | dimensionless |
| `tilt1` | Tilt angle between the primary spin vector and orbital angular momentum. | rad |
| `tilt2` | Tilt angle between the secondary spin vector and orbital angular momentum. | rad |
| `phi12` | Relative azimuthal angle between the two spin vectors. | rad |
| `phijl` | Azimuth between total spin/angular momentum direction and orbital angular momentum. | rad |
| `z_merger` | Source redshift at merger/emission epoch. | dimensionless |
| `theta_s` | Source sky polar angle (declination-equivalent coordinate). | rad |
| `phi_s` | Source sky azimuth (right-ascension-equivalent coordinate). | rad |
| `theta_l` | Binary orbital angular-momentum inclination relative to line of sight. | rad |
| `phi_l` | Azimuthal orientation angle of orbital angular momentum. | rad |
| `start_time` | Observation start or reference time for waveform generation. | day |
| `snr` | signal-to-noise ratio. | dimensionless |
| `duration_time` | Effective signal duration in the detector band / observation window. | day |

# Lensed_gw_catalogs

This dataset provides catalogs of **strongly lensed gravitational-wave (GW) events for DECIGO-band sources**. Each catalog typically includes the intrinsic binary parameters, together with lensing observables for multiple images, such as magnification factors and time delays. These quantities are designed to facilitate studies of lensing selection effects and the identification of multi-image GW signals.

The catalog files follow the naming convention {source_type}_{i}.csv, where source_type denotes the source class, including **BBH**, **BNS**, and **NSBH**, and i represents the index of the random realization used to generate the catalog.

| Parameter | Meaning | Unit |
|---|---|---|
| `mu_list` | List of image magnification factors for all lensed images of an event. | dimensionless |
| `td_list` | List of relative arrival-time delays between lensed images. | s |
| `n_list` | Morse-type ordering for individual images. | dimensionless |
| `idx` | Event identifier linking lensed entries to the intrinsic source catalogs. | index |
| `m1` | Primary component mass of the source binary. | `M_sun` |
| `m2` | Secondary component mass of the source binary. | `M_sun` |
| `a1` | Primary spin magnitude. | dimensionless |
| `a2` | Secondary spin magnitude. | dimensionless |
| `z_merge` | Source redshift of the lensed GW event. | dimensionless |
| `Dl_s` | Source luminosity distance. | Mpc |
| `duration_time` | In-band duration / observable duration of the signal. | day |
| `SNR` | Unlensed signal-to-noise ratio. | dimensionless |
| `Signal_1` ... `Signal_5` | SNR of each signal in the lensing system after considering the overlap. (when there's no signal, store "0.0" as placeholder) | dimensionless |
| `z_lens_sbh` | Lens redshift for the sub-halo lens component. (when the lensing process are not effected by the subhalo, store "-1" as placeholder) | dimensionless |
| `z_lens_hh` | Lens redshift for the host-halo lens component. | dimensionless |

