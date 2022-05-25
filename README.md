# ECON-WOCAT Harmonisation and Analysis Script

The goal of the project is to harmonise the WOCAT SLM data and perform an analysis of the costs and benefits of a selected 500+ documented SLM Technologies.

In order to support SLM/LDN project and programme design, the project produces a new open access ECON-WOCAT Database and Dashboard with a related methodological paper.

In addition, a policy brief shall help sharing results of the analysis and create awareness amongst decision-makers on costs and benefits of SLM, i.e. the investments needs and impact expected.

[Product page](https://www.wocat.net/en/projects-and-countries/projects/costs-and-benefits-slm-technologies)

## Pre-requisites

There are a couple of pre-requisites required to run this script:

- A WOCAT API Auth Token
- A copy of the [QCAT API Scripts](https://github.com/CDE-UNIBE/qcat-api-scripts)

The script assumes the following project structure:

```bash
project
│
└───qcat-api-scripts
│   │   ...
│   │
│   └───config
│   │   │   tech.py
│   │   │   ...
│   │
│   └───output
│       │   tech.csv
│   
└───ECON-WOCAT
    │   API Response Analysis.ipynb
    │   ...
```

## Installation

Follow the installation instructions for the [QCAT API Scripts](https://github.com/CDE-UNIBE/qcat-api-scripts) to setup that script.

Within the ECON-WOCAT directory the required packages need to be installed before running the script.

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

## Usage

The default qcat-api-scripts config file needs to be replaced with the `tech.py` file from this directory.

Then run the qcat api script with your auth token to generate the output file with the latest questionnaire data, further instructions can be found here: [QCAT API Scripts](https://github.com/CDE-UNIBE/qcat-api-scripts).

Start a jupyter notebook session and run all cells in the `API Response Analysis` file. The exported dataset can be found in `cleaned_dataset.xlsx` which will require some additional formatting before it is published.

## License

[MIT](https://choosealicense.com/licenses/mit/)

Copyright (c) 2022 Altus Impact

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
