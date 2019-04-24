---
title: Debuggen eines Providers
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d2dfaeed-7635-4c6b-9c35-b955ca1a85e9
description: 'Es gibt mehrere Möglichkeiten zum Debuggen eines OSC-Anbieters (Outlook Social Connector):'
ms.openlocfilehash: 39deb7b6c0b11460826bdbf1957ffd8404d926e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281069"
---
# <a name="debugging-a-provider"></a><span data-ttu-id="b1358-103">Debuggen eines Providers</span><span class="sxs-lookup"><span data-stu-id="b1358-103">Debugging a provider</span></span>

<span data-ttu-id="b1358-104">Es gibt mehrere Möglichkeiten zum Debuggen eines OSC-Anbieters (Outlook Social Connector):</span><span class="sxs-lookup"><span data-stu-id="b1358-104">There are several ways you can debug an Outlook Social Connector (OSC) provider:</span></span> 
  
- <span data-ttu-id="b1358-105">Durch Verwenden von Debug-Befehlen in der Menüband-Komponente der Office Fluent-Benutzeroberfläche in Outlook oder der unterstützenden Office-Clientanwendung, damit OSC verschiedene Aktionen ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="b1358-105">By using debug commands in the ribbon component of the Office Fluent user interface in Outlook or the supporting Office client application to cause the OSC to take various actions.</span></span>
    
- <span data-ttu-id="b1358-106">Durch die Verwendung von Fiddler zum Nachverfolgen von API-aufrufen und XML, die zwischen einem sozialen Netzwerk und seinem OSC-Anbieter gesendet werden</span><span class="sxs-lookup"><span data-stu-id="b1358-106">By using Fiddler to trace API calls and XML sent between a social network and its OSC provider</span></span>
    
## <a name="debug-buttons"></a><span data-ttu-id="b1358-107">Debug-Schaltflächen</span><span class="sxs-lookup"><span data-stu-id="b1358-107">Debug buttons</span></span>

