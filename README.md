
## About

dcm_qa_enh is a simple DICOM to NIfTI validator script and dataset to test conversion of Enhanced DICOM datasets to the NIfTI format.

## DataSets

* Generic/
  * source:  ftp://medical.nema.org/medical/Dicom/DataSets/WG30/MGH/MR/
  * note: see ftp source for raw unenhanced data. Converted to provide reference for enhanced format.
  * note: images converted to enhanced using [PixelMed](http://www.pixelmed.com/dicomtoolkit.html)
  * acquired on a [15T small bore system](https://www.nmr.mgh.harvard.edu/lab/15t-mr-laboratory).
  * version: n.b. conversion to enhanced using PixelMed. (0018,1020) LO [syngo MR B15]


* Siemens/XA10
  * source: [Jeffrey Luci, The University of Texas at Austin](https://github.com/rordenlab/dcm2niix/issues/240)
  * note: [XA11 multi-band sequences can inaccurately report single-band values in 0021,1104](https://github.com/rordenlab/dcm2niix/issues/303)
  * note: see [Siemens](https://github.com/rordenlab/dcm2niix/tree/master/Siemens) page.
  * version: (0018,1020) LO [syngo MR XA10]

## Philips

* Philips/
  * source: [Baxter Rogers, Vanderbilt University](https://github.com/rordenlab/dcm2niix/issues/363)
  * additional examples: [NITRC](https://www.nitrc.org/plugins/mwiki/index.php/dcm2nii:MainPage)
  * model: (0008,1090) Achieva dStream
  * version: (0018,1020) LO [5.3.0\5.3.0.3]

## Links

 * [NITRC dcm2niix page](https://www.nitrc.org/plugins/mwiki/index.php/dcm2nii:MainPage) hosts many enhanced DICOM samples. In particular, the [Unusual](https://www.nitrc.org/plugins/mwiki/index.php/dcm2nii:MainPage#Unusual_MRI) Philips image where a unique intensity scaling is applied to each 2D slice, which can result in [banding](https://github.com/rordenlab/dcm2niix/issues/363) if not taken into account.