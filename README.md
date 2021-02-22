# mozbc_for_WRFv3.9
Modify the WRF-Chem preprocessor tool (mozbc) to work with the hybrid sigma-pressure vertical coordinate introduced with WRF V3.9.
The WRF-Chem preprocessor tool (mozbc) is used to creates chemical lateral boundary and initial conditions from global chemistry model output. 
WRF model introduced the hybrid sigma-pressure vertical coordinated in Version 3.9. Mozbc only works with the terrain-following vertical coordinate. The sourcecode of mozbc can be obtained from https://www.acom.ucar.edu/wrf-chem/download.shtml. We modified the definition of the dry air pressure with the hybrid sigma-pressure vertical coordinate in two files (main_bc_wrfchem.f90 and mo_mozart_lib.f90).
Please download the modified verison of mozbc used for WRF-GC model.
To build mozbc:
              mkdir /your/dir/mozbc
              cd /your/dir/mozbc
              tar -xvf mozbc_for_WRFv3.9.tar
              chmod 777 *
              ./make_mozbc
