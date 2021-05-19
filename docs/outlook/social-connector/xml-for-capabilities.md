---
title: XML für „capabilities“
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: edad1223-a55f-4e4a-8e90-3471f2f559ac
description: 'Das Capabilities-Element im (OSC)-Anbieter-XML-Schema ermöglicht es einem OSC-Anbieter, seine Funktionalität anzugeben. Diese Funktionalität umfasst Folgendes:'
ms.openlocfilehash: ff6abbd4d99eb542a11e3d64a2015fc0585fca79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435005"
---
# <a name="xml-for-capabilities"></a><span data-ttu-id="241e2-104">XML für „capabilities“</span><span class="sxs-lookup"><span data-stu-id="241e2-104">XML for capabilities</span></span>

<span data-ttu-id="241e2-105">Das **Capabilities-Element** im (OSC)-Anbieter-XML-Schema ermöglicht es einem OSC-Anbieter, seine Funktionalität anzugeben.</span><span class="sxs-lookup"><span data-stu-id="241e2-105">The **capabilities** element in the (OSC) provider XML schema allows an OSC provider to specify its functionality.</span></span> <span data-ttu-id="241e2-106">Diese Funktionalität umfasst Folgendes:</span><span class="sxs-lookup"><span data-stu-id="241e2-106">Such functionality includes the following:</span></span> 
  
- <span data-ttu-id="241e2-107">Ob der Anbieter das Abrufen, Zwischenspeichern oder dynamische Suchen von Freunden und Aktivitäten aus dem sozialen Netzwerk unterstützt.</span><span class="sxs-lookup"><span data-stu-id="241e2-107">Whether the provider supports getting, caching, or dynamically looking up friends and activities from the social network.</span></span>
    
- <span data-ttu-id="241e2-108">Wie das OSC bestimmte Anmeldebenutzerschnittstellen anzeigen soll.</span><span class="sxs-lookup"><span data-stu-id="241e2-108">How the OSC should display certain logon user interfaces.</span></span>
    
- <span data-ttu-id="241e2-109">Gibt an, ob das OSC die formularbasierte Authentifizierung verwenden oder das soziale Netzwerk automatisch konfigurieren und sich beim Benutzer im sozialen Netzwerk anmeldet.</span><span class="sxs-lookup"><span data-stu-id="241e2-109">Whether the OSC should use forms-based authentication or automatically configure the social network and logs on the user on the social network.</span></span>
    
<span data-ttu-id="241e2-110">Das XML-Schema für **Funktionen** ist von entscheidender Bedeutung, da es für das OSC die vom Anbieter unterstützte Funktionalität identifiziert.</span><span class="sxs-lookup"><span data-stu-id="241e2-110">The XML schema for **capabilities** is critical because it identifies to the OSC the functionality supported by the provider.</span></span> <span data-ttu-id="241e2-111">Ein OSC-Anbieter muss die [ISocialProvider::GetCapabilities-Methode](isocialprovider-getcapabilities.md) implementieren, die eine _Ergebniszeichenfolge zurückgibt._</span><span class="sxs-lookup"><span data-stu-id="241e2-111">An OSC provider must implement the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method that returns a  _result_ string.</span></span> <span data-ttu-id="241e2-112">Das OSC ruft **ISocialProvider::GetCapabilities** auf, um Informationen zu  den Funktionen des OSC-Anbieters in der Ergebniszeichenfolge zu erhalten, die der XML-Schemadefinition für das **Capabilities-Element** entspricht.</span><span class="sxs-lookup"><span data-stu-id="241e2-112">The OSC calls **ISocialProvider::GetCapabilities** to obtain information about the capabilities of the OSC provider in the  _result_ string, which complies with the XML schema definition for the **capabilities** element.</span></span> <span data-ttu-id="241e2-113">Mit diesen Informationen können nachfolgende Aufrufe des Betriebssystems an den OSC-Anbieter ordnungsgemäß ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="241e2-113">This information enables subsequent calls from the OSC to the OSC provider to operate correctly.</span></span> 
  
<span data-ttu-id="241e2-114">Um Funktionen eines OSC-Anbieters als Ausgabeparameter der **ISocialProvider::GetCapabilities-Methode** anzugeben, müssen Sie das XML-Schema für die Erweiterbarkeit des OSC-Anbieters erfüllen.</span><span class="sxs-lookup"><span data-stu-id="241e2-114">To specify capabilities of an OSC provider as an output parameter of the **ISocialProvider::GetCapabilities** method, you must conform to the OSC provider extensibility XML schema.</span></span> <span data-ttu-id="241e2-115">Die folgende Abbildung zeigt die **XML-Struktur der Funktionen.**</span><span class="sxs-lookup"><span data-stu-id="241e2-115">The following figure shows the **capabilities** XML structure.</span></span> 
  
<span data-ttu-id="241e2-116">**Abbildung 1. \<funktionen \> XML-Struktur**</span><span class="sxs-lookup"><span data-stu-id="241e2-116">**Figure 1. \<capabilities\> XML structure**</span></span>

![Funktionen für XML-Struktur](media/ol14oscref_Specifyingxmlforcapabilities_image1.gif)
  
<span data-ttu-id="241e2-118">Ausführliche Beschreibungen untergeordneter Elemente des **Capabilities-Elements** finden Sie unter [Capabilities XML Elements](capabilities-xml-elements.md).</span><span class="sxs-lookup"><span data-stu-id="241e2-118">For detailed descriptions of child elements of the **capabilities** element, see [Capabilities XML Elements](capabilities-xml-elements.md).</span></span> <span data-ttu-id="241e2-119">Ein Beispiel für **xml-Funktionen** finden Sie unter [Capabilities XML Example](capabilities-xml-example.md).</span><span class="sxs-lookup"><span data-stu-id="241e2-119">For an example of **capabilities** XML, see [Capabilities XML Example](capabilities-xml-example.md).</span></span> <span data-ttu-id="241e2-120">Eine vollständige Definition des XML-Schemas des OSC-Anbieters, einschließlich der erforderlichen oder optionalen Elemente, finden Sie unter [Outlook Social Connector Provider XML Schema](outlook-social-connector-provider-xml-schema.md).</span><span class="sxs-lookup"><span data-stu-id="241e2-120">For a complete definition of the OSC provider XML schema, including which elements are required or optional, see [Outlook Social Connector Provider XML Schema](outlook-social-connector-provider-xml-schema.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="241e2-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="241e2-121">See also</span></span>

- [<span data-ttu-id="241e2-122">Capabilities XML(Beispiel)</span><span class="sxs-lookup"><span data-stu-id="241e2-122">Capabilities XML Example</span></span>](capabilities-xml-example.md)  
- [<span data-ttu-id="241e2-123">Synchronisieren von Freunden und Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="241e2-123">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)  
- [<span data-ttu-id="241e2-124">XML für Freunde</span><span class="sxs-lookup"><span data-stu-id="241e2-124">XML for Friends</span></span>](xml-for-friends.md)  
- [<span data-ttu-id="241e2-125">XML für Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="241e2-125">XML for Activities</span></span>](xml-for-activities.md)
- [<span data-ttu-id="241e2-126">Entwickeln eines Providers mit dem OSC-XML-Schema</span><span class="sxs-lookup"><span data-stu-id="241e2-126">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

