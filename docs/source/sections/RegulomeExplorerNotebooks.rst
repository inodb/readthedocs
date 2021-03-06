**********************
Statistical Notebooks
**********************
Integrated statistical analysis and exploration of multiple genomic and clinical data types provides researchers with a great possibility to expand our current knowledge of cancer. ISB-CGC offers a great source of diverse data types including gene expression, somatic mutations, clinical data, etc. We have developed a series of notebooks that use BigQuery to compute the statistical associations between different combinations of the data types available in ISB-CGC.

The statistical significance of each pairwise association is assessed using rank-ordered data and a statistical test appropriate to each data type pair, which are categorized as categorical or numerical. The following table lists the statistical methods implemented in the notebooks, and the data types used as examples. The Regulome Explorer inspired notebook is a special notebook that allows computation of associations between all possible data types available in the TCGA dataset; more details are below.

.. list-table:: 
   :widths: 25 25 50
   :align: center
   :header-rows: 1
  
   * - Data type 
     - Data type
     - Statistical test/notebook
   * - Gene expression
     - Clinical
     - `Kruskal-Wallis score <https://nbviewer.jupyter.org/github/isb-cgc/Community-Notebooks/blob/master/RegulomeExplorer/BigQuery-KruskalWallis.ipynb>`_
   * - Gene expression
     - Somatic mutation
     - `T-test score <https://nbviewer.jupyter.org/github/isb-cgc/Community-Notebooks/blob/master/RegulomeExplorer/BigQuery-StudentTest.ipynb>`_   
   * - Gene expression
     - Gene expression
     - `Spearman Correlation <https://nbviewer.jupyter.org/github/isb-cgc/Community-Notebooks/blob/master/RegulomeExplorer/BigQuery-SpearmanCorrelation.ipynb>`__
   * - Somatic mutation
     - Clinical
     - `Chi Square test <https://nbviewer.jupyter.org/github/isb-cgc/Community-Notebooks/blob/master/RegulomeExplorer/BigQuery-Chisquare.ipynb>`_
   * - Somatic mutation
     - Somatic Mutation
     - `Fisher’s exact test <https://nbviewer.jupyter.org/github/isb-cgc/Community-Notebooks/blob/master/RegulomeExplorer/BigQuery-FisherExact.ipynb>`_
   * - All types
     - All types
     - `Regulome Explorer inspired notebook <https://nbviewer.jupyter.org/github/isb-cgc/Community-Notebooks/blob/master/RegulomeExplorer/RegulomeExplorer-notebook.ipynb>`_


Regulome Explorer Inspired Notebook
===================================
`Regulome Explorer <http://explorer.cancerregulome.org/>`_ is a well-established web tool for the exploration and visualization of associations between clinical and molecular features of TCGA data. Regulome Explorer was developed in 2012 in close collaboration between the Institute for Systems Biology and the MD Anderson Cancer Center Regulome, and enables users to search and visualize precomputed statistical data filtered according to user-specified parameters. Although Regulome Explorer's broad functionality and high-quality graphics make it a valuable tool for exploring and visualizing 20 of the 33 TCGA data sets, it does not yet contain analysis of recent releases of TCGA and cannot be easily applied to data sets other than TCGA. 

We developed a more flexible version, replicating capabilities of Regulome Explorer, as a Python notebook that uses Google Cloud resources. Rather than working with precomputed, fixed cohorts and fixed results, statistical analyses are dynamically performed in the cloud, with user defined patient cohorts. Moreover, the notebook can be extended so that users can analyze additional data sets available as part of the 'ISB-CGC BigQuery ecosystem' such as TCGA, TARGET,  CCLE, COSMIC, and others. The notebook can be accessed in `Regulome Explorer inspired notebook <https://nbviewer.jupyter.org/github/isb-cgc/Community-Notebooks/blob/master/RegulomeExplorer/RegulomeExplorer-notebook.ipynb>`_.

