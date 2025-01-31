# nanoscopeAFM 2.0.14

* add `AFM.history()` to recreate AFM data object (reproducibility)
* bug fixes for `AFM.crop()`

# nanoscopeAFM 2.0.13

* extract force-distance spectroscopy curves with `AFM.specData()`
* add sample spectroscopy image
* allow GUI to select `AFM.crop()` origin

# nanoscopeAFM 2.0.12

* read images that are not square
* fix units for Phase image in Park AFM images
* update NanoScope image reader for V8
* `AFM.dataType()` has new type of "spectroscopy"
* Use `raster::click()` function to select two points in `AFM.lineProfile()` if coordinates are not provided
* Support pixels for profile scans in `AFM.lineProfile()`


# nanoscopeAFM 2.0.11

* Load Spectroscopy Data from TIFF (Park AFM files), stored into `data$specHead` and `data$specData`


# nanoscopeAFM 2.0.10

* Update the Vignettes and Documentation
* Height-Height Correlation Function Documentation
* Adding AFM image range adjustment
* GraphType=4 and add size to vary the bar description size
* support NID file size for non-square files in `get.NID_imageInfo` (useful for resonance curves)
* load all channels for NID file
* support NID frequency scan
* add sample NID frequency scan file
* fix unassigned variables


# nanoscopeAFM 2.0.9

* Allow to extract different channels using `AFM.getLine`
* Update descriptions and examples


# nanoscopeAFM 2.0.8

* to save space, AFMdata object can drop certain images using `AFM.selectChannel`


# nanoscopeAFM 2.0.7

* update documentation
* functionality to crop images


# nanoscopeAFM 2.0.6

* add function `AFM.getLine()` to pick one particular image line
* make trimPeak=0.01 the default for displaying images
* add cantilever and resonance frequency to AFMinfo


# nanoscopeAFM 2.0.5

* add artificial image generator
* fix profile for images that are not square
* Height-height correlation function integration
* add vignette for Line Profile
* fix x-y line profile directions
* fix bin number in histogram
* add viridis color palette by default, revert back with `redBlue=TRUE`
* create sticker with hexSticker package
* run devtools::test_coverage()
* run rhub::check_for_cran()
* fix several variables to eliminate rchk warnings
* allow `trimPeaks`, which removes extreme points for better contrast
* fix graphing of channels > 1
* add line profiles


# nanoscopeAFM 2.0.4

* update Park image reader
* integrate Igor dependence


# nanoscopeAFM 2.0.3

* allow AFMinfo.item() to return all names
* update vignette with information: 
* rcmdcheck() package and add libraries
* update changelog

# nanoscopeAFM 2.0.2

* Park images and force curves are supported

# nanoscopeAFM 2.0.0

* remove old dependencies
* add new types for AFM plotting, adding graphType = c(1,2)


# nanoscopeAFM 1.1.0

* first release, use to have backwards-compatibility
* change data format of @data in AFMdata structure from data.frame to list to accommodate multiple images
* new reader for AR images
* eliminate z-conversion, since we are saving the units for the z values, just store the converted values
* complete AFMinfo documentation for all 4 instruments

# nanoscopeAFM 1.0.5

* replace x.max.nm with x.conv, and y.conv similar to z.conv; scaling parameters to change units to nm
* add sample description possibility

# nanoscopeAFM 1.0.4

* correct height computation for NanoScope images

# nanoscopeAFM 1.0.3

* some minor fixes to make AFM.raster() work
* add AFM.lineProfile() function (not rendering though yet)
* [Github IO Help Page](https://thomasgredig.github.io/nanoscopeAFM/)

# nanoscopeAFM 1.0.1

* fix channels for AFM import
* include only data$z, generate the others using AFM.raster()


# nanoscopeAFM 1.0

* create S4 class AFMdata
* create print method to display image
* create AFM.import function to generate class AFMdata


# nanoscopeAFM 0.6.6

* update test files:
  - system.file("extdata","Park_20210916_034.tiff",package="nanoscopeAFM")
  - system.file("extdata","AR_20211011.ibw",package="nanoscopeAFM")
  - system.file("extdata","Veeco_20160622.003",package="nanoscopeAFM")
  - system.file("extdata","NanoSurf_20160301.nid",package="nanoscopeAFM")



# nanoscopeAFM 0.6.3

* add notes/comments to INFO
* open MFM images from Igor with Nap files
* using field descriptions: https://github.com/wking/igor/blob/master/igor/binarywave.py


# nanoscopeAFM 0.6.2

* add AFM.info with common information about AFM image


# nanoscopeAFM 0.6.1

* Major update, rename most functions (see README for deprecated functions)
* Add support for Park AFM images in TIFF format
* add images for Veeco, Nanosurf, Park, and Asylum Research
* expand testing (testthat)


# nanoscopeAFM 0.6.0

* support [pgkdown](https://pkgdown.r-lib.org/), use
> pkgdown::build_site()
to build the site and export to [thomasgredig.github.io](https://thomasgredig.github.io)


# nanoscopeAFM 0.5.1

* fixed scales in output
