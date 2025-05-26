Checks:
1. Make sure you have a valid proxy

```bash
cmsrel CMSSW_13_3_3
cd CMSSW_13_3_3/src
cmsenv
mkdir LHEWeightsReader
cd LHEWeightsReader

git clone https://github.com/NielsVdBossche/LHEWeightsReader

scram b -j 10
cd LHEWeightsReader/test/
cmsRun lheWeightReader_cfg.py inputFiles="MINIAOD_FILE"
```

The changes for CMSSW 13 should be the same as for CMSSW 12 and also 14+ versions unless something gets deprecated in the EDAnalyzer object in the future.
