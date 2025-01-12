**Mass-balance model tailored to the Kaskawulsh Glacier, Yukon, Canada.**

The distributed mass-balance model in this repository is adapted from Young et al. (2021). Several changes to the model workflow were introduced in Robinson et al. (2024), such as an annually updated surface elevation and a re-calibration of the model using a tuning scheme that includes distributed snowline observations. Major changes to the model include an improved treatment of supra-glacier debris based on site-specific measurements of ice ablation in the presence of debris and an improved elevation-dependent accumulation bias correction. See K. Robinson's MSc thesis for detailed descriptions of each model component. 

Robinson, K. (2024). Reconstructing a multi-decadal runoff record for a highly-glacierized catchment in Yukon, Canada. MSc thesis. https://summit.sfu.ca/item/38185

See also:

Young, E. M., Flowers, G. E., Berthier, E., & Latto, R. (2021). An imbalancing act: the delayed dynamic response of the Kaskawulsh Glacier to sustained mass loss. Journal of Glaciology, 67(262), 313-330.

Robinson, K. M., Flowers, G. E., & Rounce, D. R. (2024). Sensitivity of modelled mass balance and runoff to representations of debris and accumulation on the Kaskawulsh Glacier, Yukon, Canada.


**Model description summary: **

The climatic mass balance is calculated as the difference between surface accumulation and surface ablation. Ablation is approximated as surface melt minus meltwater that is refrozen. Melt is calculated using the enhanced temperature-index model of Hock (1999), which improves upon the classical degree-day model by capturing the influence of topographic shading, slope, and aspect on melt through incorporating a radiation factor and calculated potential direct clear-sky solar radiation. The impact of supraglacial debris cover on ablation is treated using a distributed estimate of sub-debris melt factors, which either enhance or inhibit ice melt depending on the debris thickness. The sub-debris melt factors are based on an estimate of debris thickness for the Kaskawulsh Glacier from Rounce et al. (2021) and a glacier-specific estimate of the Oestrem curve Robinson et al. (2024), that is, a function that describes the relationship between debris thickness and ablation (Oestrem, 1959). Meltwater retention via refreezing is accounted for using a thermodynic parameterization to estimate the annual potential retention mass (Janssens, 2000). Once this limit is reached, any additional snowmelt or rainfall is assumed to run off. 

Catchment-wide discharge is the sum of all sources of runoff over the glacierized and non-glacierized areas, including glacier-ice melt ($M_{\rm glacier\,\,ice}$), snowmelt ($M_{\rm snow}$), ice melt from the refrozen snowmelt/rain layers formed during previous refreezing events ($M_{\rm refrozen\,\,snowmelt/rain}$), and rainfall ($P_l$), minus the snowmelt and rainfall that are refrozen ($R$). Ice formed from refrozen snowmelt/rain is treated as superimposed ice in the ablation zone and internal accumulation in the accumulation zone. Snowmelt refers to melt of both the seasonal snowpack and snow accumulation that has persisted from previous seasons, as we do not account for the transition from snow to firn. Snowmelt, rainfall, and refreezing are treated the same over the non-glacierized area as the glacierized area of the catchment. We assume that all runoff instantaneously exits the catchment, that is, we do not account for transit times, supraglacial ponding, or englacial/subglacial storage, all of which would delay or reduce the estimated discharge. 
