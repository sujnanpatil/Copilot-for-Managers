# GitHub Copilot for Managers

### Overall Estimated Duration: 1 Hour

## Overview

In this lab, you will configure and visualize organization-level **GitHub Copilot** adoption and impact. Using a pre-prepared report with **Copilot Activity (CSV)** and **Copilot Metrics (JSON)**, you’ll publish to the Power BI Service and assemble an executive-friendly view. You’ll practice essentials like adding KPIs, weekly trends, and cohort slicers, and you’ll use lightweight measures (e.g., adoption rate, estimated time saved) to communicate value clearly. Step-by-step instructions with screenshots guide you throughout.

## Objective

Understand how to measure and communicate Copilot adoption and impact. By the end of this lab, you will be able to:

- **Create & Publish a Report:** Build a concise dashboard from Copilot Activity CSV and Metrics JSON and publish it to the Power BI Service.
- **Build & Organize a Dashboard:** Add KPIs and trends (active vs. engaged, suggestions vs. acceptances, chat usage), plus editor/language filters.
- **Enhance Presentation:** Apply branding touches (logos/themes optional), use simple ROI and adoption-rate measures, and prepare a one-page executive readout.

## Pre-requisites

- Basic knowledge of Power BI
- Access to **Power BI Desktop** and **Power BI Service**
- Read access to sample **Copilot Activity CSV** and **Copilot Metrics JSON** (provided)

## Architecture

You’ll start from a pre-created Power BI report wired to two sources:
1. **Copilot Activity (CSV):** Per-user adoption fields (e.g., suggestions, acceptances, last activity, editor/language cohorts).
2. **Copilot Metrics (JSON):** Org-level daily metrics (active users, engaged users, suggestions, acceptances, chat, PR summaries).

You’ll add visuals for **KPIs**, **weekly trends**, and **cohorts**, and then publish to the Power BI Service. Optionally, you’ll apply a theme and capture screenshots for an executive readout.

## Architecture Diagram

![](../media/arch1.PNG)

## Explanation of Components

- **Copilot Activity (CSV):** Per-user aggregates that support developer-level and cohort charts (acceptances, suggestions, last activity, editor, language).
- **Copilot Metrics (JSON):** Daily org-level counts for active/engaged users, suggestions vs. acceptances, chat usage, and PR assistant activity.
- **Power BI Service:** Cloud platform to publish, manage access, and share dashboards with leadership.

## Getting Started with the Lab

Once you're ready to dive in, your virtual machine and lab guide will be right at your fingertips within your web browser.

![](../media/12062025(0)new.png)

## Virtual Machine & Lab Guide

Your virtual machine is your workhorse throughout the workshop. The lab guide is your roadmap to success.

## Exploring Your Lab Resources

To get a better understanding of your lab resources and credentials, navigate to the **Environment** tab.

![](../media/power-02new.png)

## Utilizing the Split Window Feature

For convenience, you can open the lab guide in a separate window by selecting the **Split Window** button from the top right corner.

![](../media/power-03new.png)

## Managing Your Virtual Machine

On the **Resources (1)** tab, use the **Action buttons (2)** next to your VM. Feel free to **start**, **stop**, or **restart** your Virtual Machine as needed. Your experience is in your hands!

![](../media/power-04new.png)

## Lab Guide Zoom In/Zoom Out

To adjust the zoom level for the environment page, click the **A↕ : 100%** icon located next to the timer in the lab environment.

![](../media/zoomnew1.png)

## Let's Get Started with Power BI Portal

1. On the Lab VM, Open **Power BI Desktop** from the desktop of your lab environment.

    ![](../media/image105.png)

1. Click the **Sign-in** icon (top-right).

    ![](../media/image200.png)

1. In **Enter your email address**, paste:

    - **Email/Username:** <inject key="AzureAdUserEmail"></inject>

1. In Then select **Continue**.

    ![](../media/image106.png)

1. When prompted again, sign in with:

     - **Email/Username:** <inject key="AzureAdUserEmail"></inject>

        ![](../media/image101.png)

1. Enter the password and **Sign in**.

    - **Password:** <inject key="AzureAdUserPassword"></inject>

        ![](../media/image102.png)

1. For the prompt **Automatically sign in to all desktop apps and websites on this device?**, select **No, this app only**.

    ![](../media/image107.png)

## Support Contact

The CloudLabs support team is available 24/7, 365 days a year, via email and live chat.

**Learner Support Contacts:**
- Email: cloudlabs-support@spektrasystems.com  
- Live Chat: https://cloudlabs.ai/labs-support

Click **Next** at the bottom-right to begin your lab journey!

## Happy Learning!!
