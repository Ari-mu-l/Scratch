1. [Where do the values come from?](#where)
   1. [Run1](#run1)
   2. [Run2](#run2)
2. [What are different efficiency numbers?](#what)
3. [Where to find NLO-corrected values?](#cmsguide)

## <a name="where">Where do the values come from?</a>

#### <a name="run1">Run1</a>

...

#### <a name="run2">Run2</a>

For Run2, [GenXSecAnalyzer tool](https://github.com/cms-sw/cmssw/blob/CMSSW_7_6_X/GeneratorInterface/Core/plugins/GenXSecAnalyzer.cc) is available to compute cross section from an existing MC sample in MiniAOD format. It retrieves information from [GenLumiInfoProduct](https://github.com/cms-sw/cmssw/blob/CMSSW_7_6_X/SimDataFormats/GeneratorProducts/interface/GenLumiInfoProduct.h) and [GenFilterInfo](https://github.com/cms-sw/cmssw/blob/CMSSW_7_6_X/SimDataFormats/GeneratorProducts/interface/GenFilterInfo.h) to compute averaged cross sections over all the input luminosity blocks.

## <a name="what">What are different efficiency numbers?</a>

- Before matching: the cross section before jet matching and any filter.
- After matching: the cross section after jet matching BUT before any filter.
- Filter efficiency: the efficiency of the any filter.
- After filter: the cross section after jet matching and additional filter are applied. This is your final cross section.
