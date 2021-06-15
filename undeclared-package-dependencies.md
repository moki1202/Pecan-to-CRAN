## base 
packages mentioned below are absent from description of its respective header file


### db

- meta.analysis (MA)-
\db\man\rename_jags_columns.Rd
\db\R\rename_jags_columns.R
\db\tests\Rcheck_reference.log



### qaqc

- db
\qaqc\R\cull_database_entries.R
\qaqc\R\get_table_column_names.R
\qaqc\tests\Rcheck_reference.log

-utils
\qaqc\vignettes\compare_ED2.Rmd
\qaqc\vignettes\function_relationships.Rmd

 BIOCRO-
 \qaqc\vignettes\function_relationships.Rmd

ED2-
\qaqc\vignettes\function_relationships.Rmd

SIPNET-
\qaqc\vignettes\function_relationships.Rmd



### remote

- db
\remote\R\remote.copy.update.R
\remote\tests\Rcheck_reference.log



### settings

- all
base\settings\man\read.settings.Rd
base\settings\R\read.settings.R



### utils

 workflow-
base\utils\man\do_conversions.Rd
base\utils\man\run.write.configs.Rd
base\utils\R\do_conversions.R
base\utils\R\run.write.configs.R

benchmark-
base\utils\man\read.output.Rd
base\utils\R\read.output.R
base\utils\tests\Rcheck_reference.log

 -priors-
 base\utils\man\create.base.plot.Rd
base\utils\R\plots.R
base\utils\tests\Rcheck_reference.log

 -uncertainty-
base\utils\man\get.ensemble.samples.Rd
base\utils\man\read.ensemble.output.Rd
base\utils\man\write.ensemble.configs.Rd
base\utils\R\ensemble.R
base\utils\R\get.results.R
base\utils\tests\Rcheck_reference.log



## modules


### allometry

- utils-
modules\allometry\tests\Rcheck_reference.log
modules\allometry\tests\testthat.R


###assim.sequential

- all-
modules\assim.sequential\R\Remote_helpers.R
modules\assim.sequential\man\SDA_remote_launcher.Rd
modules\assim.sequential\inst\workflow.variance.partitioning.R

 visualization-
 **only in /inst files**  

 workflow-
 **only in /inst folder**

  linkages-
  **only in /inst folder**

   sipnet-
   **only in /inst folder**

    ED2-
    **only in /inst folder**

    uncertainty-
    **only in /inst folder**

    MA-
    **only in /inst folder**


### benchmark

- all
modules\benchmark\inst\scripts\benchmark.workflow.R


### data.atmopshere

- all-
**only in /inst folder**

 settings-
 modules\data.atmosphere\inst\ERA5\ERA5_db_register.R

ED2-
modules\data.atmosphere\inst\scripts\met.workflow.R

 SIPNET-
 modules\data.atmosphere\inst\scripts\met.workflow.R

 DALEC-
 modules\data.atmosphere\man\merge_met_variable.Rd
 modules\data.atmosphere\R\merge.met.variable.R


### uncertainty

- all-
modules\uncertainty\inst\abbreviated_workflow_SIPNET.R

 data.atmosphere-
 modules\uncertainty\R\prep.data.assim.R
 modules\uncertainty\tests\Rcheck_reference.log

  assim.sequential-
  modules\uncertainty\man\prep.data.assim.Rd
  modules\uncertainty\R\prep.data.assim.R
  modules\uncertainty\tests\Rcheck_reference.log




## MODELS  


### basgra


- ModelName-
models\basgra\R\read_restart.BASGRA.R
models\basgra\R\write_restart.BASGRA.R

 data.land-
 models\basgra\R\write.config.BASGRA.R

### bioro

- all-
/inst and /vignettes folder


### cable

- ModelName-
models\cable\tests\testthat.R

### dalec

- data.atmosphere-
models\dalec\R\met2model.DALEC.R
models\dalec\tests\Rcheck_reference.log

 data.land-
 models\dalec\R\write.configs.dalec.R
 models\dalec\tests\Rcheck_reference.log

### dvmdostem

- **logger**
models\dvmdostem\R\model2netcdf.dvmdostem.R ( many instances )

### ed(ED2)

- ModelName-
models\ed\R\read_restart.ED2.R
models\ed\R\write_restart.ED2.R

### linkages

- all-
models\linkages\inst\LINKAGES.lyford.SDA.R
models\linkages\inst\setup_da.R

 assim.sequential-
 models\linkages\inst\LINKAGES.lyford.SDA.R
 models\linkages\inst\setup_da.R

  visualization-
  models\linkages\inst\LINKAGES.lyford.SDA.R
  models\linkages\inst\setup_da.R

   allometry-
   models\linkages\inst\LINKAGES.lyford.SDA.R


### maat

- all-
models\maat\vignettes\running_maat_in_pecan.Rmd

 db-
 models\maat\vignettes\create_amerifluxLBL_drivers_for_maat.Rmd

  workflow -
  models\maat\vignettes\running_maat_in_pecan.Rmd


### sipnet

- all-
models\sipnet\inst\SIPNET.lyford.SDA.R

 assim.sequential-
 models\sipnet\inst\SIPNET.lyford.SDA.R

  visualization-
  models\sipnet\inst\SIPNET.lyford.SDA.R

   allometry-
models\sipnet\inst\SIPNET.lyford.SDA.R

 ModelName-
 models\sipnet\R\read_restart.SIPNET.R

  data.land-
  models\sipnet\R\write.configs.SIPNET.R
  models\sipnet\tests\Rcheck_reference.log
