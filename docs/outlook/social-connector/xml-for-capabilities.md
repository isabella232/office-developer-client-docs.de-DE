---
title: XML für „capabilities“
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: edad1223-a55f-4e4a-8e90-3471f2f559ac
description: 'Das Capabilities-Element im XML-Schema (OSC)-Anbieter ermöglicht einen OSC-Anbieter an seine Funktionalität. Eine solche Funktionalität umfasst Folgendes:'
ms.openlocfilehash: 8192c4d559ae656cfc3b12cd8f50f7d4acd5ed5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796084"
---
# <a name="xml-for-capabilities"></a><span data-ttu-id="a7cb7-104">XML für „capabilities“</span><span class="sxs-lookup"><span data-stu-id="a7cb7-104">XML for capabilities</span></span>

<span data-ttu-id="a7cb7-105">Das **Capabilities** -Element im XML-Schema (OSC)-Anbieter ermöglicht einen OSC-Anbieter an seine Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="a7cb7-105">The **capabilities** element in the (OSC) provider XML schema allows an OSC provider to specify its functionality.</span></span> <span data-ttu-id="a7cb7-106">Eine solche Funktionalität umfasst Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a7cb7-106">Such functionality includes the following:</span></span> 
  
- <span data-ttu-id="a7cb7-107">Gibt an, ob der Anbieter abrufen, Zwischenspeichern oder dynamisch Nachschlagen Freunde und Aktivitäten aus dem sozialen Netzwerk unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a7cb7-107">Whether the provider supports getting, caching, or dynamically looking up friends and activities from the social network.</span></span>
    
- <span data-ttu-id="a7cb7-108">Wie die OSC-Benutzeroberflächen für bestimmte Anmeldung angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a7cb7-108">How the OSC should display certain logon user interfaces.</span></span>
    
- <span data-ttu-id="a7cb7-109">Gibt an, ob die OSC formularbasierte Authentifizierung verwenden oder automatisch die für soziale Netzwerke und die Protokolle auf den Benutzer im sozialen Netzwerk konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="a7cb7-109">Whether the OSC should use forms-based authentication or automatically configure the social network and logs on the user on the social network.</span></span>
    
<span data-ttu-id="a7cb7-110">XML-Schema für **Funktionen** ist wichtig, da er den vom Anbieter unterstützten Funktionen an die OSC angegeben.</span><span class="sxs-lookup"><span data-stu-id="a7cb7-110">The XML schema for **capabilities** is critical because it identifies to the OSC the functionality supported by the provider.</span></span> <span data-ttu-id="a7cb7-111">Ein OSC-Anbieter muss die [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) -Methode implementieren, die Zeichenfolge ein _Ergebnis_ zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="a7cb7-111">An OSC provider must implement the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method that returns a  _result_ string.</span></span> <span data-ttu-id="a7cb7-112">Die OSC ruft **ISocialProvider::GetCapabilities** zum Abrufen von Informationen zu den Funktionen des OSC-Anbieters in die _resultierende_ Zeichenfolge, die die XML-Schemadefinition für das **Capabilities** -Element entspricht.</span><span class="sxs-lookup"><span data-stu-id="a7cb7-112">The OSC calls **ISocialProvider::GetCapabilities** to obtain information about the capabilities of the OSC provider in the  _result_ string, which complies with the XML schema definition for the **capabilities** element.</span></span> <span data-ttu-id="a7cb7-113">Diese Informationen kann für nachfolgende Anrufe über den OSC, OSC-Anbieter ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="a7cb7-113">This information enables subsequent calls from the OSC to the OSC provider to operate correctly.</span></span> 
  
<span data-ttu-id="a7cb7-114">Um Funktionen für einen OSC-Anbieter als Output-Parameter der Methode **ISocialProvider::GetCapabilities** angeben, müssen Sie das OSC-Anbieter Erweiterbarkeit XML-Schema entsprechen.</span><span class="sxs-lookup"><span data-stu-id="a7cb7-114">To specify capabilities of an OSC provider as an output parameter of the **ISocialProvider::GetCapabilities** method, you must conform to the OSC provider extensibility XML schema.</span></span> <span data-ttu-id="a7cb7-115">Die folgende Abbildung zeigt die XML-Struktur von **Funktionen** .</span><span class="sxs-lookup"><span data-stu-id="a7cb7-115">The following figure shows the **capabilities** XML structure.</span></span> 
  
<span data-ttu-id="a7cb7-116">**Abbildung 1. \<Funktionen\> XML-Struktur**</span><span class="sxs-lookup"><span data-stu-id="a7cb7-116">**Figure 1. \<capabilities\> XML structure**</span></span>

![Funktionen für XML-Struktur](media/ol14oscref_Specifyingxmlforcapabilities_image1.gif)
  
<span data-ttu-id="a7cb7-118">Eine ausführliche Beschreibung der untergeordneten Elemente des **Capabilities** -Element finden Sie unter [Funktionen XML-Elemente](capabilities-xml-elements.md).</span><span class="sxs-lookup"><span data-stu-id="a7cb7-118">For detailed descriptions of child elements of the **capabilities** element, see [Capabilities XML Elements](capabilities-xml-elements.md).</span></span> <span data-ttu-id="a7cb7-119">Ein Beispiel für XML- **Funktionen** finden Sie unter [Funktionen XML-Beispiel](capabilities-xml-example.md).</span><span class="sxs-lookup"><span data-stu-id="a7cb7-119">For an example of **capabilities** XML, see [Capabilities XML Example](capabilities-xml-example.md).</span></span> <span data-ttu-id="a7cb7-120">Eine vollständige Definition des OSC-Anbieter XML-Schema, welche Elemente sind, erforderlich oder optional, einschließlich finden Sie unter [Outlook Social Connector Provider XML-Schema](outlook-social-connector-provider-xml-schema.md).</span><span class="sxs-lookup"><span data-stu-id="a7cb7-120">For a complete definition of the OSC provider XML schema, including which elements are required or optional, see [Outlook Social Connector Provider XML Schema](outlook-social-connector-provider-xml-schema.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a7cb7-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a7cb7-121">See also</span></span>

- [<span data-ttu-id="a7cb7-122">Funktionen XML-Beispiel</span><span class="sxs-lookup"><span data-stu-id="a7cb7-122">Capabilities XML Example</span></span>](capabilities-xml-example.md)  
- [<span data-ttu-id="a7cb7-123">Synchronisieren von Freunde und Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="a7cb7-123">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)  
- [<span data-ttu-id="a7cb7-124">XML-Code für Freunde</span><span class="sxs-lookup"><span data-stu-id="a7cb7-124">XML for Friends</span></span>](xml-for-friends.md)  
- [<span data-ttu-id="a7cb7-125">XML-Code für Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="a7cb7-125">XML for Activities</span></span>](xml-for-activities.md)
- [<span data-ttu-id="a7cb7-126">Entwickeln eines Providers mit dem OSC-XML-Schema</span><span class="sxs-lookup"><span data-stu-id="a7cb7-126">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

