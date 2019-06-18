# WRFv4.0.3-PlumeMods
Buoyant plume modifications implemented in WRF V 4.0.3

Proper comments have been added to the files mentioned here with a search key 'PlumeMods'

Summary of modifications:

New namelist variables added in WRF-4.0.3/Registry/Registry.EM_COMMON to have user control on the source stregth, size, plume duration and number of layers to perturb
* tke_heat_flux_hot
* heat_flux_len
* heat_flux_wait_mins
* heat_flux_run_mins
* zPerturb

The following directories and files were modified to introduce a buoyant plume in default WRF model: 
      WRF-4.0.3/Registry/Registry.EM_COMMON
      WRF-4.0.3/dyn_em/module_diffusion_em.F
      WRF-4.0.3/dyn_em/module_initialize_ideal.F
      WRF-4.0.3/dyn_em/module_first_rk_step_part2.F

Changes in module_diffusion_em.F
  Main changes are done in this file. Two original subroutines are modified in order to have different heat flux inside the source than the ambience, and, to estimate the buoyancy fluxes because of the temperature difference between the source and the ambience

Changes in module_initialize_ideal.F
  Created a new namelist variable to take the number of layers to perturb for initializing convection 

Changes in module_first_rk_step_part2.F
  Modifications done in module_diffusion_em.F require some changes to the subroutine calls inside this file. 

---06-18-2019---

Currently I am working on modifying the vertical velocity tendencies so that a momentum flux can be added to the plume source

