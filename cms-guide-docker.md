1. [Where do the values come from?](#where)
   1. [Run1](#run1)
   2. [Run2](#run2)
2. [What are different efficiency numbers?](#what)
3. [Where to find NLO-corrected values?](#cmsguide)

## <a name="where">Where do the values come from?</a>

#### <a name="run1">Run1</a>

The cross section values for Run1 Standard Model MC datasets are taken from the following table. The numbers are obtained either by running published code or by quoting published results in literatures.

| Process       | Generator/Source | Phase space cuts | Order | Final state | Cross section (pb) | Error (pb) scales (+/ PDF) | Comments |
| :------------ | :--------------- | :--------------- | :---- | :---------- | :----------------- | :------------------------- | :------- |
| W+            | FEWZ 3.1         |  |
| W-            | FEWZ 3.1         |  |
| Total W       | FEWZ 3.1         |  |
| Z/a*(20)      | FEWZ 3.1         |  |
| Z/a* (50)     | FEWZ 3.1         |
| Z/a* (60-120) | FEWZ 3.1         |
| t tbar	       |                  |
| single top    |                  |
| W+cbar        | MCFM             |
| W+cbar        | MCFM             |
| Total Wc      | MCFM             |
| Total Wb bbar | aMC@NLO          |
| Z/a*b bbar    | MCFM             |
| Total WZ/a*   | MCFM             |
| ttbarW        | MCFM             |
| ttbarZ        | NLO              |
| tqZ; q!=b     | aMC@NLO          |
| tbZ           | aMC@NLO          |
| WWW           | aMC@NLO          |
| WWZ           | aMC@NLO          |
| WZZ           | aMC@NLO          |
| ZZZ           | aMC@NLO          |
| 4 TOPs        | aMC@NLO          |
| W+ W-         | MCFM 6.6         |
| W+ Z/a*       | MCFM 6.6         |
| W+ Z/a*       | MCFM 6.6         |
| W+ Z/a*       | MCFM 6.6         |
| W- Z/a*       | MCFM 6.6         |
| Z/a* Z/a*     | MCFM 6.6         |
| Z/a* Z/a*     | MCFM 6.6         |
| Z/a* Z        | MCFM 6.6         |
| Z Z           | MCFM 6.6         |

#### <a name="run2">Run2</a>

For Run2, [GenXSecAnalyzer tool](https://github.com/cms-sw/cmssw/blob/CMSSW_7_6_X/GeneratorInterface/Core/plugins/GenXSecAnalyzer.cc) is available to compute cross section from an existing MC sample in MiniAOD format. It retrieves information from [GenLumiInfoProduct](https://github.com/cms-sw/cmssw/blob/CMSSW_7_6_X/SimDataFormats/GeneratorProducts/interface/GenLumiInfoProduct.h) and [GenFilterInfo](https://github.com/cms-sw/cmssw/blob/CMSSW_7_6_X/SimDataFormats/GeneratorProducts/interface/GenFilterInfo.h) to compute averaged cross sections over all the input luminosity blocks.

Setup the cms environment following the [instruction](/docs/cms-getting-started-miniaod).

Inside the CMSSW_X_X_X/src directory, fetch the sample configuration file:
```
curl https://raw.githubusercontent.com/cms-sw/genproductions/master/Utilities/calculateXSectionAndFilterEfficiency/genXsec_cfg.py -o ana.py
```

Examine the configuration file with your preferred editor. Within the configuration file,

```
process.maxEvents = cms.untracked.PSet(
    input = cms.untracked.int32(options.maxEvents)
)
```
sets the maximum number of events passed to the GenXSecAnalyzer. Set it to `-1` if you would like to use all the events.

```
process.source = cms.Source ("PoolSource",
    fileNames = cms.untracked.vstring(options.inputFiles),
    secondaryFileNames = secFiles)
```
specifies the names of the root files to be used.

You may specify `inputFiles` and `maxEvents` and run the script in command line:
```
cmsRun ana.py inputFiles="file:root://eospublic.cern.ch//eos/opendata/cms/mc/RunIIFall15MiniAODv2/QCDJets_flat_pythia_shifted15mmvertex/MINIAODSIM/PU25nsData2015v1_Shifted15mmCollision2015_76X_mcRun2_asymptotic_v12-v1/60000/00D4D020-59B8-E511-8D6D-A0000420FE80.root" maxEvents=10
```

Here we use a root file from 2015 QCD MC sample and set the maximum number of events to 10.

The printout should look like this:
```
------------------------------------
GenXsecAnalyzer:
------------------------------------
Before Filtrer: total cross section = 1.887e+09 +- 7.281e+07 pb
Filter efficiency (taking into account weights)= (3.38384) / (3.38384) = 1.000e+00 +- 0.000e+00
Filter efficiency (event-level)= (200) / (200) = 1.000e+00 +- 0.000e+00
After filter: final cross section = 1.887e+09 +- 7.281e+07 pb

=============================================
```

The cross section values for Run2 on the Open Data Portal are computed using a maximum number of 1e7 or 1e8 events from each MC dataset.

<!---
To use a list of root files to compute the cross section for one sample or to automate the process for multiple samples, we need to first have a file list for each MC sample.

For example, if we would like to compute the cross section of *QCDuubar_Pt-15to3000_TuneZ2star_Flat_13TeV_pythia6* for 2015 collision data using all the files in this sample, we may first get the filelist from the [Open Data Portal](https://opendata.cern.ch/record/18392).

Download the filelist to CMSSW_X_X_X/src:
```
curl https://opendata.cern.ch/record/18392/files/CMS_mc_RunIIFall15MiniAODv2_QCDuubar_Pt-15to3000_TuneZ2star_Flat_13TeV_pythia6_MINIAODSIM_PU25nsData2015v1_76X_mcRun2_asymptotic_v12-v1_60000_file_index.txt -o filelist.txt
```
-->


## <a name="what">What are different efficiency numbers?</a>

- Before matching: the cross section before jet matching and any filter.
- After matching: the cross section after jet matching BUT before any filter.
- Filter efficiency: the efficiency of the any filter.
- After filter: the cross section after jet matching and additional filter are applied. This is your final cross section.

## <a name="where">Where to find NLO-corrected values?</a>


