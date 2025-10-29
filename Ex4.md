## Exercise 4: Report and Drive Adoption

### Estimated Duration: 15 Minutes

## Overview

In this exercise, you will assemble an executive-focused dashboard that unifies adoption (usage) metrics and productivity impact signals. You will introduce adjustable ROI parameters (Seconds Saved, Hourly Rate), surface key KPIs, and prepare a concise leadership readout with actionable recommendations.

## Objectives

You will be able to complete the following tasks:

- Task 1: Build an executive dashboard (KPIs, trends, cohorts, ROI measures, bookmark)
- Task 2: Present findings & next steps (summary narrative and recommended actions)

## Prerequisites

- Completion of Exercises 1–3 (usage CSV ingested, core measures defined).
- Existing measures: Active Users, Total Acceptances, Acceptance Rate %, Time Saved (hrs) or equivalent, Δ Throughput %, Lead Time Pre (hrs), Lead Time Post (hrs).
- Dataset tables accessible: `copilot_org`, `pr_post` (or your renamed equivalents).

## KPI Glossary

- Active Users: Distinct users with any Copilot activity in current filter context.
- Acceptance Rate %: Total Acceptances ÷ Total Suggestions.
- Total Acceptances: Count of suggestions accepted by users.
- Δ Throughput %: Percentage change in throughput (PRs or accepted suggestions) post-adoption vs baseline.
- Lead Time Post (hrs): Average post-adoption lead time metric (replace with your defined measure if named differently).
- Estimated Hours Saved: ([Total Acceptances] × [Seconds Saved Value]) ÷ 3600.
- Estimated Savings: [Estimated Hours Saved] × [Hourly Rate Value].
- Time Saved (hrs): Heuristic time savings from earlier exercises (optional if using dynamic Estimated Hours Saved).

## Task 1: Build an Executive Dashboard

In this task, you will curate visuals and create parameter-driven ROI measures for leadership-ready reporting.

1. Create a new page: click **+** at the bottom → rename to **Executive Dashboard**.  

   ![](../media/co-po-ex4-g1.png)  
   
   ![](../media/co-po-ex4-g2.png)
   
1. Add What-If parameters (ROI knobs): **Modeling → New parameter → Numeric range**.

   - Seconds Saved: Min 5, Max 60, Increment 5, Default 20, Add slicer = On. 
   
     ![](../media/co-po-ex4-g3.png)  
     
     ![](../media/co-po-ex4-g4.png)
     
   - Hourly Rate: Min 20, Max 150, Increment 5, Default 60.  
   
     ![](../media/co-po-ex4-g5.png)
     
1. Create ROI measures:
   - `Estimated Hours Saved := DIVIDE ( [Total Acceptances] * [Seconds Saved Value], 3600 )`  
   
     ![](../media/co-po-ex4-g6.png)
     
   - `Estimated Savings := [Estimated Hours Saved] * [Hourly Rate Value]` 
   
     ![](../media/co-po-ex4-g8.png)
     
## Task 2: Present Findings & Next Steps

In this task, you will create a concise executive readout and package shareable artifacts to drive action on adoption and productivity improvements.

1. Add ROI cards (row 1): Cards for **Estimated Hours Saved**, **Estimated Savings** (Format Currency), **Total Acceptances**.  

   ![](../media/co-po-ex4-g10.png)
   
1. Lead time KPI: Add Card for **Lead Time Post (hrs)** (or placeholder).  

   ![](../media/co-po-ex4-g11.png)
   
1. Improvement by developer (row 2): Insert **Clustered bar chart**.  
   - Y-axis: `pr_post[dev]`  
   - X-axis: `Δ Throughput %` (sort descending).  
   
   ![](../media/co-po-ex4-g12.png)
   
1. (Optional) Top performer callout: measure `Top Performer (Name) := VAR t = TOPN ( 1, VALUES ( pr_post[dev] ), [Δ Throughput %], DESC ) RETURN CONCATENATEX ( t, pr_post[dev], ", " )` then Card.  

   ![](../media/co-po-ex4-g13.png)
   
1. Usage trend (row 3): Line chart with X = `copilot_org[date]`, Y = `Total Suggestions` + `Total Acceptances`.  

   ![](../media/co-po-ex4-g14.png)
1. Slicers (left column): add slicers for `editor_primary`, `language_primary`, `pr_post[team]` (Style = Tile).

1. Format & align: Display units = None (cards); percentage KPIs Decimal = 1; page size 16:9, clean layout.

### Task: Publish the Power BI report to the Power BI Service

1. In **Power BI Desktop**, select **File** from the top-left menu.  

   ![](../media/gt-co-ex1-g8.png)

1. In the left pane, select **Publish (1)**, then on the right choose **Publish to Power BI (2)**. 

   ![](../media/gt-co-ex1-g9.png)

1. When prompted **Do you want to save your changes?**, select **Save**.  

   ![](../media/gt-co-ex1-g10.png)

1. In **Save this file**, confirm the name (e.g., `Copilot_PowerBI.pbix`) and select **Save**.  

   ![](../media/gt-co-ex1-g11.png)

1. In **Publish to Power BI**, choose **My workspace (1)** and select **Select (2)**. 

   ![](../media/gt-co-ex1-g12.png)

1. After publishing succeeds, select **Got it**. (You can use the link to open the report in Power BI.)  

   ![](../media/gt-co-ex1-g13.png)

## Summary

In this exercise, you built a leadership-ready Copilot adoption and ROI dashboard, added dynamic parameters for scenario modeling, and prepared an actionable executive readout. These assets enable data-driven prioritization of enablement and productivity initiatives.

### You have successfully completed this exercise. Thank you for advancing through the lab series >>


