# .vtk to .szplt convertor
This script can convert .vtk rectilinear grid files to .dat or .szplt files for viewing in Tecplot

## Enabling Conversions .xdmf / .vtr / .vtk to Tecplot .dat / .tec / .plt / .szplt

## Instructions
Working in Linux
1. Open Paraview readable formats in Paraview. 
2. File>Save Data...>select format as legacy .vtk and ascii.
3. Keep .vtk file in the folder containing script.
4. Copy libtecio.so from Tecplot path/to/tecplot/installation/bin to tecio directory
5. Run script:

   for output as .szplt

	```sh
			python vtk2tecplot.py szplt 
	```

   for output as .dat

	```sh
			python vtk2tecplot.py dat 
	```

## Dependencies
1. Numpy
2. TECIO.dll (included)
3. tecio_szl.py from github.com/Tecplot/handyscripts/tree/master/python/dataconversion/ (included)
4. libtecio.so or tecio.dll (not included)


Very limited testing done! Sucessfully converts a .vtk file generated by paraview from a 3d flow simulation snapshot to .dat and .szplt file readable by tecplot. May need modifications to work with 2D plots, different type of grid, etc.


