# Overview
This page contains work concerning [libpostal](https://github.com/openvenues/libpostal) done by [Senzing](https://senzing.com/).

Libpostal is an open source address parser library written in C. It has true global coverage, is fast and renders parses of high accuracy. It is used by Senzing in its [Senzing API](https://senzing.com/senzing-api/) product. You can find libpostal here: https://github.com/openvenues/libpostal.

# Senzing data model
Senzing has been working on updates of the libpostal data model for some time. The source data used is the same as libpostal uses, i.e. [Open Street Map](https://www.openstreetmap.org/) and [OpenAddresses](https://openaddresses.io) and newest data from both sources are being used. We do adjustments to the training data to correct errors and improve parses based on customer feedback.
We have included regular updates to the model in our [Senzing API](https://senzing.com/senzing-api/) product.
We are now making our data models available to broader audience.

## Version 1.0.0
This version is composed of 3 files 
- language_classifier.tar.gz - This is the same file default libpostal data model has.
- libpostal_data.tar.gz - This file is also the same as used by default libpostal datamodel.
- parser.tar.gz - This is the new updated parser model.

To download click on the links below and the browser with download them for you:
- https://public-read-libpostal-data.s3.amazonaws.com/v1.0.0/language_classifier.tar.gz
- https://public-read-libpostal-data.s3.amazonaws.com/v1.0.0/libpostal_data.tar.gz
- https://public-read-libpostal-data.s3.amazonaws.com/v1.0.0/parser.tar.gz

or you can use curl
```
curl https://public-read-libpostal-data.s3.amazonaws.com/v1.0.0/language_classifier.tar.gz -o language_classifier.tar.gz
curl https://public-read-libpostal-data.s3.amazonaws.com/v1.0.0/libpostal_data.tar.gz -o libpostal_data.tar.gz
curl https://public-read-libpostal-data.s3.amazonaws.com/v1.0.0/parser.tar.gz -o parser.tar.gz
```

To install extract the file in the libpostal data directory:
```
tar -zxvf ../language_classifier.tar.gz
tar -zxvf ../libpostal_data.tar.gz 
tar -zxvf ../parser.tar.gz
```
Since the data from the 2 first files is already in the libpostal data directory, only the last file really needs to be downloaded and extracted.

Here are some of the improvements this model offers:
- Improved parses for US rural routes
- Improves parses for US addresses without state
- General parsing improvement for Singapore addresses
- General parsing improvement for British addresses
