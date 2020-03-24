# Sentinel-1 Interferograms

Sentinel-1 Interferogram (BETA) products are prototype Level 2 [interferometric products](https://asf.alaska.edu/data-sets/derived-data-sets/insar/) produced as part of the [Getting Ready for NISAR](https://earthdata.nasa.gov/learn/articles/tools-and-technology-articles/getting-ready-for-nisar) (GRFN) project using the ARIA Science Data System under development for the NASA-ISRO Synthetic Aperture Radar (NISAR) mission. The creation, discovery, and distribution of these products is to inform the NISAR mission team of possible cloud-based processing and data-management solutions. As such, these prototype products are not part of the ASF long-term archive, and may become unavailable at any time as new SAR interferometric processing and delivery methods are explored.

## Products

Sentinel-1 interferograms are available as [NetCDF-4](https://www.unidata.ucar.edu/software/netcdf/docs/netcdf_introduction.html) products including the following science data:

- Unwrapped Phase
- Coherence
- Amplitude
- Connected components

Each data layer is also available as a stand-alone GeoTiff product.

More information is available in the full [product specification](https://aria.jpl.nasa.gov/node/97).

## Processor

Products were processed using Jet Propulsion Laboratory’s (JPL’s) [ARIA Science Data System](https://aria.jpl.nasa.gov/) under development for the NISAR mission, using the [InSAR Scientific Computing Environment](https://github.com/isce-framework/isce2) (ISCE) software package.
