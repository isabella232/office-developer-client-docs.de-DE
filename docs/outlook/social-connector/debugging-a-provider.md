---
title: Debuggen eines Providers
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d2dfaeed-7635-4c6b-9c35-b955ca1a85e9
description: 'Sie haben verschiedene Möglichkeiten, die Sie einen Anbieter für Outlook Social Connector (OSC) debuggen können:'
ms.openlocfilehash: 39deb7b6c0b11460826bdbf1957ffd8404d926e5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386852"
---
# <a name="debugging-a-provider"></a><span data-ttu-id="bce6a-103">Debuggen eines Providers</span><span class="sxs-lookup"><span data-stu-id="bce6a-103">Debugging a provider</span></span>

<span data-ttu-id="bce6a-104">Sie haben verschiedene Möglichkeiten, die Sie einen Anbieter für Outlook Social Connector (OSC) debuggen können:</span><span class="sxs-lookup"><span data-stu-id="bce6a-104">There are several ways you can debug an Outlook Social Connector (OSC) provider:</span></span> 
  
- <span data-ttu-id="bce6a-105">Mithilfe von Debug-Befehle in der Menübandkomponente der Office Fluent-Benutzeroberfläche in Outlook oder der unterstützenden Office-Clientanwendung, die dazu führen, dass die OSC verschiedene Aktionen ausführen.</span><span class="sxs-lookup"><span data-stu-id="bce6a-105">By using debug commands in the ribbon component of the Office Fluent user interface in Outlook or the supporting Office client application to cause the OSC to take various actions.</span></span>
    
- <span data-ttu-id="bce6a-106">Mithilfe von Fiddler Trace-API-Aufrufe und XML, die zwischen einem sozialen Netzwerk und den OSC-Anbieter gesendet</span><span class="sxs-lookup"><span data-stu-id="bce6a-106">By using Fiddler to trace API calls and XML sent between a social network and its OSC provider</span></span>
    
## <a name="debug-buttons"></a><span data-ttu-id="bce6a-107">Debuggen von Schaltflächen</span><span class="sxs-lookup"><span data-stu-id="bce6a-107">Debug buttons</span></span>

