---
lab:
    task: 'Configure Communication Compliance'
    exercise: 'Exercise 4 - Configure Communication Compliance'
---
## WWL Tenants - Terms of use

If you are being provided with a tenant as a part of an instructor-led training delivery, please note that the tenant is made available for the purpose of supporting the hands-on labs in the instructor-led training.

Tenants should not be shared or used for purposes outside of hands-on labs. The tenant used in this course is a trial tenant and cannot be used or accessed after the class is over and are not eligible for extension.

Tenants must not be converted to a paid subscription. Tenants obtained as a part of this course remain the property of Microsoft Corporation and we reserve the right to obtain access and repossess at any time.

# Exercise 4 skilling tasks

- **Predefined template policy**: Create a communication compliance policy using a predefined template.
- **Customized template policy**: Create a communication compliance policy by modifying a predefined template.
- **Custom communication policy**: Create a unique communication compliance policy tailored to specific organizational needs.

## Task 1 - Create a communication compliance policy from a template

In this task, you will create a policy using a predefined template to quickly address common compliance scenarios.

1. In Microsoft Edge, navigate to the Microsoft Purview portal, `https://purview.microsoft.com`, and log in.
1. Select **View all solutions**.
1. Under **Risk & Compliance** select the **Communication Compliance** card.
1. In the left navigation pane, select **Policies**.
1. Select **Create policy** and review the available policy templates:

   - **Copilot interactions**: Monitors all interactions with Copilot for Microsoft 365.
   - **Inappropriate content**: Detects hate, violence, sexual content, and self-harm in Microsoft Teams.
   - **Inappropriate text**: Flags threats, discrimination, and harassment in Exchange Online, Microsoft Teams, and Viva Engage.
   - **Inappropriate images**: Identifies adult and racy images in Exchange Online and Microsoft Teams.
   - **Sensitive information**: Monitors sensitive information across Exchange Online, Microsoft Teams, and Viva Engage with a lower review percentage.
   - **Regulatory compliance**: Ensures compliance with financial regulations in Exchange Online, Microsoft Teams, and Viva Engage.
   - **Conflict of interest**: Detects potential conflicts of interest internally within Exchange Online, Microsoft Teams, and Viva Engage.

1. Select the policy template for **Detect inappropriate text**.
1. On the **Detect communications for inappropriate text** fly-out page on the right, enter the user that will be reviewing communication compliance alerts in the **Reviewers** field.
1. Select **Create policy** at the bottom of the fly-out page, then select **Close** on the **Your policy was created** page.

You have successfully created a communication compliance policy using the **Detect inappropriate text template**.

## Task 2 - Create a communication compliance policy from a customized template

Here you will modify a policy template to tailor it to specific organizational needs.

1. You should still be on the **Policies** page within **Communication Compliance** in the Microsoft Purview portal.

   If not, in Microsoft Edge, navigate to the Microsoft Purview portal, `https://purview.microsoft.com` and log in. Select **View all solutions** > **Communication Compliance** card under **Risk & Compliance**.

1. Select **Create policy** > **Detect inappropriate images**.
1. On the **Detect communications for inappropriate images** fly-out page on the right, select **Customize policy** at the bottom of the fly-out page.
1. Select **Customize policy** at the bottom of the fly-out page.
1. On the **Name and describe your policy** select **Next**.
1. On the **Choose users and reviewers** page, enter the user that will be reviewing communication compliance alerts in the **Reviewers** field, then select **Next**.
1. On the **Choose locations to detect communications** page, enable the locations for:

   - Exchange.
   - Teams.
   - Viva Engage.

1. Select **Next**.
1. On the **Choose conditions and review percentage**, review the default actions for the inappropriate images template, and select **Next**.
1. On the **Review and finish** page, select **Create policy**, then select **Done** on the **Your policy was updated** page.

You have successfully customized a communication compliance policy using the **Detect inappropriate images** template.

## Task 3 - Create a custom communication compliance policy

In this task, you will build a communication compliance policy from scratch to meet unique compliance requirements.

1. You should still be on the **Policies** page within **Communication Compliance** in the Microsoft Purview portal.

   If not, in Microsoft Edge, navigate to the Microsoft Purview portal, `https://purview.microsoft.com` and log in. Select **View all solutions** > **Communication Compliance** card under **Risk & Compliance**.

1. Select **Create policy** > **Custom policy**.
1. On the **Name and describe your policy** page, enter:

   - **Name**: `Global Communication Compliance Policy`
   - **Description**: `Monitors emails and Teams messages for policy violations.`

1. Select **Next**.
1. On the **Choose users and reviewers** page:

   - Under **Choose users and groups** select **All users**.
   - Leave the field for **Excluded users and groups** blank.
   - In the **Reviewers** field, enter the reviewers who will monitor compliance alerts.

1. Select **Next**.
1. On the **Choose locations to detect communications** only enable:

   - Exchange
   - Teams

   Ensure all other locations aren't selected.

1. Select **Next**.
1. On the **Choose conditions and review percentage** page, leave the defaults selected for **Communication direction**.
1. Under **Conditions**, enable the option to use the **New condition builder (preview)**.
1. Select **+ Add condition** > **Content matches trainable classifier**.
1. Under **Content matches trainable classifiers** select **Add** > **Trainable classifiers**.
1. On the **Trainable classifiers** fly-out page on the right, select classifiers for **Regulatory Collusion**, **Stock manipulation**, **Unauthorized disclosure**, and **Corporate Sabotage**.
1. Select **Add** at the bottom of the **Trainable classifiers** fly-out page on the right.
1. Back on the **Choose conditions and review percentage** page, adjust the **Review percentage** slider to **25%**.
1. Select **Next** on the bottom of the **Choose conditions and review percentage** page.
1. On the **Review and finish** page, select **Create policy**, then select **Done** on the **Your policy was created** page.

You have successfully created a custom communication compliance policy named _Global Communication Compliance Policy_.
