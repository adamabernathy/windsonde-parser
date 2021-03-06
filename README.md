# Cup-sonde Parser
Data file parser for Sparv Embedded WINDSOND<sup>(TM)</sup> R1 "cup sonde".

[![Build Status](https://travis-ci.org/adamabernathy/windsond-parser.svg?branch=master)](https://travis-ci.org/adamabernathy/windsond-parser)

---
Made with :heart: by Adam C. Abernathy (http://www.adamabernathy.com)


## Summary
Parses observational data from Sparv Embedded WINDSOND sounding (granule) output and saves the data to a CSV file for use in other scientific applications.  If you like this product and want to help expand it, feel free to make a Fork, Feature or Pull request.


## Usage
    perl sonde-parser.pl
        --file=<granule name>
        --alt=<inital altitude in meters>

If `alt` is not declared the default value is used.  This is set internally.


## Script output
The script will produce an output file based on the starting time of the granule.  The table layout is as follows:

| Variable      | Description                   | Units             |
| ------------- | ----------------------------- | ----------------- |
| IDX           | Profile record number         | none              |
| UNIX-TIME     | Profile UNIX timestamp        | seconds           |
| SYS-NSAT      | Profile No. of Satellites     | none              |
| SYS-VOLT      | Profile battery voltage       | Volts             |
| GEO-LAT       | Profile geodetic latitude     | Degrees North     |
| GEO-LON       | Profile geodetic longitude    | Degrees East      |
| GEO-ELEV      | Profile geodetic elevation    | Meters            |
| DAT-TMPC      | Profile temperature           | Celsius           |
| DAT-RH        | Profile relative humidity     | Percent           |
| DAT-PRES      | Profile pressure              | Pascals           |


**Important**
  - For `geo_lat` and `geo_lon` an multiplier of 1e-6 needs to be applied.

## Version History
See change log for details.

## Legalese
I am in no way affiliated with Sparv Embedded AB. This software is licensed under the Apache 2.0 license.

Copyright 2016 Adam C. Abernathy, (adamabernathy@gmail.com)

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License.  You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.
