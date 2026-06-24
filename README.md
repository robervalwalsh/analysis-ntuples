# analysis-ntuples
Repository for the lists of ntuples and information contained therein used in the ntuple productions and analyses.

## Usage
Clone this repository in your working area
(usually in your Analysis/Tools or Analysis/Ntuplizer projects)

```bash
git clone https://github.com/desy-cms/analysis-ntuples.git data/ntuples
cd data/ntuples
```

## Obtaining Trigger Info

You must create a working area and install the `Analysis/Ntuplizer` package (https://github.com/desy-cms/analysis-ntuplizer) to be able to run the scripts described in this section.

1. Go to CMS OMS Run summary page: https://cmsoms.cern.ch/cms/runs/summary and add the range of runs for the era you are interested in. Verify that the `HLT Key` column is present in the table. If not, click on `Table Configuration` and select it from the list of available columns.
2. Click on the download icon that opens the `Export CSV` window. Click on `Load all Rows` and then on `Export Current Table.
3. Run the script<br>
`get_hlt_python_configs.py --run_summary <path_to_the_run_summary_csv_file> --filter_hlt_key <hlt_key_string>`<br>
The script will download the HLT menu config files for the runs in the range you specified and create a directory `hlt_configs` with the downloaded files. The `--filter_hlt_key` option is a string that filters the HLT keys you are interested in, e.g. `/cdaq/physics/Run2026/2e34`. This will take a while until all the menus are downloaded.
4. Prepare a txt file containing a list of the HLT paths, without the version number, e.g., `HLT_ZeroBias_v`, that you are interested in getting the trigger objects information.
5. Once you have the HLT menus python configuration files and the list of HLT paths, you can run the script<br>
`trigger_info_from_menu_config.py --hlt_paths <path_to_the_hlt_paths_txt_file> --configs <path_to_the_hlt_configs_directory> --output <path_to_the_output_yaml_file>`<br>
The output yaml file will contain the trigger paths and trigger objects information for the HLT paths you specified in the txt file considreing all the HLT menus you downloaded.

N.B.: the `hlt_configs` directory can be quite large, so do not commit it to the repository. Only your list of paths and the output yaml file should be committed.


## Recommended ntuples for MSSM Hbb analyses

