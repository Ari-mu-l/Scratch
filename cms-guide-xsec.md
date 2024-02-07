- [Run 1](#run1)

   - [7 TeV](#7tev)

   - [8 TeV](#8tev)

- [Run 2](#run2)

   - [Calculate cross sections using GenXSecAnalyzer](#genxsec)
   
   - [Find cross sections at higher order](#higher)

## <a name="run1">Run 1</a>
The cross section values for Run1 Standard Model MC datasets are taken from the following tables. The numbers are obtained either by running published code or by quoting published results in literatures.

### <a name="7tev">7 TeV</a>

|Process|Generator/Source|Phase space cuts|Order|Final state|Cross-section (pb)|Uncertainty (pb): Scale unc. (PDF unc.)|Comments|
| :---- | :------------- | :------------- | :-- | :-------- | :--------------- | :------------------------------------ | :----- |
|W+|	FEWZ|	--	NNLO	W->lv, l=e,m,t	18456	±233 ( ±850) Total = ± 881	Inclusive W production, BR(W->lv) included, l=e,m,t, PDF error also includes alphas
|W-|	FEWZ|	--	NNLO	W->lv, l=e,m,t	12858	±174 (±654) Total = ± 677	Inclusive W production, BR(W->lv) included, l=e,m,t, PDF error also includes alphas
|Total| W|	FEWZ	--	NNLO	W->lv, l=e,m,t	31314	±407 (±1504) Total = ± 1558	Inclusive W production, BR(W->lv) included, l=e,m,t, PDF error also includes alphas
|Z/a* (20)|	FEWZ	m(ll)>20GeV	NNLO	Z -> ll	4998	±34 ( ±270) Total = ± 272	Inclusive Z production Z->ll, l=e,m,t; PDF errors also includes alphas
|Z/a* (50)	FEWZ	m(ll)>50GeV	NNLO	Z -> ll	3048	±34 (±128) Total = ± 132	Inclusive Z production, Z->ll, l=e,m,t; PDF errors also includes alphas
|Z/a* (60-120)	FEWZ	60 < m(ll) < 120 GeV	NNLO	Z -> ll	2916	±34 (±122) Total = ± 127	Inclusive Z production, Z->ll, l=e,m,t; PDF errors also includes alphas
|W+cbar|	MCFM	--	NLO	Inclusive	1718	±157	Massive c quark. Inclusive Wc production and inclusive W decay
|W-c|	MCFM	--	NLO	Inclusive	1910	±164	Massive c quark. Inclusive Wc production and inclusive W decay
|Total| Wc	MCFM	--	NLO	Inclusive	3628	±227	Massive c quark. Inclusive Wc production and inclusive W decay
|W+b bbar|	MCFM	--	LO	Inclusive	22.1	±4.4	Massive b quark. Inclusive Wbb production and inclusive W decay
|W-b bbar|	MCFM	--	LO	Inclusive	13.2	±2.5	Massive b quark. Inclusive Wbb production and inclusive W decay
|Total Wb bbar|	MCFM	--	LO	Inclusive	35.3	±5.1	Massive b quark. Inclusive Wbb production and inclusive W decay
|Z/a*b bbar|	MCFM	m(ll) > 20 GeV	LO	Inclusive	67.3	±18.8	Massive b quark
|W+W-|	MCFM	--	NLO	Inclusive	43	±1.5	Inclusive WW production and inclusive W decay
|W+Z/a*|	MCFM	m(ll) > 40 GeV	NLO	Inclusive	11.8	±0.6	--
|W-Z/a*|	MCFM	m(ll) > 40 GeV	NLO	Inclusive	6.4	±0.4	--
|Total WZ/a*|	MCFM	m(ll) > 40 GeV	NLO	Inclusive	18.2	±0.7	--
|Z/a*Z/a*|	MCFM	m(ll) > 40 GeV	NLO	Inclusive	5.9	±0.15	--
|ttbarW|	--	--	NLO	Inclusive	0.1473	±0.0155	arXiv:1208.2665
|ttbarZ|	--	--	NLO	Inclusive	0.1369	±0.029	arXiv:1208.2665

### <a name="8tev">8 TeV</a>

| Process       | Generator/Source | Phase space cuts     | Order | Final state | Cross section (pb) | Error (pb) scales (+/ PDF) | Comments                                                                                   |
| :------------ | :--------------- | :------------------- | :---- | :---------- | :----------------- | :------------------------- | :----------------------------------------------------------------------------------------- |
| W+            | FEWZ 3.1         | --                   | NNLO  | W->μν       | 7213.4             | +45.3 -21.3 ( ± 241.3 )    | Inclusive W production, BR(W->lv) included, l=μ PDF error also includes alphas, muF=muR=mw |
| W-            | FEWZ 3.1         | --                   | NNLO  | W->μν       | 5074.7             | +33.8 -18.3 ( ± 188.3)     | 
| Total W       | FEWZ 3.1         | --                   | NNLO  | W->μν       | 12234.4            | +79.0 -39.7 (±414.7)       | 
| Z/a*(20)      | FEWZ 3.1         | m(ll)>20 GeV         | NNLO  | Z -> μμ     | 1966.7             | +19.8 -13.7 ( ± 87.7 )     | 
| Z/a* (50)     | FEWZ 3.1         | m(ll)>50 GeV         | NNLO  | Z -> μμ     | 1177.3             | +5.9 -3.6 (±38.8)          | 
| Z/a* (60-120) | FEWZ 3.1         | 60 < m(ll) < 120 GeV | NNLO  | Z -> μμ     | 1129.2             | +5.5 -2.6 (±37.5)          | 
| t tbar	       |                  |                      |       |             |                    |                            | 
| single top    |                  |                      |       |             |                    |                            | 
| W+cbar        | MCFM             | --                   | NLO   | Inclusive   | 2423.5             |                            | 
| W+cbar        | MCFM             | --                   | NLO   | Inclusive   | 2624.6             |                            | 
| Total Wc      | MCFM             | --                   | NLO   | Inclusive   | 5048.1             |                            | 
| Total Wb bbar | aMC@NLO          | --                   | NLO   | Inclusive   | 377.4              | +19.5% -16.8%              | 
| Z/a*b bbar    | MCFM             | m(ll) > 50 GeV       | LO    | Inclusive   | 76.75              |                            | 
| Total WZ/a*   | MCFM             | m(ll) > 12 GeV       | NLO   | Inclusive   | 33.21 (CTEQ), 33.85 (MSTW), 33.72 (NNPDF) |     |
| ttbarW        | MCFM             | --                   | NLO   | Inclusive   | 0.232              | ±0.067 (±PDF error:0.03)   |
| ttbarZ        | NLO              | --                   | NLO   | Inclusive   | 0.2057             | Scale error: +0.019, - 0.024 |
| tqZ; q!=b     | aMC@NLO          | m(ll) > 50 GeV       | NLO   | Z decays to leptons | 0.02450    | Scale error:+3.3% -2.6%    |
| tbZ           | aMC@NLO          | m(ll) > 50 GeV       | NLO   | Z decays to leptons | 0.0114     | Scale error:+3.3% -2.6%    |
| WWW           | aMC@NLO          | --                   | NLO   | Inclusive   | 8.058e-02          | +4.7% -3.9%                | 
| WWZ           | aMC@NLO          | --                   | NLO   | Inclusive   | 5.795e-02          | +5.6% -4.6%                | 
| WZZ           | aMC@NLO          | --                   | NLO   | Inclusive   | 1.968e-02          | +6.0% -4.9%                | 
| ZZZ           | aMC@NLO          | --                   | NLO   | Inclusive   | 5.527e-03          | +2.7% -2.4%                | 
| 4 TOPs        | aMC@NLO          | --                   | NLO   | Inclusive   | 9.144e-04          | +36.3%, -27.0%             | 
| W+ W-         | MCFM 6.6         | 0                    | NLO   | W->eν W->eν | 0.6472             | ± 0.0231 (± 0.0266)        | 
| W+ Z/a*       | MCFM 6.6         | m(l+l-) > 12 GeV     | NLO   | W->μν Z->ee | 0.0748             | ± 0.0025 (± 0.0029)        | 
| W+ Z/a*       | MCFM 6.6         | m(l+l-) > 40 GeV     | NLO   | W->μν Z->ee | 0.0535             | ± 0.0018 (± 0.0028)        | 
| W- Z/a*       | MCFM 6.6         | m(l+l-) > 12 GeV     | NLO   | W->μν Z->ee | 0.0446             | ± 0.0021 (± 0.0018)        | 
| W- Z/a*       | MCFM 6.6         | m(l+l-) > 40 GeV     | NLO   | W->μν Z->ee | 0.0305             | ± 0.0014 (± 0.0014)        | 
| Z/a* Z/a*     | MCFM 6.6         | both dileptonic decay<br>m(l+l-) > 12 GeV | NLO | Z->μμ Z->ee | 0.0385 | ± 0.0011 (± 0.0011) | 
| Z/a* Z/a*     | MCFM 6.6         | both dileptonic decay<br>m(l+l-) > 40 GeV | NLO | Z->μμ Z->ee | 0.0185 | ± 0.0007 (± 0.0007) | 
| Z/a* Z        | MCFM 6.6         | m(l+l- from Z/a*) > 12 GeV | NLO   | Z->ee Z->νν | 0.1318       | ± 0.0040 (± 0.0067)        | 
| Z Z           | MCFM 6.6         | both dileptonic decay<br>m(l+l-) > 1 GeV  | NLO   | Z->ee Z->μμ | 0.0173 | ± 0.0067 (± 0.0007) |

For more details, check this [Twiki](https://twiki.cern.ch/twiki/bin/view/CMSPublic/StandardModelCrossSections). 

## <a name="run2">Run 2</a>

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


