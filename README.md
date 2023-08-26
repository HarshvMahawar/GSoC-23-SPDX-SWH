# GSoC'23 @ SPDX-SWH
Report of Google Summer of Code 2023 @ SPDX
| Project Details |  |
|----------|:--------:|
| Initial Proposal |  [Generation of SPDX documents of origins @ Software Heritage](https://drive.google.com/file/d/1ymBVZ2PZfTO9GnWU-Neh7i6m-jZtBhUc/view?usp=sharing)   |
| Repository   |   [swh-spdx](https://gitlab.softwareheritage.org/swh/devel/swh-spdx)   |
| Mentors    |   [David Douard](https://gitlab.softwareheritage.org/douardda)   |
| Contributions   |   [swh-spdx](https://gitlab.softwareheritage.org/swh/devel/swh-spdx) and [tools-python](https://github.com/spdx/tools-python)  | 
| Documentation   |   [swh-spdx documentation](https://docs.softwareheritage.org/devel/swh-spdx/index.html)  |
| Duration   |   5 May'23 - 28 Aug'23 |

## About SPDX
The [Software Package Data Exchange (SPDX)](https://spdx.dev/) specification defines an open standard for communicating information about software components. SPDX is used to create Software Bill of Material lists (SBOMs), encapsulate licensing and copyright details, and provide package metadata such as version identifiers and known vulnerabilities.

SPDX was originally designed over a decade ago as a way to help developers comply with open-source licenses. Since then it's been extended with new capabilities for describing dependency trees and issuing SBOMs. SPDX was catapulted to global attention in September 2021 when ISO recognized it as the international standard for software supply chain documentation.

## About Software Heritage
[Software Heritage](https://www.softwareheritage.org/) is on a mission to collect, preserve, and share all the publicly available software with its source code and development history. The archive periodically crawls GitHub, GitLab, Debian, PyPI, etc. It has preserved more than 16 billion source code files with 3.4 billion commits spanning more than 256 million software projects.

My GSoC project was all about targeting these projects and developing a tool to generate their SBOMs (Software Bill Of Materials) in SPDX standard making use of SPDX's [tools-python](https://github.com/spdx/tools-python) library.

### OVERVIEW
I developed a Python package named [swh-spdx](https://gitlab.softwareheritage.org/swh/devel/swh-spdx) to assist in the generation of SBOMs for projects stored in the Software Heritage Archive. It utilizes the Software Heritage [GraphQL API](https://archive.softwareheritage.org/graphql/) to extract the source code of projects from different origins. I employed the [gql](https://github.com/graphql-python/gql) module to establish connectivity between the tool and the GraphQL API server of Software Heritage.

-  For Code testing
   - Unit testing -> [Pytest](https://github.com/pytest-dev/pytest) testing framework
   - Code formatting, organization, and style consisting -> [black](https://github.com/psf/black), [isort](https://github.com/PyCQA/isort) and [flake8](https://github.com/PyCQA/flake8)
   - Documentation testing -> [Sphinx](https://github.com/sphinx-doc/sphinx)
   - Automation Server @ Software Heritage -> [Jenkins](https://github.com/jenkinsci)

The tool currently supports projects from two origins that are [PyPi](https://archive.softwareheritage.org/browse/search/?q=&with_visit=true&with_content=true&visit_type=pypi) and [NPM](https://archive.softwareheritage.org/browse/search/?q=&with_visit=true&with_content=true&visit_type=npm) where the tool takes in the [SoftWare Heritage persistent IDentifier(SWHID)](https://docs.softwareheritage.org/devel/swh-model/persistent-identifiers.html) of project and writes the generated SBOM in specified path.

### Contributions
| Title |  Commit |
|:----------:|:--------:|
| Initialize the swh-spdx repo |  [D3857](https://gitlab.softwareheritage.org/swh/devel/swh-spdx/-/commit/3857c3f934f9501d1aaea921c916a1ec1225bad8)  |
| Implement the initial classes, methods, and their unit tests |   [D8213](https://gitlab.softwareheritage.org/swh/devel/swh-spdx/-/commit/8213bf960e82903ce80d1d6a68af297689a273eb)   |
| Add more test coverage | [Dbcd0](https://gitlab.softwareheritage.org/swh/devel/swh-spdx/-/commit/bcd0a2357917e75ad89b050ebca317c55790f0ba) |
| Add type annotations | [De97b](https://gitlab.softwareheritage.org/swh/devel/swh-spdx/-/commit/bcd0a2357917e75ad89b050ebca317c55790f0ba)|
| Add support for swh-model CoreSWHID class | [Db28d](https://gitlab.softwareheritage.org/swh/devel/swh-spdx/-/commit/b28d8b7b7bdc8dcdc8ce8755fdd3787cb33a13f9)|
| Implement initial SPDX generation of PyPI origin projects | [D7ea8](https://gitlab.softwareheritage.org/swh/devel/swh-spdx/-/commit/7ea889fd83d1b395f69b6cccdf0fb9ba19165b4b)|
| Implement initial SPDX generation of NPM origin projects | [D7163](https://gitlab.softwareheritage.org/swh/devel/swh-spdx/-/commit/7163df0986fdb158b5c6023db43040264e3024ef)|





