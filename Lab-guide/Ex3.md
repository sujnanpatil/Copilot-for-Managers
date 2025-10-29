# Exercise 3: Measure Productivity Impact with PR Analysis

### Estimated Duration: 15 Minutes

## Overview

In this exercise, you will import and analyze pull request (PR) metrics from before and after Copilot adoption to measure concrete productivity improvements. You'll compare baseline metrics with post-adoption metrics to quantify the business impact of GitHub Copilot across development teams.

## Objectives

You will be able to complete the following tasks:

- Task 1: Import PR baseline and post-adoption data
- Task 2: Create productivity comparison measures
- Task 3: Build executive-ready productivity impact visualizations

## Prerequisites

- Completion of Exercise 2 with Copilot adoption analysis
- PR baseline and post-adoption CSV files available
- Understanding of software development metrics (lead time, cycle time, PR throughput)

## Task 1: Import and Configure PR Performance Data

In this task, you will load both baseline (pre-Copilot) and post-adoption pull request metrics to establish a comprehensive foundation for measuring concrete productivity improvements. This comparative analysis will provide the quantitative evidence needed to demonstrate Copilot's business impact to stakeholders and executives.

1. Create a new analysis page by clicking the **+ (plus)** icon next to your existing page tab to add a new sheet.

   ![](../media/mang-cor-ex1-g33.png)

   >**Organizing Analysis:** Separating adoption metrics from productivity impact analysis helps stakeholders focus on specific aspects of Copilot's value proposition without overwhelming them with too much information at once.

1. Rename it to PR Impact.

   ![](../media/mang-cor-ex1-g34.png)

1. In your existing Power BI report, go to **Home** → **Get data** → **Text/CSV**.

   ![](../media/git_co_man-e1-g3.png)

1. Browse to **C:\\Copilot_Datasets**, select **pr_baseline.csv**, and click **Open**.

   ![](../media/mang-cor-ex1-g35.png)

1. In the preview dialog, verify the data looks correct and click **Load**.

   ![](../media/mang-cor-ex1-g36.png)

1. Browse to **C:\\Copilot_Datasets**, select **pr_post.csv**, and click **Open**.

   ![](../media/mang-cor-ex1-g37.png)

1. In the preview dialog, verify the data looks correct and click **Load**.

   ![](../media/mang-cor-ex1-g38.png)

   > **Understanding Development Productivity Metrics**: 
> - **Lead Time**: Total time from PR creation to merge, including development work, code reviews, and approval processes - a key indicator of delivery velocity
> - **Cycle Time**: Active development time spent working on code changes, reflecting developer efficiency and focus
> - **PR Size**: Lines of code changed per pull request, indicating complexity and scope of individual contributions
> - **Throughput**: Number of pull requests successfully opened and merged per time period, measuring team delivery capacity
> 
> **Manager Value**: These metrics provide objective measures of development team performance that can be tracked over time to demonstrate the concrete business impact of Copilot adoption.## Task 2: Create Comprehensive Productivity Impact Measures

In this task, you'll create sophisticated measures that quantify the concrete productivity improvements achieved through Copilot adoption. These measures will translate development efficiency gains into quantifiable metrics that demonstrate clear business value and ROI to executive stakeholders.

1. Begin creating baseline metrics by right-clicking the **pr_baseline** table in the Data pane and selecting **New measure**. Create the **Baseline Lead Time** measure:

   ![](../media/mang-cor-ex1-g39.png)

   ![](../media/mang-cor-ex2-g1.png)

   >**Understanding Lead Time:** Lead Time measures the total duration from when a pull request is created until it's merged into the main branch. This includes development time, review cycles, and approval processes - a key indicator of delivery velocity.

   ```
   Baseline Lead Time = AVERAGE('pr_baseline'[lead_time_hours])
   ```

1. Right-click **pr_post** table → **New measure**. Create **Post-Copilot Lead Time**:

   ![](../media/mang-cor-ex2-g2.png)



   ```
   Post-Copilot Lead Time = AVERAGE('pr_post'[lead_time_hours])
   ```

   ![](../media/mang-cor-ex2-g3.png)

1. Create a **Lead Time Improvement** measure in the **pr_baseline** table:

   ```
   Lead Time Improvement = [Baseline Lead Time] - [Post-Copilot Lead Time]
   ```

   ![](../media/mang-cor-ex2-g4.png)

1. Right-click **pr_baseline** table → **New measure**. Create **Lead Time Improvement %**:

   ```
   Lead Time Improvement % = DIVIDE([Lead Time Improvement], [Baseline Lead Time], 0)
   ```

   ![](../media/mang-cor-ex2-g5.png)

   Format this as **Percentage** with **1 decimal place**.

   ![](../media/mang-cor-ex2-g6.png)

1. Right-click **pr_baseline** table → **New measure**. Create **Baseline Cycle Time**:

   ```
   Baseline Cycle Time = AVERAGE('pr_baseline'[cycle_time_hours])
   ```

   ![](../media/mang-cor-ex2-g7.png)

1. Right-click **pr_post** table → **New measure**. Create **Post-Copilot Cycle Time**:

   ```
   Post-Copilot Cycle Time = AVERAGE('pr_post'[cycle_time_hours])
   ```

   ![](../media/mang-cor-ex2-g8.png)

