# GOES-16 File Naming Convention

File names have the following format:

OR_ABI-L2-MCMIPC-M3_G16_s20181781922189_e20181781924562_c20181781925075.nc

Where:

- **OR** - Indicates the system is operational
- **ABI** - Instrument type
- **L2** - Level 2 Data
- **MCMIP** - Multichannel Cloud and Moisture Imagery products
- **FDC** - Fire Detection and Characterization
- **c** - CONUS file (created every 5 minutes)
- **F** - Full Disk file (created every 10 minutes)
- **M3** - Scan mode
- **G16** - GOES-16
- **sYYYYJJJHHMMSSZ** - Scan start: 4-digit year, 3-digit day of year (Julian day), hour, minute, second, tenth second
- **eYYYYJJJHHMMSSZ** - Scan end
- **cYYYYJJJHHMMSSZ** - File Creation
- **.nc** - NetCDF file extension

To get the fire product files for 1 hour of a specific date:

```python
# files = fs.ls('noaa-goes16/ABI-L2-FDCF/2020/228/07/') # list of 6 files for 2020 day 228, UTC time 15:00, 15:10, 15:20, ..., 15:50