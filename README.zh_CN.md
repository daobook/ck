# Collective Knowledge framework (CK)

[![PyPI version](https://badge.fury.io/py/ck.svg)](https://badge.fury.io/py/ck)
[![Downloads](https://pepy.tech/badge/ck)](https://pepy.tech/project/ck)
[![Python Version](https://img.shields.io/badge/python-2.7%20|%203.4+-blue.svg)](https://pypi.org/project/ck)

[![Build Status](https://travis-ci.com/ctuning/ck.svg?branch=master)](https://travis-ci.com/ctuning/ck)
[![Windows Build status](https://ci.appveyor.com/api/projects/status/iw2k4eajy54xrvqc?svg=true)](https://ci.appveyor.com/project/gfursin/ck)
[![Coverage Status](https://coveralls.io/repos/github/ctuning/ck/badge.svg)](https://coveralls.io/github/ctuning/ck)

[![Documentation Status](https://readthedocs.org/projects/ck/badge/?version=latest)](https://ck.readthedocs.io/en/latest/?badge=latest)
[![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1Fp6uxCqTazmCSSl8v-nY93VVmcOoLiXi?usp=sharing)
[![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1a761nKgoHlJAy6gOXh-c9H4WkLV8nzRU?usp=sharing)


## 动机

随着机器学习在日常生活中变得越来越重要，设计高效的机器学习系统并在现实世界中部署它们正变得越来越具有挑战性、耗时和昂贵。研究人员和工程师必须跟上快速发展的软件堆栈和从云到边缘的硬件平台的寒武纪大爆发的步伐。这些平台都有自己的特定库、框架、API 和规范，通常需要对整个模型/软件/硬件堆栈进行重复、繁琐和特别的优化，以根据用户需求和限制来权衡准确性、延迟、整体、功耗、规模和成本。

### CK 框架

**集体知识框架** （Collective Knowledge framework，简称 CK）试图开发一个共同 plug&play 基础设施，可以通过类似维基百科学习如何解决上述挑战，让它更容易合作设计、基准、在现实世界中优化和部署的机器学习系统在不断发展的软件、硬件和数据集（请参阅 [ACM TechTalk](https://www.youtube.com/watch?v=7zpeIVwICa4) 获取更多细节）：

* CK 的目标是提供一个简单的游乐场，以减少对软件的依赖，帮助研究人员和业界人士分享他们的知识以可重用自动化菜谱的形式，带有统一的 Python API、CLI 和元描述：
  - [稳定的 CK 自动化配方](https://github.com/mlcommons/ck/tree/master/ck/repo/module)
  - [MLPerf&trade; 基准测试自动化食谱](https://github.com/mlcommons/ck/tree/master/ck-mlops/repo/module)

* CK 帮助组织软件项目，并将 Git 仓库作为上述自动化方法的数据库以及基于 [FAIR 原则](https://www.nature.com/articles/sdata201618) 的相关工件
如我们的 [期刊文章](https://arxiv.org/pdf/2011.01149.pdf) 所述 [较短的预印本](https://arxiv.org/abs/2006.07161)。
查看 CK 兼容的 GitHub 库示例：
  - [MLPerf/MLOps automation](https://github.com/mlcommons/ck-mlops)
  - [ACM REQUEST tournament for collaborative and reproducible ML/SW/HW co-design](https://github.com/ctuning/ck-request)

### Community developments

We collaborated with the community to reproduce [150+ ML and Systems papers](https://cTuning.org/ae)
and implement the following reusable automation recipes in the CK format: 

* Portable meta package manager to automatically detect, install or rebuild various ML artifacts 
  (ML models, data sets, frameworks, libraries, etc) across different platform and operating systems including Linux, Windows, MacOS and Android:
  - [ML artifact detection plugins](https://github.com/mlcommons/ck-mlops/tree/main/soft)
  - [ML meta package installation plugins](https://github.com/mlcommons/ck-mlops/tree/main/package)
  - OS descriptions: [Linux/MacOS/Android](https://github.com/mlcommons/ck-mlops/tree/main/os) ; [Windows](https://github.com/ctuning/ck-win/tree/main/os) 

* Portable manager for Python virtual environments: [CK repo](https://github.com/mlcommons/ck-venv).

* Portable workflows to support collaborative, reproducible and cross-platform benchmarking:
  - [ML Systems benchmarking](https://github.com/mlcommons/ck-mlops/tree/main/program)
  - [Compiler benchmarking](https://github.com/ctuning/ctuning-programs/tree/master/program)

* Portable workflows to automate MLPerf&trade; benchmark:
  - [End-to-end submission suite used by multiple organizations to automate the submission of MLPerf inference benchmark](https://github.com/mlcommons/ck/blob/master/docs/mlperf-automation/README.md)
    - MLperf inference v1.1 results: [MLCommons press-release](https://mlcommons.org/en/news/mlperf-inference-v11), 
      [Datacenter results](https://mlcommons.org/en/inference-datacenter-11), 
      [Edge results](https://mlcommons.org/en/inference-edge-11)
  - [Reproducibility studies for MLPerf inference benchmark v1.1 automated by CK](https://github.com/mlcommons/ck/tree/master/docs/mlperf-automation/reproduce#reproducibility-reports-mlperf-inference-benchmark-v11)
  - [Design space exploration of ML/SW/HW stacks and customizable visualization](https://cknowledge.io/result/crowd-benchmarking-mlperf-inference-classification-mobilenets-all)


Please contact [Grigori Fursin](https://www.linkedin.com/in/grigorifursin) if you are interested to join this community effort!

### Tutorials

* [CK automations for unified benchmarking]( https://colab.research.google.com/drive/1a761nKgoHlJAy6gOXh-c9H4WkLV8nzRU?usp=sharing )
* [CK-based MLPerf inference benchmark automation example]( https://colab.research.google.com/drive/1Fp6uxCqTazmCSSl8v-nY93VVmcOoLiXi?usp=sharing )
  * [CK-based MLPerf inference vision benchmark v1.1 automation (TVM)]( https://colab.research.google.com/drive/1aywGlyD1ZRDtQTrQARVgL1882JcvmFK-?usp=sharing )
  * [CK-based MLPerf inference vision benchmark v1.1 automation (ONNX)]( https://colab.research.google.com/drive/1ij1rWoqje5-Sn6UsdFj1OzYakudI2RIS?usp=sharing )
* [CK basics]( https://colab.research.google.com/drive/15lQgxuTSkEPqi4plaat1_v2gJcfIrATF?usp=sharing )

## Releases

### Stable versions

The latest version of the CK automation suite supported by MLCommons&trade;:
* [CK framework v2.6.1 (Apache 2.0 license)](https://github.com/mlcommons/ck/releases/tag/V2.6.1)
* [CK automation suite for MLPerf&trade; and ML/SW/HW co-design](https://github.com/mlcommons/ck-mlops)

### Development versions

We plan to develop a new version of the CK framework (v3) 
within the MLCommons' Design Space Exploration workgroup -
please contact [Grigori Fursin](mailto:grigori@octoml.ai) to join this community effort!


## Current projects
* [Automating MLPerf(tm) inference benchmark and packing ML models, data sets and frameworks as CK components with a unified API and meta description](https://github.com/mlcommons/ck/blob/master/docs/mlperf-automation/README.md)
* Developing customizable dashboards for MLPerf&trade; to help end-users select ML/SW/HW stacks on a Pareto frontier: [aggregated MLPerf&trade; results]( https://cknowledge.io/?q="mlperf-inference-all" )
* Providing a common format to share artifacts at ML, systems and other conferences: [video](https://youtu.be/DIkZxraTmGM), [Artifact Evaluation](https://cTuning.org/ae)
* Redesigning CK together with the community based on user feedback: [incubator](https://github.com/mlcommons/ck/tree/master/incubator)
* [Other real-world use cases](https://cKnowledge.org/partners.html) from MLPerf&trade;, Qualcomm, Arm, General Motors, IBM, the Raspberry Pi foundation, ACM and other great partners;

## Documentation

* [Online CK documentation]( https://ck.readthedocs.io ) 
  * [Why CK?]( https://ck.readthedocs.io/en/latest/src/introduction.html ) 
  * [CK Basics](https://michel-steuwer.github.io/About-CK)
  * [Try CK]( https://ck.readthedocs.io/en/latest/src/first-steps.html )
* [Publications](https://github.com/mlcommons/ck/wiki/Publications)

## Installation

Follow [this guide](https://ck.readthedocs.io/en/latest/src/installation.html) 
to install CK framework on your platform.

CK supports the following platforms:

|               | As a host platform | As a target platform |
|---------------|:------------------:|:--------------------:|
| Generic Linux | ✓ | ✓ |
| Linux (Arm)   | ✓ | ✓ |
| Raspberry Pi  | ✓ | ✓ |
| MacOS         | ✓ | ± |
| Windows       | ✓ | ✓ |
| Android       | ± | ✓ |
| iOS           | TBD | TBD |
| Bare-metal (edge devices)   | - | ± |

## Examples

### Portable CK workflow (native environment without Docker)

Here we show how to pull a GitHub repo in the CK format 
and use a unified CK interface to compile and run 
any program (image corner detection in our case)
with any compatible data set on any compatible platform:

```bash
python3 -m pip install ck

ck pull repo:mlcommons@ck-mlops

ck ls program:*susan*

ck search dataset --tags=jpeg

ck pull repo:ctuning-datasets-min

ck search dataset --tags=jpeg

ck detect soft:compiler.gcc
ck detect soft:compiler.llvm

ck show env --tags=compiler

ck compile program:image-corner-detection --speed

ck run program:image-corner-detection --repeat=1 --env.MY_ENV=123 --env.TEST=xyz
```

You can check output of this program in the following directory:
```bash
cd `ck find program:image-corner-detection`/tmp
ls

processed-image.pgm
```

You can now view this image with detected corners.


Check [CK docs](https://ck.readthedocs.io/en/latest/src/introduction.html) for further details.

### MLPerf&trade; benchmark workflows

* [Current coverage](https://github.com/mlcommons/ck/tree/master/docs/mlperf-automation#readme)
* [MLPerf inference v1.1 workflows](https://github.com/mlcommons/ck/blob/master/docs/mlperf-automation/reproduce/README.md#reproducibility-reports-mlperf-inference-benchmark-v11)

### Portable CK workflows inside containers

We have prepared adaptive CK containers to demonstrate MLOps capabilities:
* https://github.com/mlcommons/ck-mlops/tree/main/docker

You can run them as follows:

```bash
ck pull repo:mlcommons@ck-mlops
ck build docker:ck-template-mlperf --tag=ubuntu-20.04
ck run docker:ck-template-mlperf --tag=ubuntu-20.04
```

### Portable workflow example with virtual CK environments

You can create multiple [virtual CK environments](https://github.com/mlcommons/ck-venv) with templates
to automatically install different CK packages and workflows, for example for MLPerf&trade; inference:

```
ck pull repo:mlcommons@ck-venv
ck create venv:test --template=mlperf-inference-main
ck ls venv
ck activate venv:test

ck pull repo:mlcommons@ck-mlops
ck install package --ask --tags=dataset,coco,val,2017,full
ck show env

```

### Integration with web services and CI platforms

All CK modules, automation actions and workflows are accessible as a micro-service with a unified JSON I/O API
to make it easier to integrate them with web services and CI platforms as described 
[here](https://github.com/mlcommons/ck/blob/master/docs/mlperf-automation/tools/continuous-integration.md).




### Other use cases

* [List of various use cases]( https://ck.readthedocs.io/en/latest/src/introduction.html#ck-showroom )







## CK portal 

We have developed the [cKnowledge.io portal](https://cKnowledge.io) to help the community
organize and find all the CK workflows and components similar to PyPI:

* [Search CK components](https://cKnowledge.io)
* [Browse CK components](https://cKnowledge.io/browse)
* [Find reproduced results from papers]( https://cKnowledge.io/reproduced-results )
* [Test CK workflows to benchmark and optimize ML Systems]( https://cKnowledge.io/demo )



## Containers to test CK automation recipes and workflows

The community provides Docker containers to test CK and components using different ML/SW/HW stacks (DSE).

* A set of Docker containers to test the basic CK functionality
  using some MLPerf inference benchmark workflows: 
  https://github.com/mlcommons/ck-mlops/tree/main/docker/test-ck


## Contributions

Users can extend the CK functionality via [CK modules](https://github.com/mlcommons/ck/tree/master/ck/repo/module) 
or external [GitHub reposities](https://cKnowledge.io/repos) in the CK format
as described [here](https://ck.readthedocs.io/en/latest/src/typical-usage.html).

Please check [this documentation](https://ck.readthedocs.io/en/latest/src/how-to-contribute.html)
if you want to extend the CK core functionality and [modules](https://github.com/mlcommons/ck/tree/master/ck/repo/module). 

Note, that we plan to [redesign the CK framework](https://github.com/mlcommons/ck/projects/1) 
to be more pythonic (we wrote the first prototype without OO to be able 
to port it to bare-metal devices in C but eventually we decided to drop this idea).

Please contact [Grigori Fursin](mailto:grigori@octoml.ai) to join this community effort.



## Author and coordinator

* [Grigori Fursin](https://fursin.net) (OctoML/MLCommons/cTuning foundation)

## Acknowledgments

We would like to thank all [contributors](https://github.com/mlcommons/ck/blob/master/CONTRIBUTING.md) 
and [collaborators](https://cKnowledge.org/partners.html) for their support, fruitful discussions, 
and useful feedback! See more acknowledgments in the [CK journal article](https://arxiv.org/abs/2011.01149).
