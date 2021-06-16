## base 
packages mentioned below are absent from description of its respective header file


### db

- meta.analysis (MA)-
\db\man\rename_jags_columns.Rd
\db\R\rename_jags_columns.R
\db\tests\Rcheck_reference.log

To resolve: move `rename_jags_columns` to `PEcAn.MA`


### qaqc

*Can ignore* these for now: Whole qaqc package is low priority for CRAN submission

- db
\qaqc\R\cull_database_entries.R
\qaqc\R\get_table_column_names.R
\qaqc\tests\Rcheck_reference.log

To resolve: Add DB to qaqc's Imports

-utils
\qaqc\vignettes\compare_ED2.Rmd
\qaqc\vignettes\function_relationships.Rmd

To resolve: Add utils to qaqc's Suggests, but refactor the vignettes first

- BIOCRO
\qaqc\vignettes\function_relationships.Rmd

To resolve: Either add PEcAn.BIOCRO to qaqc's Suggests, or refactor/delete vignette

ED2-
\qaqc\vignettes\function_relationships.Rmd

To resolve: Either add PEcAn.ED2 to qaqc's Suggests, or refactor/delete vignette

SIPNET-
\qaqc\vignettes\function_relationships.Rmd

To resolve: Either add PEcAn.SIPNET to qaqc's Suggests, or refactor/delete vignette

### remote

- db
\remote\R\remote.copy.update.R
\remote\tests\Rcheck_reference.log

To resolve: Not determined yet. `remote` only uses two functions from `DB` and `DB` only uses two functions from `remote`, but both are deeply embedded and will be challenging to remove. May need to copy some functions between packages.

### settings

- all
base\settings\man\read.settings.Rd
base\settings\R\read.settings.R

To resolve: Edit example to use a file in `settings` -- the file being looked for in `all` doesn't exist anyway!

### utils

 workflow-
base\utils\man\do_conversions.Rd
base\utils\man\run.write.configs.Rd
base\utils\R\do_conversions.R
base\utils\R\run.write.configs.R

To resolve: Delete deprecated versions of `do_conversions` and `run.write.configs` from utils

benchmark-
base\utils\man\read.output.Rd
base\utils\R\read.output.R
base\utils\tests\Rcheck_reference.log

To resolve: Remove link and just refer to `PEcAn.benchmark::align_data` without linking to it 

 -priors-
 base\utils\man\create.base.plot.Rd
base\utils\R\plots.R
base\utils\tests\Rcheck_reference.log

To resolve: delete `create.base.plot` function, replace calls in `PEcAn.priors::plot_prior.density` with a simple call to `ggplot2::ggplot()`. Bonus cleanup: Move all remaining functions in `plots.R` to the `PEcAn.visualization` package

 -uncertainty-
base\utils\man\get.ensemble.samples.Rd
base\utils\man\read.ensemble.output.Rd
base\utils\man\write.ensemble.configs.Rd
base\utils\R\ensemble.R
base\utils\R\get.results.R
base\utils\tests\Rcheck_reference.log

To resolve: Delete deprecated copies of `get.ensemble.samples` and `read.ensemble.output` from `utils`, move `get.results` to `PEcan.uncertainty`

## modules


### allometry

- utils-
modules\allometry\tests\Rcheck_reference.log
modules\allometry\tests\testthat.R

To resolve: Delete `library(PEcAn.utils)` from `tests/testthat.R`

###assim.sequential

- all-
modules\assim.sequential\R\Remote_helpers.R
modules\assim.sequential\man\SDA_remote_launcher.Rd
modules\assim.sequential\inst\workflow.variance.partitioning.R

To resolve: Delete `library(PEcan.all)` from example (but check that example still works without it)

- visualization-
 **only in /inst files**  

- workflow-
 **only in /inst folder**

- linkages-
  **only in /inst folder**

- sipnet-
   **only in /inst folder**

- ED2-
    **only in /inst folder**

- uncertainty-
    **only in /inst folder**

- MA-
    **only in /inst folder**


### benchmark

- all
modules\benchmark\inst\scripts\benchmark.workflow.R

OK to ignore

### data.atmopshere

- all-
**only in /inst folder**

- settings-
 modules\data.atmosphere\inst\ERA5\ERA5_db_register.R

OK to ignore

