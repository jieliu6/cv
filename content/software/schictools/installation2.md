---
title: Installation
linktitle: Installation
toc: true
type: docs
date: "2019-05-05T00:00:00+01:00"
draft: false
menu:
  schictools:
    parent: Getting Ready
    weight: 2

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 3
---

## Install from GitHub

  You can install the package with following command:

  ```console
    $ git clone https://github.com/liu-bioinfo-lab/scHiCTools.git
    $ cd scHiCTools
    $ python setup.py install
  ```

## Install from PyPI

  ```console
    $ pip install scHiCTools
  ```

## Install optional interactive dependencie
  
  ```console
    $ pip install scHiCTools[interactive_scatter]
  ```
  or
  ```console
    $ pip install -e .[interactive_scatter]
  ```