<span data-ttu-id="bce6a-108">Die Erweiterbarkeit des OSC-Providers bietet die Möglichkeit zum Debuggen eines OSC-Providers.</span><span class="sxs-lookup"><span data-stu-id="bce6a-108">The OSC provider extensibility provides the capability of debugging an OSC provider.</span></span> <span data-ttu-id="bce6a-109">Um einen Anbieter zu debuggen, Erstellen einer `DebugProviders` Wert des Typs DWORD-Wert in der Windows-Registrierung unter der `SocialConnector` wichtige (wie in der folgenden Zeile dargestellt), und legen Sie die `DebugProviders` Wert auf 1.</span><span class="sxs-lookup"><span data-stu-id="bce6a-109">To debug a provider, create a  `DebugProviders` value of type DWORD in the Windows registry under the  `SocialConnector` key (as shown in the following line), and set the  `DebugProviders` value to 1.</span></span> 
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`
  
<span data-ttu-id="bce6a-110">Standardmäßig ist das Debuggen Anbieter deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="bce6a-110">By default, provider debugging is off.</span></span> <span data-ttu-id="bce6a-111">Wenn die `DebugProviders` Wert ist nicht vorhanden, oder es vorhanden ist und auf einen Wert von 0 Anbieter Debuggen festgelegt ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="bce6a-111">If the  `DebugProviders` value is not present, or it is present and set to a value of 0, provider debugging is turned off.</span></span> 
  
<span data-ttu-id="bce6a-112">Wenn der Anbieter das Debuggen aktiviert ist, zeigt die OSC ein Warnungsdialogfeld mit ausführlichen Fehlerinformationen, wenn ein Fehler tritt auf, und alle OSC-Anbieter XML für das OSC-Anbieter XML-Schema überprüft.</span><span class="sxs-lookup"><span data-stu-id="bce6a-112">If provider debugging is turned on, the OSC displays an alert dialog box with verbose error information when an error occurs, and validates any OSC provider XML against the OSC provider XML schema.</span></span> <span data-ttu-id="bce6a-113">Basierend auf den Namespace für eine XML-Zeichenfolge angegeben, wird der OSC 1.0-Schemadatei OutlookSocialProvider.xsd ein OSC-Anbieters mit OSC 1.0 entwickelt überprüft.</span><span class="sxs-lookup"><span data-stu-id="bce6a-113">Based on the namespace specified for an XML string, an OSC provider developed by using OSC 1.0 is validated against the OSC 1.0 schema file, OutlookSocialProvider.xsd.</span></span> <span data-ttu-id="bce6a-114">Ein OSC-Anbieters mithilfe von OSC 1.1 entwickelt oder später anhand der Schemadatei OutlookSocialProvider_1.1.xsd überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="bce6a-114">An OSC provider developed by using OSC 1.1 or later is validated against the schema file, OutlookSocialProvider_1.1.xsd.</span></span> <span data-ttu-id="bce6a-115">Bei Verwendung der `DebugProviders` -Wert, die Debug-Benachrichtigung wird für alle geladenen Anbieter anstelle eines bestimmten Anbieters angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bce6a-115">When you use the  `DebugProviders` value, the debug alert appears for all loaded providers instead of a specific provider.</span></span> 
  
<span data-ttu-id="bce6a-116">Um Debug Schaltflächen anzuzeigen, die beim Debuggen eines Providers helfen kann, Erstellen einer `ShowDebugButtons` Wert des Typs DWORD-Wert in der Windows-Registrierung unter der `SocialConnector` -Taste, und legen Sie die `ShowDebugButtons` Wert auf 1.</span><span class="sxs-lookup"><span data-stu-id="bce6a-116">To display debug buttons that can help you debug a provider, create a  `ShowDebugButtons` value of type DWORD in the Windows registry under the  `SocialConnector` key, and set the  `ShowDebugButtons` value to 1.</span></span> <span data-ttu-id="bce6a-117">Legen Sie zum Ausblenden der Befehlsleisten-Schaltflächen Debuggen die `ShowDebugButtons` Wert auf 0.</span><span class="sxs-lookup"><span data-stu-id="bce6a-117">To hide the debug command bar buttons, set the  `ShowDebugButtons` value to 0.</span></span> 
  
<span data-ttu-id="bce6a-118">Für Outlook 2010 und Clientanwendungen gegenüber Office 2013 werden die Debug-Schaltflächen auf der Registerkarte ' **Add-Ins** ' des Menübands Explorer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bce6a-118">For Outlook 2010 and client applications since Office 2013, the debug buttons appear on the **Add-ins** tab of the explorer ribbon.</span></span> <span data-ttu-id="bce6a-119">Für Outlook 2007 und Outlook 2003 werden die Debug-Schaltflächen auf der standard-Befehlsleiste für das Outlook Explorer-Fenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bce6a-119">For Outlook 2007 and Outlook 2003, the debug buttons appear on the standard command bar of the Outlook explorer window.</span></span> 
  
<span data-ttu-id="bce6a-120">Die folgende Tabelle beschreibt die Debug-Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="bce6a-120">The following table describes the debug buttons.</span></span>
  
|<span data-ttu-id="bce6a-121">**Schaltfläche Debuggen**</span><span class="sxs-lookup"><span data-stu-id="bce6a-121">**Debug button**</span></span>|<span data-ttu-id="bce6a-122">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="bce6a-122">**Function**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bce6a-123">Kontakte synchronisieren</span><span class="sxs-lookup"><span data-stu-id="bce6a-123">Sync Contacts</span></span>  <br/> |<span data-ttu-id="bce6a-124">Bewirkt, dass das osc bilden den OSC-Anbieter zur zwischengespeicherten Kontakte nur aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="bce6a-124">Causes the OSC to ask the OSC provider for cached contacts only.</span></span>  <br/> |
|<span data-ttu-id="bce6a-125">Synchronisierung der globalen Adressliste</span><span class="sxs-lookup"><span data-stu-id="bce6a-125">GAL Sync</span></span>  <br/> |<span data-ttu-id="bce6a-126">Bewirkt, dass die OSC zum Auffüllen von Daten aus der globalen Adressliste von Exchange zu Outlook-Kontakten.</span><span class="sxs-lookup"><span data-stu-id="bce6a-126">Causes the OSC to populate data from the Exchange Global Address List to Outlook contacts.</span></span>  <br/> |
|<span data-ttu-id="bce6a-127">Kategorie Cache ungültig</span><span class="sxs-lookup"><span data-stu-id="bce6a-127">Invalidate Category Cache</span></span>  <br/> |<span data-ttu-id="bce6a-128">Bewirkt, dass das osc bilden, die Kategorieliste für jeden Speicher erneut zu laden, wenn die Aktivitätsfeed aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="bce6a-128">Causes the OSC to reload the category list for each store when the activity feed is refreshed.</span></span>  <br/> |
   
## <a name="fiddler"></a><span data-ttu-id="bce6a-129">Fiddler</span><span class="sxs-lookup"><span data-stu-id="bce6a-129">Fiddler</span></span>

<span data-ttu-id="bce6a-130">Fiddler ist ein Tool zum Debuggen von über das Netzwerk, die API-Aufrufe, die von Ihrem Dienstanbieter in sozialen Netzwerken gesendet und dem sozialen Netzwerk an Ihren Anbieter gesendeten XML überprüfen.</span><span class="sxs-lookup"><span data-stu-id="bce6a-130">Fiddler is an over-the-wire debugging tool to check the API calls sent from your provider to the social network, and XML sent by the social network to your provider.</span></span> <span data-ttu-id="bce6a-131">Fiddler steht unter [Fiddler Web Debugging Proxy](https://www.fiddler2.com/fiddler2/version.asp)zum Download zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="bce6a-131">Fiddler is available for download at [Fiddler Web Debugging Proxy](https://www.fiddler2.com/fiddler2/version.asp).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bce6a-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bce6a-132">See also</span></span>

- [<span data-ttu-id="bce6a-133">QuickSteps für Informationen zum Entwickeln eines Providers</span><span class="sxs-lookup"><span data-stu-id="bce6a-133">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)  
- [<span data-ttu-id="bce6a-134">Synchronisieren von Freunde und Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="bce6a-134">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md) 
- [<span data-ttu-id="bce6a-135">Bewährte Methoden für das Entwickeln eines Providers</span><span class="sxs-lookup"><span data-stu-id="bce6a-135">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
- [<span data-ttu-id="bce6a-136">OSC - Typische Aufrufsequenzen</span><span class="sxs-lookup"><span data-stu-id="bce6a-136">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)  
- [<span data-ttu-id="bce6a-137">Entwickeln eines Providers mit dem OSC-XML-Schema</span><span class="sxs-lookup"><span data-stu-id="bce6a-137">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)  
- [<span data-ttu-id="bce6a-138">Vorbereitung der Freigabe eines OSC-Providers</span><span class="sxs-lookup"><span data-stu-id="bce6a-138">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)

