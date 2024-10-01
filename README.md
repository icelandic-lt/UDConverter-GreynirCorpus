# UDConverter-GreynirCorpus - Treebank format converter

![Version](https://img.shields.io/badge/Version-1.0|22.06-darkviolet)
![Python](https://img.shields.io/badge/python-3.9-blue?logo=python&logoColor=white)
![Python](https://img.shields.io/badge/python-3.10-blue?logo=python&logoColor=white)
![CI Status](https://img.shields.io/badge/CI-[unavailable]-red)
![Docker](https://img.shields.io/badge/Docker-[unavailable]-red)

UDConverter for GreynirCorpus is a tool for converting the constituency treebanks of [GreynirCorpus](http://hdl.handle.net/20.500.12537/119) to dependency treebanks following the Universal Dependencies framework. 

## Overview
- **Language:** Python
- **Language Version/Dialect:**
  - Python: 3.9, 3.10
- **Category:** [Support Tools](https://github.com/icelandic-lt/icelandic-lt/blob/main/doc/st.md)
- **Domain:** Generic
- **Status:** Stable
- **Origins:** [UDConverter for GreynirCorpus 22.06](http://hdl.handle.net/20.500.12537/222) and [Github](https://github.com/thorunna/UDConverter-GreynirCorpus).

## Description

A Python module for converting the [GreynirCorpus](https://github.com/mideind/GreynirCorpus) treebank to the [Universal Dependencies](https://universaldependencies.org/) framework. The module has been adapted from [UDConverter](https://github.com/thorunna/UDConverter).

The resulting UD treebank will be included in UD version 2.11.

## Installation

Install all requirements by running: 

``` shell
python3 -m venv .venv && . .venv/bin/activate # optionally create and activate a virtual environment
pip install -r requirements.txt
```

## Usage

Scripts to run are in the `scripts` directory, and need to be run from there.

_In all examples below, the_ `--output` _flag is used to write to files in the_ `/CoNLLU/` _output folder. Otherwise prints to standard output._

*Convert single file or directory of files:*

``` shell
python convert.py -N -i path/to/corpus/file.psd --output --post_process
convert.py -N -i path/to/corpus/* --output --post_process
```

_For further usage, input files must be placed in a folder within the_ `corpora` _directory_

*Convert single tree in treebank using sentence ID (only prints to standard output):*

``` shell
python convert.py -C FOLDER_NAME -id SENTENCE_ID
```

*Convert single file in treebank*

``` shell
python convert.py -C FOLDER_NAME -f FILE_NAME --output --post_process
```

## License

Copyright 2022 The Árni Magnússon Institue for Icelandic Studies

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

## Acknowledgements

This converter was adapted as part of the Language Technology Programme for Icelandic 2019-2023. The programme, which is managed and coordinated by Almannarómur (https://almannaromur.is/), is funded by the Icelandic Ministry of Education, Science and Culture.
