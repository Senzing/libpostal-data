# Overview

This page contains work concerning [libpostal] done by [Senzing].

Libpostal is an open source address parser library written in C. It has true global coverage, is fast and renders parses of high accuracy. It is used by Senzing in its [Senzing API] product. You can find libpostal here: https://github.com/openvenues/libpostal.

# Senzing data model

Senzing has been working on updates of the libpostal data model for some time. The source data used is the same as libpostal uses, i.e. [Open Street Map] and [OpenAddresses] and newest data from both sources are being used. We do adjustments to the training data to correct errors and improve parses based on customer feedback.
We have included regular updates to the model in our [Senzing API] product.
We are now making our data models available to broader audience.

## Version 1.1.0

This version is composed of 3 files

- language_classifier.tar.gz - This is the same file default libpostal data model has.
- libpostal_data.tar.gz - This file is also the same as used by default libpostal datamodel.
- parser.tar.gz - This is the new updated parser model.

To download click on the links below and the browser with download them for you:

- https://public-read-libpostal-data.s3.amazonaws.com/v1.1.0/language_classifier.tar.gz
- https://public-read-libpostal-data.s3.amazonaws.com/v1.1.0/libpostal_data.tar.gz
- https://public-read-libpostal-data.s3.amazonaws.com/v1.1.0/parser.tar.gz

or you can use curl

```
curl https://public-read-libpostal-data.s3.amazonaws.com/v1.1.0/language_classifier.tar.gz -o language_classifier.tar.gz
curl https://public-read-libpostal-data.s3.amazonaws.com/v1.1.0/libpostal_data.tar.gz -o libpostal_data.tar.gz
curl https://public-read-libpostal-data.s3.amazonaws.com/v1.1.0/parser.tar.gz -o parser.tar.gz
```

To install extract the file in the libpostal data directory:

```
tar -zxvf ../language_classifier.tar.gz
tar -zxvf ../libpostal_data.tar.gz
tar -zxvf ../parser.tar.gz
```

### Changes and improvements from version 1.0.0

- Latest data from all sources
- Improved parses for Japanese addresses
- Improved handling of Mexican state codes

### Quality

We have made some modification to our test data set to improve variations of address and test for improvements we made in this version. It now has 12951 addresses from 89 countries.
The over all parsing accuracy improved by 1.09%. We had improved statistics for 33 countries and had regression with 10.
You can find [statistical comparison of the tests here].
The bulk of the [test data we used is located here]. We removed about 100 records from the test set, because we don't have permissions to publish them.

### Training data

The data we used for creating the data model is available for download. There are total over 1.7 billion lines in 8 files. To download click the links below:

- https://public-read-libpostal-data.s3.amazonaws.com/v1.1.0/training_data/formatted_addresses_tagged_random.tsv.tgz
- https://public-read-libpostal-data.s3.amazonaws.com/v1.1.0/training_data/formatted_places_tagged_random.tsv.tgz
- https://public-read-libpostal-data.s3.amazonaws.com/v1.1.0/training_data/formatted_ways_tagged_random.tsv.tgz
- https://public-read-libpostal-data.s3.amazonaws.com/v1.1.0/training_data/geoplanet_formatted_addresses_tagged_random.tsv.tgz
- https://public-read-libpostal-data.s3.amazonaws.com/v1.1.0/training_data/intersections_tagged_random.tsv.tgz
- https://public-read-libpostal-data.s3.amazonaws.com/v1.1.0/training_data/openaddress_uk_formatted_random.tsv.tgz
- https://public-read-libpostal-data.s3.amazonaws.com/v1.1.0/training_data/openaddresses_formatted_addresses_tagged_random.tsv.tgz
- https://public-read-libpostal-data.s3.amazonaws.com/v1.1.0/training_data/senzing_formatted_random.tsv.tgz

Once downloaded, extract them with

```
tar -zxvf <file name>
```

## Version 1.0.0

This version is composed of 3 files

- language_classifier.tar.gz - This is the same file default libpostal data model has.
- libpostal_data.tar.gz - The address dictionary was updated.
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

### What this version addresses

Here are some of the improvements this model offers:

- Latest data from all sources
- Improved parses for US rural routes
- Improves parses for US addresses without state
- Improvements for addresses with unit numbers but no "#,apt,unit" etc in front of it
- General parsing improvement for Singapore addresses
- General parsing improvement for British addresses

### Quality

We have a data set of 12950 addresses from 89 countries that we use to test and verify the quality of our models. The data set was generated using random addresses from OSM, minimally 50 per country. Hard-to-parse addresses were gotten from Senzing support team and customers and from the libpostal github page and added to this set. We ran this data through and compared the results to the default libpostal model.
You can find statistical [comparison of the tests here].

A spreadsheet with more details about the results can be downloaded here: [Parsing_comparison.xls].

[comparison of the tests here]: ./files/stats/v1/Parsing_comparison.md
[libpostal]: https://github.com/openvenues/libpostal
[Open Street Map]: https://www.openstreetmap.org/
[OpenAddresses]: https://openaddresses.io
[Parsing_comparison.xls]: https://github.com/Senzing/libpostal-data/blob/main/files/stats/v1/Parsing_comparison.xls
[Senzing API]: https://senzing.com/senzing-api/
[Senzing]: https://senzing.com/
[statistical comparison of the tests here]: ./files/stats/v1.1.0/Parsing_comparison_v1_1_0.md
[test data we used is located here]: ./files/tests/v1.1.0/test_data.csv
