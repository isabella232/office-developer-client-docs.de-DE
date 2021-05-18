---
title: Debuggen eines Providers
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d2dfaeed-7635-4c6b-9c35-b955ca1a85e9
description: 'Es gibt verschiedene Möglichkeiten, einen Outlook Social Connector (OSC)-Anbieter zu debuggen:'
ms.openlocfilehash: 39deb7b6c0b11460826bdbf1957ffd8404d926e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281069"
---
# <a name="debugging-a-provider"></a><span data-ttu-id="d5a18-103">Debuggen eines Providers</span><span class="sxs-lookup"><span data-stu-id="d5a18-103">Debugging a provider</span></span>

<span data-ttu-id="d5a18-104">Es gibt verschiedene Möglichkeiten, einen Outlook Social Connector (OSC)-Anbieter zu debuggen:</span><span class="sxs-lookup"><span data-stu-id="d5a18-104">There are several ways you can debug an Outlook Social Connector (OSC) provider:</span></span> 
  
- <span data-ttu-id="d5a18-105">Durch Die Verwendung von Debugbefehlen in der Menübandkomponente der Office Fluent-Benutzeroberfläche in Outlook oder der unterstützenden Office-Clientanwendung kann die OSC verschiedene Aktionen ausführen.</span><span class="sxs-lookup"><span data-stu-id="d5a18-105">By using debug commands in the ribbon component of the Office Fluent user interface in Outlook or the supporting Office client application to cause the OSC to take various actions.</span></span>
    
- <span data-ttu-id="d5a18-106">Verwenden von Fiddler zum Verfolgen von API-Aufrufen und XML, die zwischen einem sozialen Netzwerk und seinem OSC-Anbieter gesendet werden</span><span class="sxs-lookup"><span data-stu-id="d5a18-106">By using Fiddler to trace API calls and XML sent between a social network and its OSC provider</span></span>
    
## <a name="debug-buttons"></a><span data-ttu-id="d5a18-107">Debugschaltflächen</span><span class="sxs-lookup"><span data-stu-id="d5a18-107">Debug buttons</span></span>

