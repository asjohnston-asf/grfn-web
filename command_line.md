# Sentinel-1 Interferograms – Command Line Tools

There are many ways to access Sentinel-1 interferograms for users comfortable working at the command line. Below are steps and options to explore.

## Find Interferograms via the CMR Search API

Sentinel-1 Interferogram (BETA) products are integrated with the ESDIS Common Metadata Repository (CMR), and are searchable via the CMR Search API. Visit the [CMR Search API](https://cmr.earthdata.nasa.gov/search/site/docs/search/api.html) documentation for details and available search parameters.

The CMR collection concept IDs for Sentinel-1 Interferogram (BETA) products are:

- C1595422627-ASF — Sentinel-1 Interferograms (BETA)
- C1596065640-ASF — Sentinel-1 Interferograms - Amplitude (BETA)
- C1596065639-ASF — Sentinel-1 Interferograms - Coherence (BETA)
- C1596065641-ASF — Sentinel-1 Interferograms - Connected Components (BETA)
- C1595765183-ASF — Sentinel-1 Interferograms - Unwrapped Phase (BETA)

For example, this search returns a list of all “Sentinel-1 Interferogram (BETA)” products over Pasadena, CA since Jan 1, 2018:

`https://cmr.earthdata.nasa.gov/search/granules.csv?collection_concept_id=C1595422627-ASF&temporal=2018-01-01T00:00:00Z,&point=-118.1445,34.1478&page_size=50`

The download URL for each product can be extracted from CMR search results and downloaded via command line tools like cURL and Wget.

## Get Interferograms via cURL and Wget

Visit [How To Access Data With cURL and Wget](https://wiki.earthdata.nasa.gov/display/EL/How+To+Access+Data+With+cURL+And+Wget) for instructions on downloading products with cURL and Wget, including how to provide your Earthdata Login credentials via a .netrc file.