- ED2-
modules\data.atmosphere\inst\scripts\met.workflow.R

OK to ignore

- SIPNET-
modules\data.atmosphere\inst\scripts\met.workflow.R

OK to ignore

- DALEC-
modules\data.atmosphere\man\merge_met_variable.Rd
modules\data.atmosphere\R\merge.met.variable.R

TO resolve: Either 

    1. rewrite example to use only in-package examples (may not be possible; I think all met2model functions live in individual model packages), or 
    2. Change example to `met2model.SIPNET` and add `PEcan.SIPNET` to data.atmosphere's Suggests

### uncertainty

- all-
modules\uncertainty\inst\abbreviated_workflow_SIPNET.R

OK to ignore

- data.atmosphere-
modules\uncertainty\R\prep.data.assim.R
modules\uncertainty\tests\Rcheck_reference.log

To resolve: Add data.atmosphere to uncertainty's Imports

- assim.sequential-
modules\uncertainty\man\prep.data.assim.Rd
modules\uncertainty\R\prep.data.assim.R
modules\uncertainty\tests\Rcheck_reference.log

To resolve: Add assim.sequential to uncertainty's Imports



## MODELS  


### basgra

- ModelName-
models\basgra\R\read_restart.BASGRA.R
models\basgra\R\write_restart.BASGRA.R

Probably OK to ignore: used only by Roxygen, so dependency will not be present in version sent to CRAN

- data.land-
models\basgra\R\write.config.BASGRA.R

To resolve: delete commented-out line, then make sure @istfer approves the PR

### biocro

- all-
/inst and /vignettes folder

To resolve: ignore `inst/`, refactor vignettes to avoid using `PEcAn.all`

### cable

- ModelName-
models\cable\tests\testthat.R

Probably OK to ignore: used only by Roxygen, so dependency will not be present in version sent to CRAN


### dalec

- data.atmosphere-
models\dalec\R\met2model.DALEC.R
models\dalec\tests\Rcheck_reference.log

To resolve: add data.atmosphere to DALEC's Imports

- data.land-
models\dalec\R\write.configs.dalec.R
models\dalec\tests\Rcheck_reference.log

To resolve: add data.land to DALEC's Imports

### dvmdostem

- **logger**
models\dvmdostem\R\model2netcdf.dvmdostem.R ( many instances )

To resolve: Add logger to dvmdostem's Imports

### ed(ED2)

- ModelName-
models\ed\R\read_restart.ED2.R
models\ed\R\write_restart.ED2.R

Probably OK to ignore: used only by Roxygen, so dependency will not be present in version sent to CRAN

### linkages

- all-
models\linkages\inst\LINKAGES.lyford.SDA.R
models\linkages\inst\setup_da.R

OK to ignore

- assim.sequential-
models\linkages\inst\LINKAGES.lyford.SDA.R
models\linkages\inst\setup_da.R

OK to ignore

- visualization-
models\linkages\inst\LINKAGES.lyford.SDA.R
models\linkages\inst\setup_da.R

OK to ignore

- allometry-
models\linkages\inst\LINKAGES.lyford.SDA.R

OK to ignore


### maat

- all-
models\maat\vignettes\running_maat_in_pecan.Rmd

To resolve: refactor vignette to avoid using PEcAn.all (may work to simply delete `library(PEcAn.all)` line)

- db-
models\maat\vignettes\create_amerifluxLBL_drivers_for_maat.Rmd

To resolve: Add DB to maat's Suggests

- workflow -
models\maat\vignettes\running_maat_in_pecan.Rmd

To resolve: Add workflow to maat's Suggests


### sipnet

- all-
models\sipnet\inst\SIPNET.lyford.SDA.R

OK to ignore

- assim.sequential-
models\sipnet\inst\SIPNET.lyford.SDA.R

OK to ignore

- visualization-
models\sipnet\inst\SIPNET.lyford.SDA.R

OK to ignore

- allometry-
models\sipnet\inst\SIPNET.lyford.SDA.R

OK to ignore

- ModelName-
models\sipnet\R\read_restart.SIPNET.R

Probably OK to ignore: used only by Roxygen, so dependency will not be present in version sent to CRAN

- data.land-
models\sipnet\R\write.configs.SIPNET.R
models\sipnet\tests\Rcheck_reference.log

To resolve: add data.land to SIPNET's Imports
