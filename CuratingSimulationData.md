Questions for simulation data (netCDF files and/or code) depositors:

Researcher deposits netCDF files.
- Questions for researcher:
    - Is this raw output?
    - Is this processed output?
        - What code was used to process this data?
    - What model (GITM, CMIP, HYCOM, MITgcm, etc.) was used to generate this data?
        - Get model version, URL, etc
    - Is this based on observational data?
        - Yes – get that input data as well
        - No – done.
    - What is the goal of this deposit:
        - Journal requirement – is the expectation reproducibility?
            - Yes – get system configuration information, input parameters/data
            - No – what are their expectations?
        - Make raw data available for re-analysis
        - Reproducibility
- Data deposit organization:
    - Model
       - [model code]
    - Pre_processing
        - [data]
        - [scripts]
        - Metadata.txt
    - Manuscript_related
        - [data]
        - [scripts]
        - Metadata.txt
    - Post_processing
        - [data]
        - [scripts]
        - Metadata.txt
    - Readme_all.txt
- Preservation needs?
    - File format transformation not needed for netCDF files
- How long to keep the data?
    - EarthCube workshop rubric - https://modeldatarcn.github.io/

