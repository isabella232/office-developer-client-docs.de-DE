---
title: Sämtliche Gateway-Eigenschaften
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3a51ee7e-d030-4f04-915b-ff8bd351207d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 07c215511f010741e69c08c184df0ca3ce461e13
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583617"
---
# <a name="gateway-mappable-properties"></a><span data-ttu-id="00c0e-103">Sämtliche Gateway-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="00c0e-103">Gateway mappable properties</span></span>

<span data-ttu-id="00c0e-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00c0e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00c0e-105">Gateway-sämtliche Eigenschaften sind, die Übersetzung beim Senden von einer messaging-Domäne in eine andere erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="00c0e-105">Gateway-mappable properties are properties that may require translation when sent from one messaging domain to another.</span></span> <span data-ttu-id="00c0e-106">Zum Zuordnen geeignete Gateway des MAPI-Eigenschaften aktivieren Nachrichten an Informationen enthalten, die ein Gateway aus, um sicherzustellen, dass das Ziel messaging-System verwendet ordnungsgemäß erfordert.</span><span class="sxs-lookup"><span data-stu-id="00c0e-106">MAPI's gateway-mappable properties enable messages to include information that requires a gateway to ensure the destination messaging system uses it properly.</span></span> <span data-ttu-id="00c0e-107">Obwohl Entwickler Gateway nicht erforderlich sind, diese Übersetzungsfunktion bereitstellen, sollten sie Gateway sämtliche Eigenschaften als Gelegenheit zur Behandlung von Inhalt zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="00c0e-107">Although gateway developers are not required to provide this translation capability, they should consider gateway-mappable properties as an opportunity to improve handling of message content.</span></span>
  
<span data-ttu-id="00c0e-108">MAPI gibt fünf Typen von Gateways sämtliche Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="00c0e-108">MAPI specifies five types of gateway-mappable properties:</span></span>
  
- <span data-ttu-id="00c0e-109">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="00c0e-109">Display name</span></span>
    
- <span data-ttu-id="00c0e-110">E-Mail-Adresse</span><span class="sxs-lookup"><span data-stu-id="00c0e-110">Email address</span></span>
    
- <span data-ttu-id="00c0e-111">E-Mail-Typ</span><span class="sxs-lookup"><span data-stu-id="00c0e-111">Email type</span></span>
    
- <span data-ttu-id="00c0e-112">Eintrags-ID</span><span class="sxs-lookup"><span data-stu-id="00c0e-112">Entry identifier</span></span>
    
- <span data-ttu-id="00c0e-113">Suchen-Taste</span><span class="sxs-lookup"><span data-stu-id="00c0e-113">Search key</span></span>
    
<span data-ttu-id="00c0e-114">Dies ist der Satz von reagieren auf Eigenschaften, die Empfänger, Absender, Berichtempfänger und delegierte Absender und Empfänger zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="00c0e-114">This is the set of addressing properties that are associated with recipients, senders, report recipients, and delegated senders and recipients.</span></span> <span data-ttu-id="00c0e-115">Gibt an, mit denen Ihre Client diese Eigenschaften zu definieren, sodass ein Gateway sie speziell behandelt, MAPI eine Benennungskonvention von benannten Eigenschaften und Eigenschaftensätze.</span><span class="sxs-lookup"><span data-stu-id="00c0e-115">To help your client define these properties so that a gateway handles them specially, MAPI specifies a naming convention using named properties and property sets.</span></span> <span data-ttu-id="00c0e-116">Fünf Eigenschaftensätze vorhanden benannte Eigenschaften, die Adressierung Eigenschaften enthalten, die zugeordnet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="00c0e-116">Five property sets exist to hold named properties, the addressing properties that require mapping.</span></span> <span data-ttu-id="00c0e-117">Es gibt eine Eigenschaft für jeden Typ, der sämtliche-Eigenschaft festgelegt.</span><span class="sxs-lookup"><span data-stu-id="00c0e-117">There is one property set for each type of mappable property.</span></span> <span data-ttu-id="00c0e-118">Die Eigenschaftensätze, die diese benannte reagieren auf Eigenschaften enthalten sind wie folgt.</span><span class="sxs-lookup"><span data-stu-id="00c0e-118">The property sets that will hold these named addressing properties are as follows.</span></span>
  
|<span data-ttu-id="00c0e-119">**Eigenschaftensatz**</span><span class="sxs-lookup"><span data-stu-id="00c0e-119">**Property set**</span></span>|<span data-ttu-id="00c0e-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="00c0e-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="00c0e-121">PS_ROUTING_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="00c0e-121">PS_ROUTING_DISPLAY_NAME</span></span>  <br/> |<span data-ttu-id="00c0e-122">Enthält Zeichenfolgeneigenschaften als Anzeigenamen verwendet.</span><span class="sxs-lookup"><span data-stu-id="00c0e-122">Contains string properties used as display names.</span></span>  <br/> |
|<span data-ttu-id="00c0e-123">PS_ROUTING_EMAIL_ADDRESSES</span><span class="sxs-lookup"><span data-stu-id="00c0e-123">PS_ROUTING_EMAIL_ADDRESSES</span></span>  <br/> |<span data-ttu-id="00c0e-124">Enthält Zeichenfolgeneigenschaften als e-Mail-Adressen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="00c0e-124">Contains string properties used as email addresses.</span></span>  <br/> |
|<span data-ttu-id="00c0e-125">PS_ROUTING_ADDRTYPE</span><span class="sxs-lookup"><span data-stu-id="00c0e-125">PS_ROUTING_ADDRTYPE</span></span>  <br/> |<span data-ttu-id="00c0e-126">Enthält Zeichenfolgeneigenschaften als e-Mail-Adresstypen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="00c0e-126">Contains string properties used as email address types.</span></span>  <br/> |
|<span data-ttu-id="00c0e-127">PS_ROUTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="00c0e-127">PS_ROUTING_ENTRYID</span></span>  <br/> |<span data-ttu-id="00c0e-128">Enthält binäre Eigenschaften als langfristige-Eintragsbezeichner verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="00c0e-128">Contains binary properties used as long-term entry identifiers.</span></span>  <br/> |
|<span data-ttu-id="00c0e-129">PS_ROUTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="00c0e-129">PS_ROUTING_SEARCH_KEY</span></span>  <br/> |<span data-ttu-id="00c0e-130">Binäre Eigenschaften, die als Suche Schlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="00c0e-130">Contains binary properties used as search keys.</span></span>  <br/> |
   