<span data-ttu-id="b1358-108">Die OSC-Anbieter Erweiterbarkeit bietet die Möglichkeit zum Debuggen eines OSC-Anbieters.</span><span class="sxs-lookup"><span data-stu-id="b1358-108">The OSC provider extensibility provides the capability of debugging an OSC provider.</span></span> <span data-ttu-id="b1358-109">Erstellen Sie zum Debuggen eines Anbieters `DebugProviders` in der Windows-Registrierung unter dem `SocialConnector` Schlüssel einen Wert vom Typ DWORD (wie in der folgenden Abbildung dargestellt), und `DebugProviders` legen Sie den Wert auf 1 fest.</span><span class="sxs-lookup"><span data-stu-id="b1358-109">To debug a provider, create a  `DebugProviders` value of type DWORD in the Windows registry under the  `SocialConnector` key (as shown in the following line), and set the  `DebugProviders` value to 1.</span></span> 
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`
  
<span data-ttu-id="b1358-110">Standardmäßig ist das Anbieter Debugging deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b1358-110">By default, provider debugging is off.</span></span> <span data-ttu-id="b1358-111">Wenn der `DebugProviders` Wert nicht vorhanden ist, oder er vorhanden ist und auf den Wert 0 festgelegt ist, wird das Anbieter Debugging deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b1358-111">If the  `DebugProviders` value is not present, or it is present and set to a value of 0, provider debugging is turned off.</span></span> 
  
<span data-ttu-id="b1358-112">Wenn das Anbieter Debugging aktiviert ist, zeigt der OSC ein Warnungsdialogfeld mit ausführlichen Fehlerinformationen an, wenn ein Fehler auftritt, und überprüft alle OSC-Anbieter-XML-Daten anhand des OSC-Anbieter-XML-Schemas.</span><span class="sxs-lookup"><span data-stu-id="b1358-112">If provider debugging is turned on, the OSC displays an alert dialog box with verbose error information when an error occurs, and validates any OSC provider XML against the OSC provider XML schema.</span></span> <span data-ttu-id="b1358-113">Basierend auf dem für eine XML-Zeichenfolge angegebenen Namespace wird ein mit OSC 1,0 entwickelter OSC-Anbieter anhand der OSC 1,0-Schemadatei OutlookSocialProvider. xsd validiert.</span><span class="sxs-lookup"><span data-stu-id="b1358-113">Based on the namespace specified for an XML string, an OSC provider developed by using OSC 1.0 is validated against the OSC 1.0 schema file, OutlookSocialProvider.xsd.</span></span> <span data-ttu-id="b1358-114">Ein OSC-Anbieter, der mit OSC 1,1 oder höher entwickelt wurde, wird anhand der Schemadatei OutlookSocialProvider_ 1.1. xsd validiert.</span><span class="sxs-lookup"><span data-stu-id="b1358-114">An OSC provider developed by using OSC 1.1 or later is validated against the schema file, OutlookSocialProvider_1.1.xsd.</span></span> <span data-ttu-id="b1358-115">Wenn Sie den `DebugProviders` Wert verwenden, wird die Debug-Warnung für alle geladenen Anbieter anstelle eines bestimmten Anbieters angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b1358-115">When you use the  `DebugProviders` value, the debug alert appears for all loaded providers instead of a specific provider.</span></span> 
  
<span data-ttu-id="b1358-116">Zum Anzeigen von Debug-Schaltflächen, die Ihnen beim Debuggen eines Anbieters helfen können, erstellen Sie in der Windows- `SocialConnector` Registrierung unter dem Schlüssel einen `ShowDebugButtons` `ShowDebugButtons` Wert vom Typ DWORD, und legen Sie den Wert auf 1 fest.</span><span class="sxs-lookup"><span data-stu-id="b1358-116">To display debug buttons that can help you debug a provider, create a  `ShowDebugButtons` value of type DWORD in the Windows registry under the  `SocialConnector` key, and set the  `ShowDebugButtons` value to 1.</span></span> <span data-ttu-id="b1358-117">Um die Debug-Befehlsleistenschaltflächen auszublenden, `ShowDebugButtons` legen Sie den Wert auf 0 fest.</span><span class="sxs-lookup"><span data-stu-id="b1358-117">To hide the debug command bar buttons, set the  `ShowDebugButtons` value to 0.</span></span> 
  
<span data-ttu-id="b1358-118">Für Outlook 2010-und Clientanwendungen seit Office 2013 werden die Debug-Schaltflächen auf der Registerkarte **Add-ins** des Explorer-Menübands angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b1358-118">For Outlook 2010 and client applications since Office 2013, the debug buttons appear on the **Add-ins** tab of the explorer ribbon.</span></span> <span data-ttu-id="b1358-119">Für Outlook 2007 und Outlook 2003 werden die Debug-Schaltflächen in der Standardbefehls Leiste des Outlook-Explorer-Fensters angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b1358-119">For Outlook 2007 and Outlook 2003, the debug buttons appear on the standard command bar of the Outlook explorer window.</span></span> 
  
<span data-ttu-id="b1358-120">In der folgenden Tabelle werden die Debug-Schaltflächen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b1358-120">The following table describes the debug buttons.</span></span>
  
|<span data-ttu-id="b1358-121">**Debug-Schaltfläche**</span><span class="sxs-lookup"><span data-stu-id="b1358-121">**Debug button**</span></span>|<span data-ttu-id="b1358-122">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="b1358-122">**Function**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b1358-123">Kontakte synchronisieren</span><span class="sxs-lookup"><span data-stu-id="b1358-123">Sync Contacts</span></span>  <br/> |<span data-ttu-id="b1358-124">Veranlasst OSC, den OSC-Anbieter nur für zwischengespeicherte Kontakte zu Fragen.</span><span class="sxs-lookup"><span data-stu-id="b1358-124">Causes the OSC to ask the OSC provider for cached contacts only.</span></span>  <br/> |
|<span data-ttu-id="b1358-125">GAL-Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="b1358-125">GAL Sync</span></span>  <br/> |<span data-ttu-id="b1358-126">Veranlasst OSC, Daten aus der globalen Exchange-Adressliste in Outlook-Kontakte aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="b1358-126">Causes the OSC to populate data from the Exchange Global Address List to Outlook contacts.</span></span>  <br/> |
|<span data-ttu-id="b1358-127">Ungültiger Category-Cache</span><span class="sxs-lookup"><span data-stu-id="b1358-127">Invalidate Category Cache</span></span>  <br/> |<span data-ttu-id="b1358-128">Veranlasst OSC, die Kategorienliste für jeden Speicher neu zu laden, wenn der Aktivitätsfeed aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="b1358-128">Causes the OSC to reload the category list for each store when the activity feed is refreshed.</span></span>  <br/> |
   
## <a name="fiddler"></a><span data-ttu-id="b1358-129">Fiddler</span><span class="sxs-lookup"><span data-stu-id="b1358-129">Fiddler</span></span>

<span data-ttu-id="b1358-130">Fiddler ist ein Over-The-Wire-Debugging-Tool zum Überprüfen der API-Aufrufe, die von Ihrem Anbieter an das soziale Netzwerk gesendet werden, und XML, die vom sozialen Netzwerk an Ihren Anbieter gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="b1358-130">Fiddler is an over-the-wire debugging tool to check the API calls sent from your provider to the social network, and XML sent by the social network to your provider.</span></span> <span data-ttu-id="b1358-131">Fiddler kann unter [Fiddler Web Debugging Proxy](https://www.fiddler2.com/fiddler2/version.asp)heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="b1358-131">Fiddler is available for download at [Fiddler Web Debugging Proxy](https://www.fiddler2.com/fiddler2/version.asp).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b1358-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1358-132">See also</span></span>

- [<span data-ttu-id="b1358-133">Schnelle Schritte für die Entwicklung eines Anbieters</span><span class="sxs-lookup"><span data-stu-id="b1358-133">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)  
- [<span data-ttu-id="b1358-134">Synchronisieren von Freunden und Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="b1358-134">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md) 
- [<span data-ttu-id="b1358-135">Bewährte Methoden für die Entwicklung eines Anbieters</span><span class="sxs-lookup"><span data-stu-id="b1358-135">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
- [<span data-ttu-id="b1358-136">OSC - Typische Aufrufsequenzen</span><span class="sxs-lookup"><span data-stu-id="b1358-136">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)  
- [<span data-ttu-id="b1358-137">Entwickeln eines Providers mit dem OSC-XML-Schema</span><span class="sxs-lookup"><span data-stu-id="b1358-137">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)  
- [<span data-ttu-id="b1358-138">Vorbereitung der Freigabe eines OSC-Providers</span><span class="sxs-lookup"><span data-stu-id="b1358-138">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)

