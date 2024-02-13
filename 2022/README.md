### Get the menus python configuration files
```
hltGetConfiguration /frozen/2022/2e34/v1.0/HLT/V1 &> $CMSSW_BASE/src/Analysis/Ntuplizer/python/hlt_menus/2022/v1/frozen_2022_2e34_v1p0_HLT_V1.py
hltGetConfiguration /frozen/2022/2e34/v1.1/HLT/V1 &> $CMSSW_BASE/src/Analysis/Ntuplizer/python/hlt_menus/2022/v1/frozen_2022_2e34_v1p1_HLT_V1.py
hltGetConfiguration /frozen/2022/2e34/v1.1/HLT/V2 &> $CMSSW_BASE/src/Analysis/Ntuplizer/python/hlt_menus/2022/v1/frozen_2022_2e34_v1p1_HLT_V2.py
hltGetConfiguration /frozen/2022/2e34/v1.2/HLT/V1 &> $CMSSW_BASE/src/Analysis/Ntuplizer/python/hlt_menus/2022/v1/frozen_2022_2e34_v1p2_HLT_V1.py
hltGetConfiguration /frozen/2022/2e34/v1.3/HLT/V1 &> $CMSSW_BASE/src/Analysis/Ntuplizer/python/hlt_menus/2022/v1/frozen_2022_2e34_v1p3_HLT_V1.py
hltGetConfiguration /frozen/2022/2e34/v1.4/HLT/V1 &> $CMSSW_BASE/src/Analysis/Ntuplizer/python/hlt_menus/2022/v1/frozen_2022_2e34_v1p4_HLT_V1.py
hltGetConfiguration /frozen/2022/2e34/v1.5/HLT/V1 &> $CMSSW_BASE/src/Analysis/Ntuplizer/python/hlt_menus/2022/v1/frozen_2022_2e34_v1p5_HLT_V1.py
```

### Compile 
```
cd $CMSSW_BASE/src
scram b -j4
```

### Retrieve trigger information – L1 seeds and trigger objects
```
cd $CMSSW_BASE/src/Analysis/Ntuplizer/data/ntuples/2022/v1
trigger_info_from_menu_config.py \
--configs=\
Analysis.Ntuplizer.hlt_menus.2022.frozen_2022_2e34_v1p0_HLT_V1,\
Analysis.Ntuplizer.hlt_menus.2022.frozen_2022_2e34_v1p1_HLT_V1,\
Analysis.Ntuplizer.hlt_menus.2022.frozen_2022_2e34_v1p1_HLT_V2,\
Analysis.Ntuplizer.hlt_menus.2022.frozen_2022_2e34_v1p2_HLT_V1,\
Analysis.Ntuplizer.hlt_menus.2022.frozen_2022_2e34_v1p3_HLT_V1,\
Analysis.Ntuplizer.hlt_menus.2022.frozen_2022_2e34_v1p4_HLT_V1,\
Analysis.Ntuplizer.hlt_menus.2022.frozen_2022_2e34_v1p5_HLT_V1
```

### Put trigger information in a single file
```
cat frozen_*.yml > trigger_info.yml
```
