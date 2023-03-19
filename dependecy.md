# List of dependencies for different packages




## BASE packages
packages mentioned below belong to the base sub-directory.

### logger (PEcAn.logger)

NO NON-CRAN DEPENDENCIES!

### db (PEcAn.DB)

- 1) logger 2) remote  3) utils

### qaqc (PEcAn.qaqc)

- 1) utils    2) BIOCRO  3) ED2  4) SIPNET

### remote (PEcAn.remote)

- 1) logger 2) workflow 3) DB

### settings (PEcAn.settings)

- 1) all  2) DB  3) logger  4) remote  5) utils

### utils (PEcAn.utils)

- 1) DB  2) logger  3) remote  4) workflow  5) data.atmosphere  6) benchmark

### visualization (PEcAn.visualization)

- 1) DB  2) logger  3) utils

### workflow (PEcAn.workflow)

- 1) DB  2) logger  3) remote  4) settings  5) utils    6) data.atmosphere  7) data.land  8) uncertainty


## MODULES packages
packages mentioned below belong to the modules sub-directory.

### allometry (PEcAn.allometry)

- 1) DB  2) utils

### assim.batch (PEcAn.assim.batch)

- 1) logger  2) DB  3) remote  4) settings  5) utils    6) meta.analysis  7) uncertainty  8) emulator  9) benchmark  10) workflow

### assim.sequential (PEcAn.assim.sequential)

- 1) all  2) DB  3) logger  4) remote  5) settings  6) utils  7) visualization  8) workflow 9) meta.analysis  10) uncertainty  11) LINKAGES  12) SIPNET  13) ED2    14) data.remote

### benchmark (PEcAn.benchmark)

- 1) all  2) DB  3) logger  4) remote  5) settings  6) utils    7) data.land

### data.atmosphere (PEcAn.data.atmosphere)

- 1) all  2) DB  3) logger  4) remote  5) settings  6) utils    7) ED2  8) SIPNET  9) DALEC

### data.hydrology (PEcAn.hydrology)

- 1) logger  2) utils

### data.land (PEcAn.data.land)

- 1) logger  2) DB  3) remote  4) settings  5) utils  6) visualization  7) data.atmosphere 8) benchmark

### data.mining (PEcAn.data.mining)

- 1) logger  2) utils

### data.remote (PEcAn.data.remote)

- 1) DB  2) utils  3) logger  4) remote

### emulator (PEcAn.emulator)

- 1) logger

### meta.analysis(PEcAn.MA)

- 1) utils  2) DB  3) logger 4) settings

### photosynthesis (PEcAn.photosynthesis)

**NO NON-CRAN DEPENDENCIES!**

### priors (PEcAn.priors)

- 1) utils  2) logger          3) meta.analysis

### rtm (PEcAnRTM)

- 1) logger  2) utils         3) assim.batch           4)ED2

### uncertainty (PEcAn.uncertainty)

- 1) utils  2) DB  3) logger  4) all  5) assim.sequential  6) data.atmosphere  7) emulator  8) priors


## MODELS PACKAGES
packages mentioned below belong to the models sub-directory.

### basgra (PEcAn.BASGRA)

- 1) logger  2) utils          3) data.atmosphere  4) data.land               5)ModelName (template)

### biocro (PEcAn.BIOCRO)

- 1) logger  2) remote  3) utils  4) settings  5) DB  6) all          7) data.atmosphere  8) data.land  

### cable (PEcAn.CABLE)

- 1) logger  2) utils            3) ModelName (template)

### clm45 (PEcAn.CLM45)

- 1) logger  2) utils

### dalec (PEcAn.DALEC)

- 1) logger  2) remote  3) utils          4) data.atmosphere  5) data.land

### dvmdostem (PEcAn.dvmdostem)

- 1) utils  2) logger

### ed (PEcAn.ED2)

- 1) utils  2) logger 3) remote  4) settings  5) data.atmosphere  6) data.land  7) ModelName (template)

### fates (PEcAn.FATES)

- 1) utils  2) remote  3) logger

### gday (PEcAn.GDAY)

- 1) utils  2) logger  3) remote

### jules (PEcAn.JULES)

- 1) utils  2) logger  3) remote

### linkages (PEcAn.LINKAGES)

- 1) utils  2) logger  3) remote  4) all  5) visualization           6) data.atmosphere  7) assim.sequential  8) allometry

### lpjguess (PEcAn.LPJGUESS)

- 1) utils  2) remote  3) logger

### maat (PEcAn.MAAT)

- 1) logger  2) settings  3) remote  4) utils  5) DB  6) all  7)workflow            8) data.atmosphere

### maespa (PEcAn.MAESPA)

- 1) logger  2) remote  3) utils             4) data.atmosphere

### preles (PEcAn.PRELES)

- 1) utils  2) logger           3) data.atmosphere

### sipnet (PEcAn.SIPNET)

- 1) logger  2) remote  3) utils  4) all  5) visualization           6) data.atmosphere  7) data.land  8) assim.sequential  9) allometry                10) ModelName (template)

### stics (PEcAn.STICS)

- 1) settings  2) DB  3) logger  4) utils  5) remote

### template (PEcAn.ModelName)

- 1) DB  2) logger  3) utils
