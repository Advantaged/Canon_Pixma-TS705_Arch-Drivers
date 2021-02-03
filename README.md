# Canon_Pixma-TS705_Arch-and-or-Manjaro_Drivers
Basically this regard the conversion of `*.deb` packages to `*.zst` pakages for and non newbie.

# [Canon PIXMA TS705 Drivers](https://www.canon.de/support/consumer_products/products/fax__multifunctionals/inkjet/pixma_ts_series/pixma-ts705.html?type=drivers&language=de&os=linux%20(64-bit))

### Step 1. Download [Canon PIXMA TS705 Drivers](https://www.canon.de/support/consumer_products/products/fax__multifunctionals/inkjet/pixma_ts_series/pixma-ts705.html?type=drivers&language=de&os=linux%20(64-bit)), choose [(debian Packagearchive)](https://www.canon.de/support/consumer_products/products/fax__multifunctionals/inkjet/pixma_ts_series/pixma-ts705.html?type=drivers&driverdetailid=tcm:83-1821456&os=linux%20%2864-bit%29&language=de).
### Step 2. Unpack the archive with File-manager or Code: 
`tar xzf cnijfilter2-5.80-1-deb.tar.gz`

### Step 3. Inside unpacked archive/folder we find the package of interest, this is: 
`/cnijfilter2-5.80-1-deb/packages/cnijfilter2_5.80-1_amd64.deb`

### Step 4. Install 'debtap' with Code: 
`sudo pacman -S --needed debtap`

### Step 5. Initialize 'debtap' with Code:
`sudo debtap -u`

### Step 6. Convert deb-package to zst-package with Code:
`debtap -q cnijfilter2_5.80-1_amd64.deb`

### Step 7. Install new converted zst-package with Code:
1. Recommended is the installation <span style="color:green">**without**</span> 'ARM-RISK 32-bit' dependencies with Code:

`sudo pacman -Udd cnijfilter2-5.80-1-x86_64.pkg.tar.zst`

2. Installation <span style="color:red">**with**</span> 'ARM-RISK 32-bit' dependencies with Code:

`sudo pacman -U cnijfilter2-5.80-1-x86_64.pkg.tar.zst`

## Remove drivers or any other package (Arch-Linux &/ Manjaro)

`sudo pacman -Rns cnijfilter2-5.80-1-x86_64.pkg.tar.zst`

Thanks again to [Nachlese](https://forum.manjaro.org/u/Nachlese) to helping me!
 
- [x] **Done! & Enjoy!**
