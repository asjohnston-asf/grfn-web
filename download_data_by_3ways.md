#This document tells you how to download data with API.
0. prerequirement
A new user must register at https://urs.earthdata.nasa.gov/ to get username and password. then use this username/password to login to vertex at https://search.asf.alaska.edu/ and accept end user agreement. After you finish these steps, you are ready to download data.

1. bulkdownload with asf bulk_downaload_tool

In vertex, choose the inetering files, add the selected files to cart, click "download" button, choose the "Download Python Script (py)" to download the python script (for example: download-all-2020-03-25_02-42-54.py) to your computer.

#run the script

$python3 ./download-all-2020-03-25_02-42-54.py

#input username/password, download data in your currrent directory.

2. wget to get a single file or a single zip file.

wget command uses wget.conf to store your username and password. You can create the wget.conf by

$echo 'http_user=CHANGE_ME' >> wget.conf
$echo 'http_password=CHANGE_ME' >> wget.conf

and change the file permission to 6000

$chmod 600 wget.conf

define a environment variable

$export WGETRC="wget.conf"

Now you can get the interesting file name from vertex. for example, S1A_EW_GRDM_1SDH_20151003T040339_20151003T040443_007983_00B2A6_DDE4.zip.
then download the file by

$wget -c "https://datapool.asf.alaska.edu/GRD_MD/SA/S1A_EW_GRDM_1SDH_20151003T040339_20151003T040443_007983_00B2A6_DDE4.zip"

#wget command uses wget.conf to store your username and password. export WGETRC="path/wget.conf"

3. use aria2 to download data

You must have aria2 installed on your computer. Before you run above command, you need create aria2.conf file by

$echo 'http-user=CHANGE_ME' >> aria2.conf
$echo 'http-passwd=CHANGE_ME' >> aria2.conf

and change the file permission to 600 by

$chmod 600 aria2.conf.

If you want to download granule, for example, S1A_EW_GRDM_1SDH_20151003T040339_20151003T040443_007983_00B2A6_DDE4, you can use following command:

$aria2c --conf-path=aria2.conf --http-auth-challenge=true "https://api.daac.asf.alaska.edu/services/search/param?granule_list=S1A_EW_GRDM_1SDH_20151003T040339_20151003T040443_007983_00B2A6_DDE4&output=metalink"

Data are downloaded successfully to current directory.
