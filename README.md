# WRFv4.0.3-PlumeMods
Buoyant plume modifications implemented in WRF V 4.0.3

Summary of modifications:

New namelist variables added in WRF-4.0.3/Registry/Registry.EM_COMMON to have user control on the source stregth, size and durations
  tke_heat_flux_hot
  heat_flux_len
  heat_flux_wait_mins
  heat_flux_run_mins
  zPerturb

Proper comments have been added to the files mentioned here with a search key 'PlumeMods'

The following directories and files were modified to introduce a buoyant plume in default WRF model: 
WRF-4.0.3/dyn_em/module_diffusion_em.F
WRF-4.0.3/dyn_em/module_initialize_ideal.F
WRF-4.0.3/dyn_em/module_first_rk_step_part2.F





