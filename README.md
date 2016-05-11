# **SAIVT Semantic Person Search Database**

## **Overview**

The SAIVT Semantic Person Search Database was developed to provide a suitable platform to develop and evaluate techniques that search for a person using a semantic query (i.e. tall, red shirt, jeans). Sequences for 110 subjects consisting of 30 initialisation frames (to, for instance, learn a background model), a number of annotated frames containing the target subject, and a description of the subject incorporating a number of traits including clothing type and colour, gender, height and build are provided.

You can [read our paper](http://eprints.qut.edu.au/72887/) on eprints

Contact Dr Simon Denman (s dot denman at qut dot edu dot au) for further information.

## **Licensing**

The SAIVT-SoftBioSearch database is © 2012 QUT and is licensed under the [Creative Commons Attribution-ShareAlike 3.0 Australia License] (http://creativecommons.org/licenses/by-sa/3.0/).

## **Attribution**

To attribute this database, please include the following citation:

> Halstead, Michael, Denman, Simon, Sridharan, Sridha, & Fookes, Clinton B. (2014) Locating People in Video from Semantic Descriptions : A New Database and Approach. In the 22nd International Conference on Pattern Recognition, 24 - 28 August 2014, Stockholm, Sweden.
 
Our paper is available on [eprints](http://eprints.qut.edu.au/72887/).

## **Acknowledging the Database in your Publications**

In addition to citing our paper, we kindly request that the following text be included in an acknowledgements section at the end of your publications:

> We would like to thank the SAIVT Research Labs at Queensland University of Technology (QUT) for freely supplying us with the SAIVT-SoftBioSearch database for our research.

## **Installing the SAIVT-SoftBioSearch Database**

Download and unzip the following archives:

- [SAIVT-SoftBioSearchDB.tar.gz (157 MB)] (https://Q0102-RO:Vieyae3G@q0102.qcloud.qcif.edu.au/SAIVT-SoftBioSearchDB.tar.gz)
- [SAIVT-SoftBioSearchDB-C1.tar.gz (1.6 GB)] (https://Q0102-RO:Vieyae3G@q0102.qcloud.qcif.edu.au/SAIVT-SoftBioSearchDB-C1.tar.gz)
- [SAIVT-SoftBioSearchDB-C2.tar.gz (1.0 GB)] (https://Q0102-RO:Vieyae3G@q0102.qcloud.qcif.edu.au/SAIVT-SoftBioSearchDB-C2.tar.gz)
- [SAIVT-SoftBioSearchDB-C3.tar.gz (1.5 GB)] (https://Q0102-RO:Vieyae3G@q0102.qcloud.qcif.edu.au/SAIVT-SoftBioSearchDB-C3.tar.gz)
- [SAIVT-SoftBioSearchDB-C4.tar.gz (908 MB)] (https://Q0102-RO:Vieyae3G@q0102.qcloud.qcif.edu.au/SAIVT-SoftBioSearchDB-C4.tar.gz)
- [SAIVT-SoftBioSearchDB-C5.tar.gz (858 MB)] (https://Q0102-RO:Vieyae3G@q0102.qcloud.qcif.edu.au/SAIVT-SoftBioSearchDB-C5.tar.gz)
- [SAIVT-SoftBioSearchDB-C6.tar.gz (591 MB)] (https://Q0102-RO:Vieyae3G@q0102.qcloud.qcif.edu.au/SAIVT-SoftBioSearchDB-C6.tar.gz)

At this point, you should have the following data structure and the SAIVT-SoftBioSearch database is installed:
```
SAIVT-SoftBioSearch 
+-- C1-BlackBlueStripe-BlueJeans 
+-- C1-BlackShirt-PinkShorts 
+-- ... 
+-- C6-YellowWhiteSpotDress 
+-- Calibration 
+-- Data 
+-- CultureColours 
+-- Black 
+-- Blue 
+-- ... 
+-- Videos 
+-- Cam1 
+-- Cam2 
+-- ... 
+-- Halstead 2014 - Locating People in Video from Semantic Descriptions.pdf 
+-- LICENSE.txt 
+-- README.txt (this document) 
+-- SAIVTSoftBioDatabase.xml
```

Sequences for the individual subjects are contained within the directories named C[1..6]-[TorsoDescription]-[LegDescription]. There are 110 subjects captured from six different cameras. Each directory contains an XML file with the annotation for that sequence, and the images that belong to the sequence. For each sequence, the first 30 frames are reserved for updating/learning a background model, and as such have no annotation.

The 'Calibration' directory contains a camera calibration (using Tsai's method) for the six cameras used in the database.

The 'Data' directory contains additional data that may of use. In particular, it contains a collection of colour patches within 'Data/CultureColours' that can be used to train models for a specific colour. It also contains a set of patches for skin, and for non-skin colours. 'Data/Videos' contains videos for each camera, that can be used to learn the background. It should also be noted that for a portion of the time when the database was captured, a temporary wall was up due to construction works. This impacted the following sequences captured from cameras 1 and 6:
- Camera1 
  - C1-GreenWhiteHorizontal-BlackPants 
  - C1-RedCheck-BlackSkirt 
  - C1-GreenCheck-BrownPants
- Camera6 
  - C6-GreenFaceCover-Blue-Blue 
  - C6-YellowWhiteSpotDress

Additional videos for these cameras are also included and are named CamX_Wall.avi. The 'SAIVTSoftBioSearchDB.xml' file defines the database. This file specifies the cameras and their calibrations/background sequences, includes definitions for the traits/soft biometrics, and lists the sequences.

This paper is also available alongside this document in the file 'Halstead 2014 - Locating People in Video from Semantic Descriptions.pdf'.
