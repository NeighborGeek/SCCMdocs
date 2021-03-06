---
title: "Firewalls and domains | Microsoft Docs"
description: "Configure firewalls, ports, and domains to prepare for System Center Configuration Manager communications."
ms.custom: na
ms.date: 10/06/2016
ms.prod: configuration-manager
ms.reviewer: na
ms.suite: na
ms.technology:
  - configmgr-other
ms.tgt_pltfrm: na
ms.topic: get-started-article
ms.assetid: d6993bba-f6bd-4639-adbf-efc1c638b2f3
caps.latest.revision: 15
caps.handback.revision: 0
author: Brendunsms.author: brendunsmanager: angrobe

---
# Configure firewalls, ports, and domains for System Center Configuration Manager*Applies to: System Center Configuration Manager (Current Branch)*
To prepare your network to support System Center Configuration Manager, plan to configure infrastructure like firewalls to pass the communications used by Configuration Manager.  

|Consideration|Details|  
|-------------------|-------------|  
|**Ports and protocols** used by different Configuration Manager capabilities. Some ports are required, while other **Domains and services** can be customized.|Most Configuration Manager communications use common ports such as port 80 for HTTP or 443 for HTTPS communication. However, [some site system roles support use of custom websites](/sccm/core/plan-design/network/websites-for-site-system-servers) and custom ports.<br /><br /> **Before you deploy Configuration Manager**, identify the ports you plan to use and configure firewalls accordingly.<br /><br /> **Later, if you need to change a port** after you install Configuration Manager, don't forget to update firewalls on devices and the network and also change the configuration of the port from within Configuration Manager.<br /><br /> For more information see: </br>- [How to configure client communication ports](../../../core/clients/deploy/configure-client-communication-ports.md) </br>- [Ports used in Configuration Manager](../../../core/plan-design/hierarchy/ports.md) </br>- [Internet access requirements for the service connection point](/sccm/core/servers/deploy/configure/about-the-service-connection-point#bkmk_urls)|  
|**Domains and services** that site servers and clients might need to access.|Configuration Manager capabilities can require site servers and clients have access to specific services and Domains on the internet, like Windowsudpate.microsoft.com or the Microsoft Intune service.<br /><br /> If you will use Microsoft Intune to manage mobile devices, you must also configure access to [ports and domains that are required by Intune.](https://docs.microsoft.com/en-us/intune/get-started/network-infrastructure-requirements-for-microsoft-intune)|  
|**Proxy servers** for site system servers and for client communications. You can specify separate proxy servers for different site system servers and clients.|Because these configurations are made at the time you install a site system role or client, you only need to be aware of the proxy server configurations for later reference when you configure site system roles and clients.<br /><br /> If you're not sure your deployment will need to use proxy servers, review [Proxy server support in System Center Configuration Manager](../../../core/plan-design/network/proxy-server-support.md) to learn about  site system roles and client actions that can use a proxy server.|  
