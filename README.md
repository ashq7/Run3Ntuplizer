Installation:

```

cmsrel CMSSW_12_4_3
cd CMSSW_12_4_3/src/
cmsenv
git cms-init
git cms-addpkg L1Trigger/L1TCaloLayer1
git cms-merge-topic ashq7:l1boosted-regioninfo
cd L1Trigger
git clone -b L1boosted_124X_regioninfo git@github.com:ashq7/Run3Ntuplizer.git
cd ..
scram b -j 12

## to edit analyzer:
vim ~/CMSSW_12_4_3/src/L1Trigger/Run3Ntuplizer/BoostedJetStudies.cc

## to run after installation:
ssh [username]@lxplus.cern.ch
cd CMSSW_12_4_3/src/
cmsenv
scram b -j 8
cd L1Trigger/Run3Ntuplizer/test

## to run boosted ggHbb events
cmsRun testL1TCaloSummary-ggHBB.py
## note capital BB!


```
