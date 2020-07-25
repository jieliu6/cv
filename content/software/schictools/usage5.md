---
title: Visualization
linktitle: Visualization
toc: true
type: docs
date: "2019-05-05T00:00:00+01:00"
draft: false
menu:
  schictools:
    parent: Usage
    weight: 5

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 7
---

  ```console
  >>>scatter(data, dimension="2D", point_size=3, sty='default',
  ... label=None, title=None, alpha=None, aes_label=None
  ... )
  >>>plt.show()
  ```

  This function is to plot scatter plot of embedding points of single cell data.
    Scatter plot of either two-dimensions or three-dimensions will be generated.


  - data (numpy.array): A numpy array which has 2 or 3 columns, every row represent a point.

  - dimension (str): Specifiy the dimension of the plot, either "2D" or "3D". Default: "2D".

  - point_size (float): Set the size of the points in scatter plot. Default: 3.

  - sty (str): Styles of Matplotlib. Default: 'default'.

  - label (list or None): specifiy the label of each point. Default: None.

  - title (str): Title of the plot. Default: None.

  - alpha (float): The alpha blending value. Default: None.

  - aes_label (list): Set the label of every axis. Default: None.


"scHiCTools" also support interactive scatter plot which require the module 'plotly'

  ```console
  >>>interactive_scatter(loaded_data, data, out_file, dimension='2D', point_size=3,
  ... label=None, title=None, alpha=1, aes_label=None)
  ```

  This function is to generate an interactive scatter plot of embedded single cell data.
    The plot will be stored in a file.

  - schic (scHiCs): A `scHiCs` object.
  - data (numpy.array): A numpy array which has 2 or 3 columns, every row represent a point.
  - out_file (str): Output file path.
  - dimension (str): Specifiy the dimension of the plot, either "2D" or "3D". The default is "2D".
  - point_size (float): Set the size of the points in scatter plot. The default is 3.
  - label (list or None): Specifiy the label of each point. The default is None.
  - title (str): Title of the plot. The default is None.
  - alpha (float): The alpha blending value. The default is 1.
  - aes_label (list): Set the label of every axis. The default is None.



