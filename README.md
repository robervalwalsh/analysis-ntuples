# analysis-ntuples
Repository for the lists of ntuples and information contained therein used in the analyses.

## Usage
Clone this repository in your working area
(usually in your Analysis/Tools or Analysis/Ntuplizer projects)

```bash
git clone https://github.com/desy-cms/analysis-ntuples.git data/ntuples
cd data/ntuples
```

In the **analysis-specific** directory tree there is a README.md
with information about the available datasets and two directories,
namely *data* and *mc*, inside which one can find the rootFileList.txt
files for each dataset plus additional info about the ntuple production.

## Obtaining Trigger Info

Assuming you created a working area and installed the `Analysis/Ntuplizer`

1. Copy the HLT menu config file (obtained using `hltGetConfiguration`) to `$CMSSW_BASE/src/Analysis/Ntuplizer/python`
2. Go to your `$CMSSW_BASE/src/Analysis/Ntuplizer/data/ntuples/<year>/<version>` directory
3. Add the trigger paths you want to be included in the ntuples to the `hlt_paths.txt` file. Create the file if it does not exist.
4. Run the script `trigger_info_from_menu_config.py`. When prompt, enter the name of the config file (step 2 above). It will create a yaml file with the same basename of the config file containing HLT paths and trigger objects.
5. Merge the resulting yaml file from step 3 to `trigger_info.yml`. If `trigger_info.yml` does not exist, create it.
6. Commit the changes of `$CMSSW_BASE/src/Analysis/Ntuplizer/data/ntuples` to the repository and make a PR. The changes will be used by the `Analysis/Tools` once the ntuples are ready.



## Recommended ntuples for MSSM Hbb analyses

* RunII Legacy 2018 analysis: [2018/v5](2018/v5)
  * [trigger information](2018/v5/trigger_info.yml)
  * [datasets for data](2018/v5/data/datasets.yml)
  * [datasets for monte carlo](2018/v5/mc/datasets.yml)
* RunII Legacy 2017 analysis: [2017/v5](2017/v5)
  * [trigger information](2017/v5/trigger_info.yml)
  * [datasets for data](2017/v5/data/datasets.yml)
  * [datasets for monte carlo](2017/v5/mc/datasets.yml)
* RunII re-reco 2018 analysis: [2018/v3](2018/v3)
* RunII re-reco 2017 analysis: [2017/v4](2017/v4)

:warning: the versioning labels mssmhbb-2017-v4 and mssmhbb-2018-v3 are deprecated and will be removed in the future