1. Right-click **pr_baseline** table → **New measure**. Create **Cycle Time Improvement %**:

   ```
   Cycle Time Improvement % = DIVIDE(
       [Baseline Cycle Time] - [Post-Copilot Cycle Time], 
       [Baseline Cycle Time], 
       0
   )
   ```

   Format as **Percentage** with **1 decimal place**.

   ![](../media/mang-cor-ex2-g9.png)

1. Right-click **pr_baseline** table → **New measure**. Create **Baseline PRs Merged**:

   ```
   Baseline PRs Merged = AVERAGE('pr_baseline'[prs_merged])
   ```

   ![](../media/mang-cor-ex2-g10.png)

1. Right-click **pr_post** table → **New measure**. Create **Post-Copilot PRs Merged**:

   ```
   Post-Copilot PRs Merged = AVERAGE('pr_post'[prs_merged])
   ```

   ![](../media/mang-cor-ex2-g11.png)

1. Right-click **pr_baseline** table → **New measure**. Create **Throughput Improvement %**:

   ```
   Throughput Improvement % = DIVIDE(
       [Post-Copilot PRs Merged] - [Baseline PRs Merged],
       [Baseline PRs Merged],
       0
   )
   ```

   ![](../media/mang-cor-ex2-g12.png)

## Task 3: Build Executive-Ready Productivity Impact Dashboard

In this task, you will create compelling visualizations that clearly communicate the tangible productivity improvements achieved through Copilot adoption. These visuals will serve as powerful storytelling tools for executive presentations and business case justifications.

### A. Create High-Impact Productivity KPI Cards

1. Begin by inserting **Card** visuals that highlight your most important productivity metrics. Click the **Card** visual icon in the **Visualizations** pane:

   ![](../media/mang-cor-ex2-g13.png)

   >**Executive Communication:** Card visuals provide immediate visual impact by prominently displaying key metrics. They're perfect for executive dashboards where stakeholders need to quickly grasp performance improvements.

1. Create cards for these measures:
   - **Lead Time Improvement %**

   ![](../media/mang-cor-ex2-g14.png)

   - **Cycle Time Improvement %** 
   - **Throughput Improvement %**

   ![](../media/mang-cor-ex2-g15.png)

   > **Manager Value**: These cards immediately show the quantifiable impact of Copilot investment with clear percentage improvements.

### B. Create Team Performance Comparison

1. Insert a **Clustered bar chart**.

   ![](../media/mang-cor-ex2-g16.png)

1. Configure the chart:
   - **Y-axis**: team (from pr_baseline)
   - **X-axis**: Lead Time Improvement %
   - **Legend**: (none needed)

   ![](../media/mang-cor-ex2-g17.png)

   > **Manager Insight**: This shows which teams are benefiting most from Copilot, helping identify best practices to share across the organization.

### C. Create Before/After Metrics Table

1. Insert a **Matrix** visual.

   ![](../media/mang-cor-ex2-g18.png)

1. Configure the matrix:
   - **Rows**: team
   - **Values**: 
     - Baseline Lead Time
     - Post-Copilot Lead Time
     - Lead Time Improvement %
     - Throughput Improvement %
   
      ![](../media/mang-cor-ex2-g19.png)

   > **Executive Value**: This provides a comprehensive view of improvements across all teams in a single table format.

### D. Add Team Performance Slicers

1. Insert a **Slicer** for **team** from the pr_baseline table with **Tile** style.

   ![](../media/mang-cor-ex2-g20.png)

   ![](../media/mang-cor-ex2-g21.png)

1. This allows filtering all visuals by specific teams to focus analysis.

   ![](../media/mang-cor-ex2-g22.png)

## Notes

- **Positive improvements** in lead time and cycle time reductions indicate faster delivery
- **Increased throughput** shows teams are completing more work in the same time
- Use the team slicer to analyze which teams are seeing the most benefit from Copilot
- Focus on teams with significant improvements to identify success patterns that can be replicated
- Consider that different teams may show benefits in different areas (some in speed, others in throughput)

<validation step="ex3-validate-productivity" />

> **Congratulations** on completing the task! Now, it's time to validate it. Here are the steps:
> - Hit the Validate button for the corresponding task. If you receive a success message, you can proceed to the next task. 
> - If not, carefully read the error message and retry the step, following the instructions in the lab guide.
> - If you need any assistance, please contact us at cloudlabs-support@spektrasystems.com. We are available 24/7 to help.

## Summary

In this exercise, you successfully measured the concrete productivity impact of GitHub Copilot by establishing comprehensive before-and-after comparisons using pull request metrics. You created sophisticated measures that quantify lead time reductions, cycle time improvements, and throughput increases, transforming technical improvements into business-relevant insights. The executive-ready visualizations you built provide compelling evidence of Copilot's value proposition, giving you the quantitative foundation needed for ROI calculations and strategic decision-making. This productivity analysis, combined with your adoption metrics from Exercise 2, creates a comprehensive view of Copilot's organizational impact that will be essential for the final ROI dashboard in Exercise 4.

### You have successfully completed this exercise, please continue to next one >>

   ![](../media/a-gs-g2.png)