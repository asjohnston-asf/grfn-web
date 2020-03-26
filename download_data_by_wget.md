#This document tells you how to download data with API.
0. prerequirement
newew user must register at https://urs.earthdata.nasa.gov/. login to vertex at https://search.asf.alaska.edu/ and accept end user agreement.

1. bulkdownload with asf bulk_downaload_tool

in vertex, choose the inetering files, add the selected files to cart, click "download" button, choose the "Download Python Script (py)" to download the python script (for example: download-all-2020-03-25_02-42-54.py) to your computer.

#run the script

$python3 ./download-all-2020-03-25_02-42-54.py

#input username/password, download data in your currrent directory.

2. wget to get a single file or a single zip file.

you can get the file name from vertex. for example, S1A_EW_GRDM_1SDH_20151003T040339_20151003T040443_007983_00B2A6_DDE4.zip.

wget -c "https://datapool.asf.alaska.edu/GRD_MD/SA/S1A_EW_GRDM_1SDH_20151003T040339_20151003T040443_007983_00B2A6_DDE4.zip"

#wget command uses wget.conf to store your username and password. export WGETRC="path/wget.conf"



