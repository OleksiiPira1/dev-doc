---
title: Cancellation Offers Report
excerpt: 'See how viewers move through the cancellation flow and how retention offers perform for your app'
deprecated: false
hidden: false
metadata:
  title: 'Cancellation Offers Analytics Report | Roku Developer Docs'
  description: 'The Cancellation Offers Analytics Report shows how many viewers enter the cancellation flow, how many are shown a retention offer, what they do after seeing it, and which offers are redeemed by plan and currency.'
  robots: index
next:
  description: ''
---
You can use the Cancellation Offers Analytics Report to see how many viewers enter the manage-subscription/cancellation experience, how many are shown a retention offer, what viewers do after seeing an offer (accept, cancel anyway, or take no action), and which offers are ultimately redeemed by plan and currency.

This report is especially useful for evaluating the health of your retention strategy: whether offers are reaching the right viewers, how effective they are at preventing churn, and which price points and billing cadences drive the most redemptions. Reviewing these trends week over week helps you spot shifts in cancellation behavior early and adjust your offer strategy before churn accelerates.

## Filters

The filters applied to this report are:

* **Channel ID** – Identifies the app whose cancellation and offer data you want to analyze. A Channel ID is required for the report to return data.

* **Date Filter** – Sets the data sample period for the entire report (for example, "is in the last 30 days" or a custom date range). All visualizations are aggregated by week (Date Key Week) within the selected period.

## Visualizations

The report includes the following three charts, which are aggregated weekly along the horizontal axis (Date Key Week):

* Weekly Retention offer funnel
* Weekly Cancellations without offer
* Weekly offer redemptions by plan cadence and currency

You can click any item in the legend at the bottom of a chart to isolate or combine metrics.

> Some legend labels use internal shorthand ("AR" refers to auto-renew). The plain-language definition beneath each label explains what the metric represents from the viewer's perspective.

### Weekly Retention offer funnel

![roku815px - cancellation-weekly-retention](https://image.roku.com/ZHZscHItMTc2/cancellation-weekly-retention.png "cancellation-weekly-retention")

The Weekly Subscriptions and Offers visualization shows the top of the retention funnel, from entering the cancellation flow through the outcome after an offer is shown.

The metrics in this report track how many viewers reach the manage-subscription experience, how many are shown a retention offer, and what they do next:

* **Manage Subscription Events** – The number of times viewers entered the manage-subscription/cancellation experience.

* **Shown Offer** – Viewers who were presented with a retention offer during that flow.

* **Shown Offer Accept Offer** – Viewers who were shown an offer and accepted it (a successful save).

* **Shown Offer And Cancel** – Viewers who were shown an offer but chose to cancel anyway (offer did not save them).

* **Shown Offer No Accept No Cancel** – Viewers who were shown an offer, did not accept it, and did not cancel — effectively a passive save where the viewer took no further action.

### Weekly cancellations without offer

![roku815px - cancellation-weekly-events](https://image.roku.com/ZHZscHItMTc2/cancellation-weekly-events.png "cancellation-weekly-events")

The Weekly Cancellation Events report shows cancellation activity, including viewers who were not shown an offer and their eventual outcome.

The metrics in this report break down cancellation activity, focusing on viewers who initiated cancellation but were not shown a retention offer, and whether they ultimately canceled.

* **Cancellation Flow Started** (dashboard label: Cancel Initiation Events) – Viewers who started the cancellation flow.

* **Started Cancellation, No Action Taken** – Viewers who started cancellation but neither accepted an offer nor turned off auto-renew — a passive save where the viewer took no action and did not cancel.

* **Started Cancellation, No Offer Shown** – Viewers who initiated cancellation and were not shown a retention offer. This group splits into the two outcomes below.

* **No Offer Shown, Subscription Canceled** – Viewers not shown an offer who went through with the cancellation (auto-renew turned off).

* **No Offer Shown, Subscription Retained** – Viewers not shown an offer who did not go through with the cancellation. Comparing this against the "Subscription Canceled" group gives the save rate for viewers who were never shown an offer.

### Weekly offer redemptions by cadence and currency

![roku815px - cancellation-weekly-redemption](https://image.roku.com/ZHZscHItMTc2/cancellation-weekly-redemption.png "cancellation-weekly-redemption")

The Weekly Redemption Offers visualization shows the number of offers redeemed each week, broken down by currency and billing cadence.

The metrics in this report track the total number of retention offers redeemed each week (vertical axis: Offer Redemptions), stacked by currency and billing cadence so you can see which price points and plan types drive the most saves:

* **BRL - Monthly** – Offers redeemed on monthly plans billed in Brazilian Real.

* **MXN - Monthly** – Offers redeemed on monthly plans billed in Mexican Peso.

* **USD - Monthly** – Offers redeemed on monthly plans billed in US dollars.

* **MXN - Yearly** – Offers redeemed on annual plans billed in Mexican Peso.

* **USD - Yearly** – Offers redeemed on annual plans billed in US dollars.
