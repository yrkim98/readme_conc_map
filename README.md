# Allen Institute for Cell Science EGFP Molarity Calibrated Imaging Dataset
**Maintainer**: Derek Thirstrup (derekt@alleninstitute.org) and Brian Kim (briank@alleninstitute.org)

## Overview
This package contains raw Zeiss CZI 3D image stacks, EGFP molarity calibration data, associated metadata, and EGFP molarity calibrated image stacks which accompany the publication <insert publication link here> by the [Allen Institute for Cell Science](https://alleninstitute.org/what-we-do/cell-science/).

## Package Feedback
Feedback on benefits and issues you discovered while using this data package is greatly appreciated. The point of contact for this project is listed above.

Much of the data gathered by the Allen Institute for Cell Science has previously been released as zipped or tarred batches of files hosted on our website. This repository provides the same high quality, curated datasets of labeled cell lines, but through Quilt’s loading mechanism.

## Data Organization
The data in this package is organized into separate data sets, reflecting raw image data, and different downstream processing / feature derivation.

The data sets included in this package are listed at the end of this readme.

## Content
Our images are of endogenously-tagged hiPSC, grown on Matrigel-coated 96-well, glass bottom imaging plates. Each 880 field of view (FOV) includes 1 channel (EGFP). Each SDC field of view (FOV) includes 2 channels (BF, EGFP) collected interwoven simultaneously with two cameras (Workflow Pipeline 4.4). You can use the file metadata of each image to target the specific channel you are interested in.

## Access
The dataset is programmatically accessible via quilt, and is also browseable via this web ui with limited functionality.

## Usage
We understand this package is quite large and may not fit on your machine. Here is our list of methods for interacting with this package that work well for us and alleviate the package size burden. If you would like a deeper understanding of what all you can do with Quilt, please refer to their documentation.
**To Load The Package**:

`import quilt3`

`pkg = quilt3.Package.browse("aics/concentration_map", registry="s3://allencell-internal-quilt")`

You can use the quilt package (quilt3.Package) object to navigate around the dataset using dictionary accessors like so:

`sub_package = pkg["2020-05-26"]["ZSD1"]["100x_zstack"]

To then download individual file to your local disk you can use the fetch function:

`fetched_image = sub_package.fetch("/100x_zstack/")

You can also download the whole subfolder with the fetch function:

`fetched_folder = example_image.fetch()  # Download whole folder at /2020-05-26/ZSD1/100x_zstack`


This dataset is large (2.8TB), so it is reccomended you only download the files you need. However, the whole package can be downloaded:

`p = quilt3.Package.browse('aics/concentration_map', 's3://allencell-internal-quilt')`

`p.fetch()`

**For additional documenation on how to use and interact with this dataset please refer to** https://docs.quiltdata.com/walkthrough/reading-from-a-package.
## List of Datasets

 * \2020-05-26\ZSD1
 * \2020-05-26\LSM880-2
 * \2020-02-25\ZSD1
 * \2020-02-25\ZSD3
 * \2020-02-25\LSM880-2
 * \2020-07-06\ZSD1
 * \2020-07-06\LSM880-1
 * \2020-05-27\LSM880-2
 * \2020-05-05\ZSD1
 * \2020-05-05\ZSD3
 * \2020-05-05\LSM880-2
 * \2020-05-05\LSM880-1
 * \2019-05-20\LSM880-2
 * \2019-05-20\LSM880-1
 * \2020-02-03\ZSD1
 * \2020-02-03\ZSD3
 * \2020-02-03\LSM880-2
 * \2020-02-03\ZSD2
 * \2020-02-21\ZSD1
 * \2020-02-21\ZSD3
 * \2020-02-21\LSM880-2
 * \2020-02-21\LSM880-1
 * \2020-02-21\ZSD2
 * \2019-07-09\LSM880-2
 * \2019-05-07\LSM880-2
 * \2019-05-07\LSM880-1
 * \2019-08-16\LSM880-1
 * \2019-07-08\LSM880-1
 * \2020-01-30\ZSD1
 * \2020-01-30\ZSD3
 * \2020-01-30\LSM880-2
 * \2020-01-30\ZSD0
 * \2020-01-30\ZSD2
 * \2020-03-02\ZSD1
 * \2020-03-02\ZSD3
 * \2020-03-02\LSM880-2
 * \2020-03-02\ZSD2
 * \2019-05-31\ZSD1
 * \2019-05-31\ZSD3
 * \2019-05-31\LSM880-1
 * \2019-06-18\LSM880-2
 * \2019-06-18\LSM880-1
 * \2020-02-14\ZSD1
 * \2020-02-14\ZSD3
 * \2020-02-14\LSM880-2
 * \2020-02-14\ZSD2
 * \2020-06-05\ZSD1
 * \2020-06-05\LSM880-1
 * \2019-05-17\LSM880-2
 * \2019-05-17\LSM880-1
 * \2019-09-16\LSM880-1
 * \2019-12-17\LSM880-2
 * \2019-12-17\LLS7
 * \2019-12-17\LSM880-1
 * \2020-07-01\LLS7
 * \2020-07-01\LSM880-1
 * \2020-03-03\ZSD1
 * \2020-03-03\ZSD3
 * \2020-03-03\LSM880-2
 * \2020-02-05\ZSD1
 * \2020-02-05\ZSD3
 * \2020-02-05\LSM880-2
 * \2020-02-05\ZSD2
 * \2020-03-04\ZSD1
 * \2020-03-04\ZSD3
 * \2020-03-04\LSM880-2
 * \2020-03-04\LLS7
 * \2019-05-13\LSM880-2
 * \2019-05-13\LSM880-1
 * \2019-05-21\LSM880-2
 * \2019-05-21\LSM880-1
 * \2019-12-16\ZSD1
 * \2019-12-16\ZSD3
 * \2019-12-16\LSM880-2
 * \2019-12-16\LSM880-1
 * \2020-02-10\ZSD1
 * \2020-02-10\ZSD3
 * \2020-02-10\LSM880-2
 * \2020-02-10\ZSD2
 * \2019-06-07\LSM880-1
 * \2019-05-08\LSM880-2
 * \2019-11-22\LSM880-2
 * \2019-11-22\LLS7
 * \2019-11-22\LSM880-1
 * \2019-06-03\ZSD1
 * \2019-06-03\ZSD3
 * \2019-06-03\LSM880-1
 * \2020-02-24\ZSD1
 * \2020-02-24\ZSD3
 * \2020-02-24\LSM880-2
 * \2020-02-24\ZSD2
 * \2020-06-25\LLS7
 * \2020-06-25\LSM880-1
 * \2020-02-28\ZSD1
 * \2020-02-28\ZSD3
 * \2020-02-28\LSM880-2
 * \2019-08-07\LSM880-1
 * \2020-01-31\ZSD1
 * \2020-01-31\ZSD3
 * \2020-01-31\LSM880-2
 * \2020-01-31\ZSD2
 * \2019-05-06\LSM880-2
 * \2019-05-06\LSM880-1
 * \2020-06-12\LLS7
 * \2020-06-12\LSM880-1
 * \2019-05-30\LSM880-2
 * \2019-05-30\LSM880-1
 * \2020-05-12\LSM880-2
 * \2020-01-27\ZSD1
 * \2020-01-27\ZSD3
 * \2020-01-27\LSM880-2
 * \2020-07-21\ZSD1
 * \2020-07-21\LSM880-2
 * \2020-07-21\LLS7
 * \2020-01-28\ZSD1
 * \2020-01-28\ZSD3
 * \2020-01-28\LSM880-2
 * \2020-01-28\ZSD2
 * \2019-06-04\LSM880-1
 * \2019-05-24\LSM880-1
 * \2020-02-04\ZSD1
 * \2020-02-04\ZSD3
 * \2020-02-04\LSM880-2
 * \2020-02-04\ZSD2
 * \2019-06-20\LSM880-1
 * \2019-09-10\LSM880-1
 * \2019-06-05\LSM880-1
 * \2019-11-25\LSM880-2
 * \2019-11-25\LLS7
 * \2019-11-25\LSM880-1
 * \TestData\2020-03-04\ZSD1
 * \TestData\2020-03-04\ZSD3
 * \TestData\2020-03-04\LSM880-2
 * \TestData\2020-03-04\LLS7
 * \CalibratedImagesStatistics\2019-12-17\LSM880-2
 * \CalibratedImagesStatistics\2019-12-17\LSM880-1

## Distribution
This package was created and distributed by [Brian Kim](mailto:brian.kim@alleninstitute.org) using Quilt3.

## License
For questions on licensing please refer to https://www.allencell.org/terms-of-use.html.
