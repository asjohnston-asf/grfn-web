# Sentinel-1 Interferograms – Command Line Tools

There are many ways to access Sentinel-1 interferograms for users comfortable working at the command line. Below are steps and options to explore.

## Find Interferograms via the ASF Search API

Sentinel-1 Interferogram (BETA) products are searchable via the [ASF Search API](https://asf.alaska.edu/api/).  Visit the  documentation for details and available search parameters.

Interferograms are most easily searched using these values for the `processinglevel` keyword:

- GUNW_STD — Standard Product, NetCDF
- GUNW_AMP — Amplitude, GeoTIFF
- GUNW_COH — Coherence, GeoTIFF
- GUNW_CON — Connected Components, GeoTIFF
- GUNW_UNW — Unwrapped Phase, GeoTIFF

For example, this search returns a list of "Standard Product, NetCDF" products over Pasadena, CA since Jan 1, 2018:

`https://api.daac.asf.alaska.edu/services/search/param?processinglevel=GUNW_STD&start=2018-01-01&intersectswith=point(-118.1445+34.1478)&output=csv&maxResults=50`

## Find Interferograms via the CMR Search API

Sentinel-1 Interferogram (BETA) products are integrated with the ESDIS Common Metadata Repository (CMR), and are searchable via the [CMR Search API](https://cmr.earthdata.nasa.gov/search/site/docs/search/api.html).  Visit the documentation for details and available search parameters.

Interferograms are most easily searched using these values for the `collection_concept_id` parameter:

- C1595422627-ASF — Standard Product, NetCDF
- C1596065640-ASF — Amplitude, GeoTIFF
- C1596065639-ASF — Coherence, GeoTIFF
- C1596065641-ASF — Connected Components, GeoTIFF
- C1595765183-ASF — Unwrapped Phase, GeoTIFF

For example, this search returns a list of "Standard Product, NetCDF" products over Pasadena, CA since Jan 1, 2018:

`https://cmr.earthdata.nasa.gov/search/granules.csv?collection_concept_id=C1595422627-ASF&temporal=2018-01-01T00:00:00Z,&point=-118.1445,34.1478&page_size=50`

## Get Interferograms via cURL and Wget

The download URL for each product can be extracted from search results and downloaded via command line tools like cURL and Wget.

Visit [How To Access Data With cURL and Wget](https://wiki.earthdata.nasa.gov/display/EL/How+To+Access+Data+With+cURL+And+Wget) for instructions on downloading products, including how to provide your Earthdata Login credentials via a .netrc file.
