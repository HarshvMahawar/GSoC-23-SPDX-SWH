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