<span data-ttu-id="d5a18-108">Die Erweiterbarkeit des OSC-Anbieters bietet die Möglichkeit, einen OSC-Anbieter zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="d5a18-108">The OSC provider extensibility provides the capability of debugging an OSC provider.</span></span> <span data-ttu-id="d5a18-109">Erstellen Sie zum Debuggen eines Anbieters einen Wert vom Typ DWORD in der Windows-Registrierung unter dem Schlüssel (wie in der folgenden Zeile gezeigt), und legen Sie den Wert auf  `DebugProviders`  `SocialConnector`  `DebugProviders` 1.</span><span class="sxs-lookup"><span data-stu-id="d5a18-109">To debug a provider, create a  `DebugProviders` value of type DWORD in the Windows registry under the  `SocialConnector` key (as shown in the following line), and set the  `DebugProviders` value to 1.</span></span> 
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`
  
<span data-ttu-id="d5a18-110">Standardmäßig ist das Anbieterdebubugen deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d5a18-110">By default, provider debugging is off.</span></span> <span data-ttu-id="d5a18-111">Wenn der Wert nicht vorhanden oder vorhanden ist und auf den Wert 0 festgelegt ist, ist das  `DebugProviders` Anbieterdebuding deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d5a18-111">If the  `DebugProviders` value is not present, or it is present and set to a value of 0, provider debugging is turned off.</span></span> 
  
<span data-ttu-id="d5a18-112">Wenn das Anbieterdebuding aktiviert ist, zeigt die OSC ein Benachrichtigungsdialogfeld mit ausführlichen Fehlerinformationen an, wenn ein Fehler auftritt, und überprüft alle XML-Daten des OSC-Anbieters mit dem XML-Schema des OSC-Anbieters.</span><span class="sxs-lookup"><span data-stu-id="d5a18-112">If provider debugging is turned on, the OSC displays an alert dialog box with verbose error information when an error occurs, and validates any OSC provider XML against the OSC provider XML schema.</span></span> <span data-ttu-id="d5a18-113">Basierend auf dem für eine XML-Zeichenfolge angegebenen Namespace wird ein mit OSC 1.0 entwickelter OSC-Anbieter mit der OSC 1.0-Schemadatei OutlookSocialProvider.xsd überprüft.</span><span class="sxs-lookup"><span data-stu-id="d5a18-113">Based on the namespace specified for an XML string, an OSC provider developed by using OSC 1.0 is validated against the OSC 1.0 schema file, OutlookSocialProvider.xsd.</span></span> <span data-ttu-id="d5a18-114">Ein mit OSC 1.1 oder höher entwickelter OSC-Anbieter wird anhand der Schemadatei OutlookSocialProvider_1.1.xsd überprüft.</span><span class="sxs-lookup"><span data-stu-id="d5a18-114">An OSC provider developed by using OSC 1.1 or later is validated against the schema file, OutlookSocialProvider_1.1.xsd.</span></span> <span data-ttu-id="d5a18-115">Wenn Sie den Wert verwenden, wird die Debugwarnung für alle geladenen Anbieter anstelle  `DebugProviders` eines bestimmten Anbieters angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d5a18-115">When you use the  `DebugProviders` value, the debug alert appears for all loaded providers instead of a specific provider.</span></span> 
  
<span data-ttu-id="d5a18-116">Um Debugschaltflächen anzuzeigen, mit deren Hilfe Sie einen Anbieter debuggen können, erstellen Sie in der Windows-Registrierung unter dem Schlüssel einen Wert vom Typ DWORD, und legen Sie den Wert auf  `ShowDebugButtons`  `SocialConnector`  `ShowDebugButtons` 1 fest.</span><span class="sxs-lookup"><span data-stu-id="d5a18-116">To display debug buttons that can help you debug a provider, create a  `ShowDebugButtons` value of type DWORD in the Windows registry under the  `SocialConnector` key, and set the  `ShowDebugButtons` value to 1.</span></span> <span data-ttu-id="d5a18-117">Um die Schaltflächen für die Debugbefehlsleiste auszublenden, legen Sie  `ShowDebugButtons` den Wert auf 0.</span><span class="sxs-lookup"><span data-stu-id="d5a18-117">To hide the debug command bar buttons, set the  `ShowDebugButtons` value to 0.</span></span> 
  
<span data-ttu-id="d5a18-118">Für Outlook 2010 und Clientanwendungen seit Office 2013 werden die Debugschaltflächen auf der Registerkarte **Add-Ins** des Explorer-Menübands angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d5a18-118">For Outlook 2010 and client applications since Office 2013, the debug buttons appear on the **Add-ins** tab of the explorer ribbon.</span></span> <span data-ttu-id="d5a18-119">Für Outlook 2007 und Outlook 2003 werden die Debugschaltflächen in der Standardbefehlsleiste des Outlook-Explorer-Fensters angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d5a18-119">For Outlook 2007 and Outlook 2003, the debug buttons appear on the standard command bar of the Outlook explorer window.</span></span> 
  
<span data-ttu-id="d5a18-120">In der folgenden Tabelle werden die Debugschaltflächen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d5a18-120">The following table describes the debug buttons.</span></span>
  
|<span data-ttu-id="d5a18-121">**Schaltfläche "Debuggen"**</span><span class="sxs-lookup"><span data-stu-id="d5a18-121">**Debug button**</span></span>|<span data-ttu-id="d5a18-122">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="d5a18-122">**Function**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d5a18-123">Synchronisieren von Kontakten</span><span class="sxs-lookup"><span data-stu-id="d5a18-123">Sync Contacts</span></span>  <br/> |<span data-ttu-id="d5a18-124">Bewirkt, dass das OSC den OSC-Anbieter nur nach zwischengespeicherten Kontakten fragt.</span><span class="sxs-lookup"><span data-stu-id="d5a18-124">Causes the OSC to ask the OSC provider for cached contacts only.</span></span>  <br/> |
|<span data-ttu-id="d5a18-125">GAL-Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="d5a18-125">GAL Sync</span></span>  <br/> |<span data-ttu-id="d5a18-126">Bewirkt, dass die OSC Daten aus der globalen Exchange-Adressliste in Outlook-Kontakte auffüllt.</span><span class="sxs-lookup"><span data-stu-id="d5a18-126">Causes the OSC to populate data from the Exchange Global Address List to Outlook contacts.</span></span>  <br/> |
|<span data-ttu-id="d5a18-127">Ungültiger Kategoriecache</span><span class="sxs-lookup"><span data-stu-id="d5a18-127">Invalidate Category Cache</span></span>  <br/> |<span data-ttu-id="d5a18-128">Bewirkt, dass das OSC die Kategorieliste für jeden Speicher neu lädt, wenn der Aktivitätsfeed aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="d5a18-128">Causes the OSC to reload the category list for each store when the activity feed is refreshed.</span></span>  <br/> |
   
## <a name="fiddler"></a><span data-ttu-id="d5a18-129">Fiddler</span><span class="sxs-lookup"><span data-stu-id="d5a18-129">Fiddler</span></span>

<span data-ttu-id="d5a18-130">Fiddler ist ein out-the-Wire-Debugging-Tool, um die API-Aufrufe zu überprüfen, die von Ihrem Anbieter an das soziale Netzwerk gesendet werden, und XML, das vom sozialen Netzwerk an Ihren Anbieter gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="d5a18-130">Fiddler is an over-the-wire debugging tool to check the API calls sent from your provider to the social network, and XML sent by the social network to your provider.</span></span> <span data-ttu-id="d5a18-131">Fiddler steht unter [Fiddler Web Debugging Proxy zum Download zur Verfügung.](https://www.fiddler2.com/fiddler2/version.asp)</span><span class="sxs-lookup"><span data-stu-id="d5a18-131">Fiddler is available for download at [Fiddler Web Debugging Proxy](https://www.fiddler2.com/fiddler2/version.asp).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d5a18-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d5a18-132">See also</span></span>

- [<span data-ttu-id="d5a18-133">Schnelle Schritte zum Entwickeln eines Anbieters</span><span class="sxs-lookup"><span data-stu-id="d5a18-133">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)  
- [<span data-ttu-id="d5a18-134">Synchronisieren von Freunden und Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="d5a18-134">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md) 
- [<span data-ttu-id="d5a18-135">Bewährte Methoden für die Entwicklung eines Anbieters</span><span class="sxs-lookup"><span data-stu-id="d5a18-135">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
- [<span data-ttu-id="d5a18-136">OSC - Typische Aufrufsequenzen</span><span class="sxs-lookup"><span data-stu-id="d5a18-136">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)  
- [<span data-ttu-id="d5a18-137">Entwickeln eines Providers mit dem OSC-XML-Schema</span><span class="sxs-lookup"><span data-stu-id="d5a18-137">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)  
- [<span data-ttu-id="d5a18-138">Vorbereitung der Freigabe eines OSC-Providers</span><span class="sxs-lookup"><span data-stu-id="d5a18-138">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)

