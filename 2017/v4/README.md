# Ntuples Lists for the MSSM Hbb analyses

* [Configuration](#configuration)
* [DATA](#data)
   * [BTagCSV](#btagcsv)
   * [DoubleMuon](#doublemuon)
   * [JetHT](#jetht)
   * [SingleMuon](#singlemuon)
* [MC](#mc)
   * [QCD-bEnriched](#qcd-benriched)
   * [QCD-BGenFilter](#qcd-bgenfilter)
   * [QCD-MuEnrichedPt5](#qcd-muenrichedpt5)
   * [QCD](#qcd)
   * [SUSYGluGluToBBHToBB](#susygluglutobbhtobb)


## Configuration

* Ntuplizer release: [94X_2017_rereco31Mar18_fall17-v4](https://github.com/desy-cms/analysis-ntuplizer/tree/94X_2017_rereco31Mar18_fall17-v4)
* See also configurations:
   * [data](https://github.com/desy-cms/analysis-ntuplizer/blob/94X_2017_rereco31Mar18_fall17-v4/test/ntuplizer_92X_data_2017-v4.py)
   * [mc](https://github.com/desy-cms/analysis-ntuplizer/blob/94X_2017_rereco31Mar18_fall17-v4/test/ntuplizer_94X_mc_2017_fall17-v4.py)

* b-jet energy regression (from nanoAOD) ([Installation](https://twiki.cern.ch/twiki/bin/view/CMSPublic/WorkBookNanoAOD?rev=43))
* DeepFlavour b-tag: ([Installation](https://twiki.cern.ch/twiki/bin/view/CMS/DeepJet?rev=18))

* CMSSW Release: CMSSW_9_4_12
* GlobalTag:
   * Data: 94X_dataRun2_v11
   * Monte Carlo: 94X_mc2017_realistic_v17
* JEC reapplied!!! (see [Recommended jet energy corrections and uncertainties](https://twiki.cern.ch/twiki/bin/view/CMS/JECDataMC?rev=145))

* Filters:
   * Primary vertex filter: <literal>cut = cms.string("!isFake && ndof > 4 && abs(z) <= 24 && position.Rho <= 2")</literal>
   * Data-only:
      * JSON: **NO** lumi mask used.
      * Trigger filters - **OR** of several triggers (see [MssmHbbTriggerResultsFilter_cfi.py](https://github.com/desy-cms/analysis-ntuplizer/blob/94X_2017_rereco31Mar18_fall17-v4/python/run2017/v4/MssmHbbTriggerResultsFilter_cfi.py))



## DATA

### BTagCSV

| rootFileList | Adidtional Info | Comments|
| --------     | --------        | -------- |
| [BTagCSV_Run2017C_rootFileList.txt](data/BTagCSV_Run2017C_rootFileList.txt) |  [processedLumis.json](data/additional_info/BTagCSV_Run2017C_processedLumis.json) <br /> |  | 
| [BTagCSV_Run2017D_rootFileList.txt](data/BTagCSV_Run2017D_rootFileList.txt) |  [processedLumis.json](data/additional_info/BTagCSV_Run2017D_processedLumis.json) <br /> |  | 
| [BTagCSV_Run2017E_rootFileList.txt](data/BTagCSV_Run2017E_rootFileList.txt) |  [processedLumis.json](data/additional_info/BTagCSV_Run2017E_processedLumis.json) <br /> |  | 
| [BTagCSV_Run2017F_rootFileList.txt](data/BTagCSV_Run2017F_rootFileList.txt) |  [processedLumis.json](data/additional_info/BTagCSV_Run2017F_processedLumis.json) <br /> |  | 

### DoubleMuon

| rootFileList | Adidtional Info | Comments|
| --------     | --------        | -------- |
| [DoubleMuon_Run2017C_rootFileList.txt](data/DoubleMuon_Run2017C_rootFileList.txt) |  [processedLumis.json](data/additional_info/DoubleMuon_Run2017C_processedLumis.json) <br /> |  | 
| [DoubleMuon_Run2017D_rootFileList.txt](data/DoubleMuon_Run2017D_rootFileList.txt) |  [processedLumis.json](data/additional_info/DoubleMuon_Run2017D_processedLumis.json) <br /> |  | 
| [DoubleMuon_Run2017E_rootFileList.txt](data/DoubleMuon_Run2017E_rootFileList.txt) |  [processedLumis.json](data/additional_info/DoubleMuon_Run2017E_processedLumis.json) <br /> |  | 
| [DoubleMuon_Run2017F_rootFileList.txt](data/DoubleMuon_Run2017F_rootFileList.txt) |  | :x: **Missing processedLumis.json!?**<br />:warning: **Not all data processed!!!** <br /> | 

### JetHT

| rootFileList | Adidtional Info | Comments|
| --------     | --------        | -------- |
| [JetHT_Run2017C_rootFileList.txt](data/JetHT_Run2017C_rootFileList.txt) |  [processedLumis.json](data/additional_info/JetHT_Run2017C_processedLumis.json) <br /> |  | 
| [JetHT_Run2017D_rootFileList.txt](data/JetHT_Run2017D_rootFileList.txt) |  [processedLumis.json](data/additional_info/JetHT_Run2017D_processedLumis.json) <br /> |  | 
| [JetHT_Run2017E_rootFileList.txt](data/JetHT_Run2017E_rootFileList.txt) |  [processedLumis.json](data/additional_info/JetHT_Run2017E_processedLumis.json) <br /> |  | 
| [JetHT_Run2017F_rootFileList.txt](data/JetHT_Run2017F_rootFileList.txt) |  [processedLumis.json](data/additional_info/JetHT_Run2017F_processedLumis.json) <br /> |  | 

### SingleMuon

| rootFileList | Adidtional Info | Comments|
| --------     | --------        | -------- |
| [SingleMuon_Run2017C_rootFileList.txt](data/SingleMuon_Run2017C_rootFileList.txt) |  [processedLumis.json](data/additional_info/SingleMuon_Run2017C_processedLumis.json) <br /> |  | 
| [SingleMuon_Run2017D_rootFileList.txt](data/SingleMuon_Run2017D_rootFileList.txt) |  [processedLumis.json](data/additional_info/SingleMuon_Run2017D_processedLumis.json) <br /> |  | 
| [SingleMuon_Run2017E_rootFileList.txt](data/SingleMuon_Run2017E_rootFileList.txt) |  [processedLumis.json](data/additional_info/SingleMuon_Run2017E_processedLumis.json) <br /> |  | 
| [SingleMuon_Run2017F_rootFileList.txt](data/SingleMuon_Run2017F_rootFileList.txt) |  [processedLumis.json](data/additional_info/SingleMuon_Run2017F_processedLumis.json) <br /> |  | 


## MC

### QCD-bEnriched

| rootFileList | Adidtional Info | Comments|
| --------     | --------        | -------- |
| [QCD-bEnriched_HT1000to1500_ext1_rootFileList.txt](mc/QCD-bEnriched_HT1000to1500_ext1_rootFileList.txt) |  |  | 
| [QCD-bEnriched_HT1000to1500_ext2_rootFileList.txt](mc/QCD-bEnriched_HT1000to1500_ext2_rootFileList.txt) |  |  | 
| [QCD-bEnriched_HT1000to1500_rootFileList.txt](mc/QCD-bEnriched_HT1000to1500_rootFileList.txt) |  |  | 
| [QCD-bEnriched_HT100to200_rootFileList.txt](mc/QCD-bEnriched_HT100to200_rootFileList.txt) |  |  | 
| [QCD-bEnriched_HT1500to2000_ext1_rootFileList.txt](mc/QCD-bEnriched_HT1500to2000_ext1_rootFileList.txt) |  |  | 
| [QCD-bEnriched_HT1500to2000_ext2_rootFileList.txt](mc/QCD-bEnriched_HT1500to2000_ext2_rootFileList.txt) |  |  | 
| [QCD-bEnriched_HT1500to2000_rootFileList.txt](mc/QCD-bEnriched_HT1500to2000_rootFileList.txt) |  |  | 
| [QCD-bEnriched_HT2000toInf_ext1_rootFileList.txt](mc/QCD-bEnriched_HT2000toInf_ext1_rootFileList.txt) |  |  | 
| [QCD-bEnriched_HT2000toInf_rootFileList.txt](mc/QCD-bEnriched_HT2000toInf_rootFileList.txt) |  |  | 
| [QCD-bEnriched_HT200to300_ext1_rootFileList.txt](mc/QCD-bEnriched_HT200to300_ext1_rootFileList.txt) |  |  | 
| [QCD-bEnriched_HT200to300_rootFileList.txt](mc/QCD-bEnriched_HT200to300_rootFileList.txt) |  |  | 
| [QCD-bEnriched_HT300to500_ext1_rootFileList.txt](mc/QCD-bEnriched_HT300to500_ext1_rootFileList.txt) |  |  | 
| [QCD-bEnriched_HT300to500_rootFileList.txt](mc/QCD-bEnriched_HT300to500_rootFileList.txt) |  |  | 
| [QCD-bEnriched_HT500to700_ext1_rootFileList.txt](mc/QCD-bEnriched_HT500to700_ext1_rootFileList.txt) |  |  | 
| [QCD-bEnriched_HT500to700_rootFileList.txt](mc/QCD-bEnriched_HT500to700_rootFileList.txt) |  |  | 
| [QCD-bEnriched_HT700to1000_ext1_rootFileList.txt](mc/QCD-bEnriched_HT700to1000_ext1_rootFileList.txt) |  |  | 
| [QCD-bEnriched_HT700to1000_pmx_rootFileList.txt](mc/QCD-bEnriched_HT700to1000_pmx_rootFileList.txt) |  |  | 
| [QCD-bEnriched_HT700to1000_rootFileList.txt](mc/QCD-bEnriched_HT700to1000_rootFileList.txt) |  |  | 

### QCD-BGenFilter

| rootFileList | Adidtional Info | Comments|
| --------     | --------        | -------- |
| [QCD-BGenFilter_HT1000to1500_rootFileList.txt](mc/QCD-BGenFilter_HT1000to1500_rootFileList.txt) |  |  | 
| [QCD-BGenFilter_HT100to200_rootFileList.txt](mc/QCD-BGenFilter_HT100to200_rootFileList.txt) |  |  | 
| [QCD-BGenFilter_HT1500to2000_ext1_rootFileList.txt](mc/QCD-BGenFilter_HT1500to2000_ext1_rootFileList.txt) |  |  | 
| [QCD-BGenFilter_HT1500to2000_rootFileList.txt](mc/QCD-BGenFilter_HT1500to2000_rootFileList.txt) |  |  | 
| [QCD-BGenFilter_HT2000toInf_ext1_rootFileList.txt](mc/QCD-BGenFilter_HT2000toInf_ext1_rootFileList.txt) |  |  | 
| [QCD-BGenFilter_HT2000toInf_rootFileList.txt](mc/QCD-BGenFilter_HT2000toInf_rootFileList.txt) |  |  | 
| [QCD-BGenFilter_HT200to300_rootFileList.txt](mc/QCD-BGenFilter_HT200to300_rootFileList.txt) |  |  | 
| [QCD-BGenFilter_HT300to500_rootFileList.txt](mc/QCD-BGenFilter_HT300to500_rootFileList.txt) |  |  | 
| [QCD-BGenFilter_HT500to700_rootFileList.txt](mc/QCD-BGenFilter_HT500to700_rootFileList.txt) |  |  | 
| [QCD-BGenFilter_HT700to1000_ext1_rootFileList.txt](mc/QCD-BGenFilter_HT700to1000_ext1_rootFileList.txt) |  |  | 
| [QCD-BGenFilter_HT700to1000_ext2_rootFileList.txt](mc/QCD-BGenFilter_HT700to1000_ext2_rootFileList.txt) |  |  | 
| [QCD-BGenFilter_HT700to1000_rootFileList.txt](mc/QCD-BGenFilter_HT700to1000_rootFileList.txt) |  |  | 

### QCD-MuEnrichedPt5

| rootFileList | Adidtional Info | Comments|
| --------     | --------        | -------- |
| [QCD-MuEnrichedPt5_Pt-1000toInf_rootFileList.txt](mc/QCD-MuEnrichedPt5_Pt-1000toInf_rootFileList.txt) |  |  | 
| [QCD-MuEnrichedPt5_Pt-120to170_rootFileList.txt](mc/QCD-MuEnrichedPt5_Pt-120to170_rootFileList.txt) |  |  | 
| [QCD-MuEnrichedPt5_Pt-170to300_rootFileList.txt](mc/QCD-MuEnrichedPt5_Pt-170to300_rootFileList.txt) |  |  | 
| [QCD-MuEnrichedPt5_Pt-300to470_rootFileList.txt](mc/QCD-MuEnrichedPt5_Pt-300to470_rootFileList.txt) |  |  | 
| [QCD-MuEnrichedPt5_Pt-30to50_rootFileList.txt](mc/QCD-MuEnrichedPt5_Pt-30to50_rootFileList.txt) |  |  | 
| [QCD-MuEnrichedPt5_Pt-470to600_rootFileList.txt](mc/QCD-MuEnrichedPt5_Pt-470to600_rootFileList.txt) |  |  | 
| [QCD-MuEnrichedPt5_Pt-50to80_rootFileList.txt](mc/QCD-MuEnrichedPt5_Pt-50to80_rootFileList.txt) |  |  | 
| [QCD-MuEnrichedPt5_Pt-600to800_rootFileList.txt](mc/QCD-MuEnrichedPt5_Pt-600to800_rootFileList.txt) |  |  | 
| [QCD-MuEnrichedPt5_Pt-800to1000_rootFileList.txt](mc/QCD-MuEnrichedPt5_Pt-800to1000_rootFileList.txt) |  |  | 
| [QCD-MuEnrichedPt5_Pt-80to120_rootFileList.txt](mc/QCD-MuEnrichedPt5_Pt-80to120_rootFileList.txt) |  |  | 

### QCD

| rootFileList | Adidtional Info | Comments|
| --------     | --------        | -------- |
| [QCD_HT1000to1500_rootFileList.txt](mc/QCD_HT1000to1500_rootFileList.txt) |  |  | 
| [QCD_HT100to200_ext1_rootFileList.txt](mc/QCD_HT100to200_ext1_rootFileList.txt) |  |  | 
| [QCD_HT100to200_rootFileList.txt](mc/QCD_HT100to200_rootFileList.txt) |  |  | 
| [QCD_HT1500to2000_rootFileList.txt](mc/QCD_HT1500to2000_rootFileList.txt) |  |  | 
| [QCD_HT2000toInf_rootFileList.txt](mc/QCD_HT2000toInf_rootFileList.txt) |  |  | 
| [QCD_HT200to300_rootFileList.txt](mc/QCD_HT200to300_rootFileList.txt) |  |  | 
| [QCD_HT300to500_rootFileList.txt](mc/QCD_HT300to500_rootFileList.txt) |  |  | 
| [QCD_HT500to700_rootFileList.txt](mc/QCD_HT500to700_rootFileList.txt) |  |  | 
| [QCD_HT700to1000_rootFileList.txt](mc/QCD_HT700to1000_rootFileList.txt) |  |  | 

### SUSYGluGluToBBHToBB

| rootFileList | Adidtional Info | Comments|
| --------     | --------        | -------- |
| [SUSYGluGluToBBHToBB_M-1000_rootFileList.txt](mc/SUSYGluGluToBBHToBB_M-1000_rootFileList.txt) |  |  | 
| [SUSYGluGluToBBHToBB_M-1200_rootFileList.txt](mc/SUSYGluGluToBBHToBB_M-1200_rootFileList.txt) |  |  | 
| [SUSYGluGluToBBHToBB_M-120_rootFileList.txt](mc/SUSYGluGluToBBHToBB_M-120_rootFileList.txt) |  |  | 
| [SUSYGluGluToBBHToBB_M-125_rootFileList.txt](mc/SUSYGluGluToBBHToBB_M-125_rootFileList.txt) |  |  | 
| [SUSYGluGluToBBHToBB_M-130_rootFileList.txt](mc/SUSYGluGluToBBHToBB_M-130_rootFileList.txt) |  |  | 
| [SUSYGluGluToBBHToBB_M-1400_rootFileList.txt](mc/SUSYGluGluToBBHToBB_M-1400_rootFileList.txt) |  |  | 
| [SUSYGluGluToBBHToBB_M-140_rootFileList.txt](mc/SUSYGluGluToBBHToBB_M-140_rootFileList.txt) |  |  | 
| [SUSYGluGluToBBHToBB_M-1600_rootFileList.txt](mc/SUSYGluGluToBBHToBB_M-1600_rootFileList.txt) |  |  | 
| [SUSYGluGluToBBHToBB_M-160_rootFileList.txt](mc/SUSYGluGluToBBHToBB_M-160_rootFileList.txt) |  |  | 
| [SUSYGluGluToBBHToBB_M-180_rootFileList.txt](mc/SUSYGluGluToBBHToBB_M-180_rootFileList.txt) |  |  | 
| [SUSYGluGluToBBHToBB_M-200_rootFileList.txt](mc/SUSYGluGluToBBHToBB_M-200_rootFileList.txt) |  |  | 
| [SUSYGluGluToBBHToBB_M-250_rootFileList.txt](mc/SUSYGluGluToBBHToBB_M-250_rootFileList.txt) |  |  | 
| [SUSYGluGluToBBHToBB_M-300_rootFileList.txt](mc/SUSYGluGluToBBHToBB_M-300_rootFileList.txt) |  |  | 
| [SUSYGluGluToBBHToBB_M-350_rootFileList.txt](mc/SUSYGluGluToBBHToBB_M-350_rootFileList.txt) |  |  | 
| [SUSYGluGluToBBHToBB_M-400_rootFileList.txt](mc/SUSYGluGluToBBHToBB_M-400_rootFileList.txt) |  |  | 
| [SUSYGluGluToBBHToBB_M-450_rootFileList.txt](mc/SUSYGluGluToBBHToBB_M-450_rootFileList.txt) |  |  | 
| [SUSYGluGluToBBHToBB_M-500_rootFileList.txt](mc/SUSYGluGluToBBHToBB_M-500_rootFileList.txt) |  |  | 
| [SUSYGluGluToBBHToBB_M-600_rootFileList.txt](mc/SUSYGluGluToBBHToBB_M-600_rootFileList.txt) |  |  | 
| [SUSYGluGluToBBHToBB_M-700_rootFileList.txt](mc/SUSYGluGluToBBHToBB_M-700_rootFileList.txt) |  |  | 
| [SUSYGluGluToBBHToBB_M-800_rootFileList.txt](mc/SUSYGluGluToBBHToBB_M-800_rootFileList.txt) |  |  | 
| [SUSYGluGluToBBHToBB_M-900_rootFileList.txt](mc/SUSYGluGluToBBHToBB_M-900_rootFileList.txt) |  |  | 


