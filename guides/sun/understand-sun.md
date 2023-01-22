# Understand the Sun

The Sun keeps time on the Farm in [Seasons](../../protocol/glossary.md#season) and incentivizes cost-efficient and timely calling of the [sunrise()](../../protocol/glossary.md#sunrise) function.

You can view [the Sun](../../farm/sun.md) at the upper left corner of [app.bean.money](https://app.bean.money/).

![](../../.gitbook/assets/image.png)

The Sun displays the current Season, which is the number of Seasons completed since `sunrise` was called for the first time. If [Beans were minted](../../peg-maintenance/overview.md#bean-supply) during the current Season based on the [peg maintenance mechanism](../../peg-maintenance/overview.md), the Sun will appear as a rain cloud icon.

Selecting the Sun displays more detail on historical Seasons and a forecast for the next Season. The following information is shown for each Season:

* Number of new Beans minted,
* [Soil](../../farm/field.md#soil) made available in the [Field](../../farm/field.md),
* [Temperature](../../farm/field.md#temperature) for [Sowing Beans](../../protocol/glossary.md#sow),
* [Pod Rate](../../protocol/glossary.md#pod-rate), and
* [Delta Demand](../../protocol/glossary.md#delta-demand), if it was used to measure Demand for Soil. If there is between 0 and 1 Soil remaining at the end of any Season, [Delta Demand is not used](../../peg-maintenance/temperature.md#demand-for-soil).
