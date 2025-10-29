# Exercise 1: Enable & Access Copilot Usage Reports

### Estimated Duration: 15 Minutes

## Overview

In this exercise, you will enable and access GitHub Copilot organization-level usage reports to establish foundational visibility for managers and program owners. You will learn how to request activity reports that provide crucial data about adoption patterns, user engagement, and usage metrics across your organization. These reports form the basis for the comprehensive analytics dashboard you'll build in subsequent exercises, enabling data-driven decisions about Copilot deployment and optimization.

## Objectives

You will be able to complete the following tasks:

- Task 1: Navigate to GitHub Copilot administrative settings and activate reporting features
- Task 2: Request and download organization-level usage data for analysis

## Prerequisites

- You are an **Organization Owner** of the target GitHub organization (e.g., `contoso-impact`).
- GitHub Copilot Business or Enterprise is already licensed for the org.
- Email access to the owner mailbox (for the report-ready notification).

## Task 1: Navigate to GitHub Copilot Administrative Settings

In this task, you will navigate to the GitHub Copilot administrative area within your organization settings and initiate the Activity report generation. This report provides comprehensive usage data that managers need to understand Copilot adoption across their development teams.

1. In the top-right corner of GitHub, click your **profile picture (1)** and select **Organizations (2)** from the dropdown menu.

   ![](../media/gt-co-ex1-g1.png)

   >**Note:** You must have Organization Owner permissions to access Copilot usage reports. If you don't see your organization listed, contact your GitHub administrator.

1. On the **Settings › Organizations** page, locate and click your organization **contoso-impact** where you have **Owner** role permissions.  

   ![](../media/gt-co-ex1-g2.png)

1. Once you're in the organization dashboard, navigate to the **Settings** tab from the top navigation menu.  

   ![](../media/gt-co-ex1-g3.png)

   >**Manager Insight:** The organization settings area is where you control all aspects of Copilot deployment, including user access, policy settings, and usage reporting.

1. In the left sidebar navigation, locate the **Code, planning, and automation (1)** section, expand **Copilot (2)**, and click on **Access (3)**.  

   ![](../media/gt-co-ex1-g4.png)

1. On the **Access management** page, locate the **Get Usage report (1)** section and select **Activity report (new) (2)** from the available options.

   ![](../media/gt-co-ex1-g5.png)

   >**Understanding Activity Reports:** The Activity report provides per-user metrics including code suggestions, acceptances, chat usage, and technology preferences. This data is essential for measuring adoption success and identifying areas for improvement.

## Task 2: Request and Download Organization Usage Data

In this task, you will initiate the report generation process and obtain the CSV file containing your organization's Copilot usage data. This data will serve as the foundation for all subsequent analysis and dashboard creation.

1. After selecting the Activity report option, confirm that the green notification banner **"Your activity report is being generated…"** appears at the top of the page.  

   ![](../media/gt-co-ex1-g6.png)

   >**Important:** Report generation is an asynchronous process that runs in the background. The time required depends on your organization size and usage history.

1. Monitor your email for the notification titled **"Your GitHub Copilot Activity report is ready"** and download the attached CSV file when it becomes available.  

   ![](../media/gt-co-ex1-g7.png)

   >**Manager Value:** This CSV contains per-user data including suggestions offered, acceptances, team assignments, editor preferences, and chat usage patterns - all critical metrics for understanding Copilot ROI and adoption success.

1. Once downloaded, save the CSV file to a known location on your computer for use in the upcoming exercises.

   >**Best Practice:** Keep the original CSV file unmodified as your source of truth. You'll create working copies for analysis in Power BI to preserve data integrity.

## Notes

- If you do not see **Activity report (new)**, ensure your organization is on a supported Copilot plan and that you have Owner permissions.
- The downloaded CSV (often named like `copilot_org.csv`) will be used in Exercise 2 for building analytics measures.
- Regenerating a report overwrites the previous pending request but does not delete earlier downloaded files you saved locally.
- Keep the raw CSV unmodified; create a copy for transformation steps in later exercises.

<validation step="ex1-validate-usage-report" />

> **Congratulations** on completing the task! Now, it's time to validate it. Here are the steps:
> - Hit the Validate button for the corresponding task. If you receive a success message, you can proceed to the next task. 
> - If not, carefully read the error message and retry the step, following the instructions in the lab guide.
> - If you need any assistance, please contact us at cloudlabs-support@spektrasystems.com. We are available 24/7 to help.

## Summary

In this exercise, you successfully enabled GitHub Copilot usage reporting and initiated the Activity report generation process. You learned how to navigate the administrative settings, request comprehensive usage data, and understand the value of this information for management decision-making. The CSV dataset you obtained now serves as the authoritative foundation for all subsequent adoption analysis, engagement metrics, and ROI calculations you'll perform in the following exercises. This data-driven approach ensures your Copilot program decisions are based on concrete evidence rather than assumptions.

### You have successfully completed this exercise, please continue to next one >>

   ![](../media/a-gs-g2.png)
