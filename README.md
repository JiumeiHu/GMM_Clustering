This repository contains the Python scripts and example datasets used for processing and analyzing multiplex fluorescence-coding ddPCR data in the FluoMag-dCoDe platform.

The analysis pipeline implements Gaussian Mixture Model (GMM)–based clustering, outlier detection, and Poisson-based concentration calculation to enable the simultaneous quantification of multiple mRNA and protein targets from two-color ddPCR data.

Overview
The FluoMag-dCoDe data analysis workflow consists of the following key steps:
1.	Input of raw ddPCR droplet fluorescence data, which consists of two-dimensional fluorescence amplitudes (FAM and HEX) exported from Bio-Rad QuantaSoft software.
2.	Definition of fluorescence-coded cluster locations, where the cluster representing each target are predefined using pooled synthetic fluorescence-coded DNA templates (for mRNA targets) and standard-curve measurements (for protein targets).
3.	GMM-based clustering. A Gaussian Mixture Model is applied to identify target-specific clusters, negative droplets, and outliers.
4.	Assignment of sample droplets. Droplets from biological samples are mapped onto the predefined fluorescence code space.
5.	Positive droplets within each target-specific cluster are counted to calculate the target concentrations via Poisson statistics.
