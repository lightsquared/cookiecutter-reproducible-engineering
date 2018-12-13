Reproducible Engineering
========================

A boilerplate for reproducible and transparent engineering with close resemblances to the philosophy of [Cookiecutter Data Science](https://github.com/mkrapp/cookiecutter-reproducible-science): *A logical, reasonably standardized, but flexible project structure for doing and sharing science work.*

Requirements
------------
Install `cookiecutter` command line: `pip install cookiecutter`    

Usage
-----
To start a new science project:

`cookiecutter gh:mkrapp/cookiecutter-reproducible-engineering`

Project Structure
-----------------

```
.
├── AUTHORS.md
├── LICENSE
├── README.md
├── 0_research              <- Documentation, e.g., doxygen or scientific papers (not tracked by git)
├── 1_planning              <- Configuration files for testing
    ├── instrumentation     <- Configuration files for instrumentation
    ├── test plans          <- test plans for analytical data
    ├── doxygen             <- Configuration file for doxgen
    └── models              <- Configuration files for software models
├── 2_data
│   ├── test_1              <- Data from test 1.
│       ├── external        <- Data from third party sources.
│       ├── interim         <- Intermediate data that has been transformed.
│       ├── processed       <- The final, canonical data sets for modeling.
│       └── raw             <- The original, immutable data dump.
│   └── test_2...           <- Data from test 2.
├── 3_media
│   ├── photographs         <- Photographs of the test setup and results
│   └── video               <- Video of tests
└── 4_analysis              <- Analysis for this project
│   ├── test_1              <- Analysis of test data 1
│       ├── notebooks       <- Jupyter or R notebooks
│       ├── external        <- Any external source code, e.g., pull other git projects, or external libraries
│       ├── models          <- Source code for your own model
│       ├── tools           <- Any helper scripts go here
│       └── visualization   <- Scripts for visualization of your results, e.g., matplotlib, ggplot2 related.
│   └── test_2...
├── 5_reports               <- For a manuscript source, e.g., LaTeX, Markdown, etc., or any project reports
│   ├── bibliography        <- Bibliography file, e.g., bibtex, Mendeley, Papers.
│   └── figures             <- Figures for the manuscript or reports
└── 6_presentations         <- For a presentation source, e.g., Jupyter notebook, Keynote, etc., or any project presentations
```

File Naming Conventions

Each project should have a readme.txt file that contains the file naming convention, and acronyms used in the file name.  General guidelines are,

YYYY-MM-DD_location_test-01_instrument_what-is-measured_condition

1. Underlines _ are used to separate metadata.
2. Dashes are used to separate words so your eyes don't fall out and roll away.
3. Use all lower case.
3. No spaces or punctuation in the file name.
3. YYYY-MM-DD this is the date the data was collected.
4. location: Corkern Range (cr), McKinley Range (mr), Capano Range (cr), NCETR Lab (nl)
4. test_01 is the test number on that date.  This should be sequential.  Pad with zeros.  This can also be shot_01.
5. instrument is the general instrument that was used to collect the data.  High Speed Camera (hsc), Pencil Probe (pp), Gas Chromatography Mass spectrometry (gcms), Thermocouple (t), Sensitivity Friction (sf), Sensitivity Impact (si), Sensitivity Static (ss), Thermal Gravometric Analysis (tga), Bomb Calorimeter (bc), Differential Scanning Calorimetry (dsc), thermocouple (t), VOD Probe Rod (vpr), VOD Fiber Optic (vfo).
6. List what was measured.  temperature (t), pressure (p), weight (wt), impulse (i), electrical energy (ee), internal energy (u), enthalpy (h)
7. condition defines whether the data is raw (r), processed (p), or final (f).

Example 1:  Several ammonium nitrate and aluminum samples are tested in a bomb calorimeter.  The test took place on Jan 2, 2018, at one of the NCETR labs.  A good file name for the data would be:  2018-01-02_nl_test-03_bc_u_r.csv  This translates to date, NCETR Lab, Test-03 that day, instrument was a bomb calorimeter, you measured internal energy, and this is the raw data file.

Example 2: Several smokeless powder samples are shot on McKinley Bravo Range to measure overpressure using pencil probes.  The test took place on July 4, 1776.  A good file name for this would be:  1776-07-04_mr-b_shot-2_pp_p_r.csv
This translates to date, McKinley Bravo, shot 2 that day, using a pencil probe to measure pressure and the data is raw.

Example 3:  Photographs are taken during the test from example 2 both pre and post blast.  A good name for these would be:  1776-07-04_mr-b_shot-2_preblast_001.jpg
The difference between example 2 and 3 file names is the removal of the measurement meta data and the addition of a photograph description and sequence number.

License
-------
This project is licensed under the terms of the [BSD License](/LICENSE)
