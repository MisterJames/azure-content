<properties
   pageTitle="Azure Security Center quick start guide | Microsoft Azure"
   description="This article helps you get started quickly with Azure Security Center by guiding you through the security monitoring and policy management components and linking you to next steps."
   services="security-center"
   documentationCenter="na"
   authors="TerryLanfear"
   manager="MBaldwin"
   editor=""/>

<tags
   ms.service="security-center"
   ms.devlang="na"
   ms.topic="article"
   ms.tgt_pltfrm="na"
   ms.workload="na"
   ms.date="10/28/2016"
   ms.author="terrylan"/>

# Azure Security Center quick start guide

This article helps you quickly get started with Azure Security Center by guiding you through the security monitoring and policy management components of Security Center.

> [AZURE.NOTE] This article introduces the service by using an example deployment. This article is not a step-by-step guide.

## Prerequisites

To get started with Security Center, you must have a subscription to Microsoft Azure. If you do not have a subscription, you can sign up for a [free account](https://azure.microsoft.com/pricing/free-trial/).

The Free tier of Security Center is automatically enabled with your subscription and provides visibility into the security state of your Azure resources. It provides basic security policy management, security recommendations, and integration with security products and services from Azure partners.

You access Security Center from the [Azure portal](https://azure.microsoft.com/features/azure-portal/). To learn more about the Azure portal, see the [portal documentation](https://azure.microsoft.com/documentation/services/azure-portal/).

## Data collection

Security Center collects data from your virtual machines (VMs) to assess their security state, provide security recommendations, and alert you to threats. When you first access Security Center, data collection is enabled on all VMs in your subscription. Data collection is recommended, but you can opt out by turning off data collection in the Security Center policy.

The following steps describe how to access and use the components of Security Center. In these steps, we show you how to turn off data collection if you choose to opt out.

## Access Security Center

In the portal, follow these steps to access Security Center:

1. On the **Microsoft Azure** menu, select **Security Center**.
![Azure menu][1]

2. If you are accessing Security Center for the first time, the **Welcome** blade opens. Select **Yes! I want to Launch Azure Security Center** to open the **Security Center** blade and to enable data collection.
![Welcome screen][10]

3. After you launch Security Center from the Welcome blade or select Security Center from the Microsoft Azure menu, the **Security Center** blade opens. For easy access to the **Security Center** blade in the future, select the **Pin blade to dashboard** option (upper right).
![Pin blade to dashboard option][2]

## Use Security Center

You can configure security policies for your Azure subscriptions and resource groups. Let's configure a security policy for your subscription:

1. On the **Security Center** blade, select the **Policy** tile.
![Security policy][3]

2. On the **Security policy - Define policy per subscription or resource group** blade, select a subscription.
3. On the **Security policy** blade, **Data collection** is enabled to automatically collect logs. The monitoring extension is provisioned on all current and new VMs in the subscription. (You can opt out of data collection by setting **Data collection** to **Off**, but this prevents Security Center from giving you security alerts and recommendations.)
4. On the **Security policy** blade, select **Choose a storage account per region**. For each region in which you have VMs running, you choose the storage account where data collected from those VMs is stored. If you do not choose a storage account for each region, it is created for you. The data that's collected is logically isolated from other customers' data for security reasons.

     > [AZURE.NOTE] We recommend that you enable data collection and choose a storage account at the subscription level first. Security policies can be set at the Azure subscription level and resource group level, but configuration of data collection and storage account occurs at the subscription level only.

5. On the **Security policy** blade, select **Prevention policy**. This opens the **Prevention policy** blade.
![Prevention policy][4]

6. On the **Prevention policy** blade, turn on the recommendations that you want to see as part of your security policy. Examples:

 - Setting **System updates** to **On** scans all supported virtual machines for missing OS updates.
 - Setting **OS vulnerabilities** to **On** scans all supported virtual machines to identify any OS configurations that might make the virtual machine more vulnerable to attack.

### View recommendations

1. Return to the **Security Center** blade and select the **Recommendations** tile. Security Center periodically analyzes the security state of your Azure resources. When Security Center identifies potential security vulnerabilities, it shows recommendations on the **Recommendations** blade.
![Recommendations in Azure Security Center][5]

2.	Select a recommendation on the **Recommendations** blade to view more information and/or to take action to resolve the issue.

### View the health and security state of your resources

1.	Return to the **Security Center** blade. The **Resources security health** tile contains indicators of the security state for virtual machines, networking, data, and applications.
2.	Select **Virtual machines** to view more information. The **Virtual machines** blade opens and displays a status summary of antimalware programs, system updates, restarts, and OS vulnerabilities of your VMs.
![The Resources health tile in Azure Security Center][6]

3.	Select a recommendation under **VIRTUAL MACHINE RECOMMENDATIONS** to view more information and/or take action to configure necessary controls.
4.	Select a VM under **Virtual machines** to view additional details.

### View security alerts

1.	Return to the **Security Center** blade and select the **Security alerts** tile. The **Security alerts** blade opens and displays a list of alerts. The Security Center analysis of your security logs and network activity generates these alerts. Alerts from integrated partner solutions are included.
![Security alerts in Azure Security Center][7]

    > [AZURE.NOTE] Security alerts are only available if the Standard tier of Security Center is enabled. A 90 day free trial of the Standard tier is available. See [Next steps](#next-steps) for information on how to get the Standard tier.

2.	Select an alert to view additional information. In this example, let's select **Modified system binary discovered**. This opens blades that provide additional details about the alert.
![Security alert details in Azure Security Center][8]

### View the health of your partner solutions

1. Return to the **Security Center** blade. The **Partner solutions** tile lets you monitor, at a glance, the health status of your partner solutions integrated with your Azure subscription.
2. Select the **Partner solutions** tile. A blade opens and displays a list of your partner solutions connected to Security Center.
![Partner solutions][9]

3. Select a partner solution. In this example, let's select the **F5-WAF** solution.  A blade opens and shows you the status of the partner solution and the solution's associated resources. Select **Solution console** to open the partner management experience for this solution.

## Next steps
This article introduced you to the security monitoring and policy management components of Security Center. Now that you're familiar with Security Center, try the following steps:

- Configure a security policy for your Azure subscription. To learn more, see [Setting security policies in Azure Security Center](security-center-policies.md).
- Use the recommendations in Security Center to help you protect your Azure resources. To learn more, see [Managing security recommendations in Azure Security Center](security-center-recommendations.md).
- Review and manage your current security alerts. To learn more, see [Managing and responding to security alerts in Azure Security Center](security-center-managing-and-responding-alerts.md).
- Learn more about the [advanced threat detection features](security-center-detection-capabilities.md) that come with the [Standard tier](security-center-pricing.md) of Security Center. A 90 day free trial of the Standard tier is available.
- If you have questions about using Security Center, see the [Azure Security Center FAQ](security-center-faq.md).

<!--Image references-->
[1]: ./media/security-center-get-started/azure-menu.png
[2]: ./media/security-center-get-started/security-center-pin.png
[3]: ./media/security-center-get-started/security-policy.png
[4]: ./media/security-center-get-started/prevention-policy.png
[5]: ./media/security-center-get-started/recommendations.png
[6]: ./media/security-center-get-started/resources-health.png
[7]: ./media/security-center-get-started/security-alert.png
[8]: ./media/security-center-get-started/security-alert-detail.png
[9]: ./media/security-center-get-started/partner-solutions.png
[10]: ./media/security-center-get-started/welcome.png
