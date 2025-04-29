# Simulations and Data Availability


This page gives the basic overview of the model simulations and available data. Details on the models are stored [here](https://github.com/digital-earths-global-hackathon/hk25/tree/main/content/models).

<ins> **Model** </ins>

| Domain and resolution                                                 | Host team          | Link to data                     | Data contact           |
|-----------------------------------------------------------------------|--------------------|----------------------------------|------------------------|
|  <ins> **[SCREAM](https://github.com/digital-earths-global-hackathon/hk25/blob/main/content/models/scream.md)** </ins>      |  |  |  |
| Global, 3.25 km / 128 levels     | [US-West](https://sites.google.com/lbl.gov/uswest-hackathon/home)                        | [NERSC Data via Globus](https://github.com/digital-earths-global-hackathon/tools/tree/main/dataset_transfer/NERSC_globus.md)         | [Andrew Gettelman](mailto:andrew.gettelman@pnnl.gov)            |
|  <ins> **[ICON](https://github.com/digital-earths-global-hackathon/hk25/blob/main/content/models/icon.md)** </ins>          |  |  |  |
| Global, 2.5 km                   | [Hamburg](https://digital-earths-global-hackathon.github.io/hamburg-node/)               | *tba*                       | [Florian Ziemen](mailto:ziemen@dkrz.de)                         |
|  <ins> **[NICAM](https://github.com/digital-earths-global-hackathon/hk25/blob/main/content/models/nicam.md)** </ins>        |  |  |  |
| Global, 3.5 km                   | [Tokyo](https://dpo.aori.u-tokyo.ac.jp/dmmg/ICCP-GSRA/Global-Hackathon_Tokyo.htm)        | *tba*                       | [Daisuke Takasuka](mailto:takasuka@tohoku.ac.jp)      |
|  <ins> **[Unified Model](https://github.com/digital-earths-global-hackathon/hk25/blob/main/content/models/um.md)** </ins>   |  |  |  |
| Global & regional, 5 km & 10 km  | [Oxford](https://digital-earths-global-hackathon-uk.github.io/)                          | [UK Object Store](https://github.com/digital-earths-global-hackathon/tools/blob/main/dataset_transfer/UK_s3_rclone.md) | [P.L. Vidale](mailto:p.l.vidale@reading.ac.uk), [Mark Muetzelfeldt](mailto:mark.muetzelfeldt@reading.ac.uk) |
|  <ins> **[CAS-ESM](https://github.com/digital-earths-global-hackathon/hk25/blob/main/content/models/cas.md)** </ins>        |  |  |  |
| Global 10 km (partly 5 km)       | [Beijing](https://earthlab.iap.ac.cn/en/hackathon2025/)                                  | *tba*                       | *tbd*            |
| <ins> **[IFS-FESOM](https://github.com/digital-earths-global-hackathon/hk25/blob/main/content/models/ifs.md)** </ins>       |  |  |  |
| Global atm 2.8 km / ocean 5 km   | [Hamburg](https://digital-earths-global-hackathon.github.io/hamburg-node/)               | *tba*                       | [Thomas Rackow](mailto:thomas.rackow@ecmwf.int)       |
| <ins> **[NCAR-MPAS](https://github.com/digital-earths-global-hackathon/hk25/blob/main/content/models/mpas.md)** </ins>      |  |  |  |
| Global                           | [US-Central](https://www.cisl.ucar.edu/events/digital-earths-global-hackathon)           | *tba*                       | [Brain Medeiros](mailto:brianpm@ucar.edu )            |
| <ins>   **[NCAR-WRF](https://github.com/digital-earths-global-hackathon/hk25/blob/main/content/models/wrf.md)**  </ins>       |  |  |  |
| Regional: N./S. America, 4 km    | [US-Central](https://www.cisl.ucar.edu/events/digital-earths-global-hackathon)           | *tba*                       | [Julia Kukulies](mailto:kukulies@ucar.edu)            |
| <ins> **[GFDL](https://github.com/digital-earths-global-hackathon/hk25/blob/main/content/models/gfdl.md)**  </ins>          |  |  |  |
| Global                           | [US-East](https://cimes.princeton.edu/princeton-university-geophysical-fluid-dynamics-laboratory-global-km-scale-hackathon-0) | *tba* | [Tim Merlis](mailto:tmerlis@princeton.edu)      |



<!---
| Model | Team | Domain and Resolution | Model Contact | Host Team/Node | Data Status | Link to Data | Data Contact |
|-------|------|------------------------|----------------|----------------|--------------|---------------|----------------|
| [SCREAM](https://github.com/E3SM-Project/E3SM) | DOE E3SM Project | 3.25 km global 128 levels  | [Peter Caldwell](mailto:caldwell19@llnl.gov), [Chris Terai](mailto:terai1@llnl.gov) | US-West (NERSC) | Processed to HEALPix: Staging | Delivery via Globus | [Andrew Gettelman](mailto:andrew.gettelman@pnnl.gov) |
| [ICON](https://icon-model.org/) | MPI-M | Global, 2.5 km | [Daniel Klocke](mailto:daniel.klocke@mpimet.mpg.de) | EU |  |  | [Florian Zemian](mailto:ziemen@dkrz.de) |
| NICAM | NICAM team | Global 3.5 km | [Masaki Satoh](mailto:satoh@aori.u-tokyo.ac.jp), [Daisuke Takasuka](mailto:takasuka@tohoku.ac.jp) | Japan |  |  |  |
| Unified Model | [UK HRCM](https://hrcm.ceda.ac.uk) (MO+NCAS) | Global & regional 5km & 10km | [P.L. Vidale](mailto:p.l.vidale@reading.ac.uk), Huw Lewis | Oxford - Met Office  | Partially Uploaded  | [UK Object Store Instructions](https://github.com/digital-earths-global-hackathon/tools/blob/main/dataset_transfer/UK_s3_rclone.md) | [P.L. Vidale](mailto:p.l.vidale@reading.ac.uk), [Mark Muetzelfeldt](mailto:mark.muetzelfeldt@reading.ac.uk) |
| CAS-ESM2.0  | CAS-ESM | Global 10km and/or 5km | [He Zhang](mailto:zhanghe@mail.iap.ac.cn), [Kece Fei](mailto:feikece@mail.iap.ac.cn) | IAP (China) |  |  |  |
| IFS-FESOM | ECMWF/AWI | Global: atmosphere ~2.8km, ocean ~5km | [Thomas Rackow](mailto:thomas.rackow@ecmwf.int) | EU |  |  |  |
| MPAS | NCAR-MPAS | Global | [Bill Skamarock](mailto:skamarock@ucar.edu) | US-Central (NCAR) | Processing to HEALPix |  | [Brian Medeiros](mailto:brianpm@ucar.edu) |
| X-SHIELD | GFDL | Global | [Tim Merlis](mailto:tmerlis@princeton.edu) | US-East (Princeton) | Processing to HEALPix |  | [Tim Merlis](mailto:tmerlis@princeton.edu) |
| WRF | NCAR - WF | 4km Regional: N. America and S. America | [Julia Kukulies](mailto:kukulies@ucar.edu) | US-Central (NCAR) | Processing to HEALPix |  | [Julia Kukulies](mailto:kukulies@ucar.edu) |
!-->

