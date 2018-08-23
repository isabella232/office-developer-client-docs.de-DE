---
title: Eigenschaftennamen und Eigenschaftensätze
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cb216f5c-c965-4372-a15b-82090a410266
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0272464d9a397f169b27aa15c80a17b49a3e9977
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571829"
---
# <a name="property-names-and-property-sets"></a><span data-ttu-id="37d0b-103">Eigenschaftennamen und Eigenschaftensätze</span><span class="sxs-lookup"><span data-stu-id="37d0b-103">Property Names and Property Sets</span></span>

  
  
<span data-ttu-id="37d0b-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="37d0b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="37d0b-105">Der Name jeder benannten Eigenschaft besteht aus zwei Teilen:</span><span class="sxs-lookup"><span data-stu-id="37d0b-105">The name of every named property has two parts:</span></span>
  
- <span data-ttu-id="37d0b-106">Einen global eindeutigen Bezeichner oder um eine GUID, die einen Eigenschaftensatz angibt.</span><span class="sxs-lookup"><span data-stu-id="37d0b-106">A globally unique identifier, or GUID, that specifies a property set.</span></span>
    
- <span data-ttu-id="37d0b-107">Eine Unicode-Zeichenfolge oder eine 32-Bit-numerischen Wert.</span><span class="sxs-lookup"><span data-stu-id="37d0b-107">A Unicode character string or 32-bit numeric value.</span></span> 
    
<span data-ttu-id="37d0b-108">Namen der benannten Eigenschaften werden durch eine [MAPINAMEID](mapinameid.md) Struktur beschrieben.</span><span class="sxs-lookup"><span data-stu-id="37d0b-108">Names of named properties are described using a [MAPINAMEID](mapinameid.md) structure.</span></span> <span data-ttu-id="37d0b-109">Diese Struktur enthält ein Eigenschaft Set-Element, ein Element zum Angeben des Namens im Format numerischen oder Zeichenfolgenwerten und Mitglied zum Identifizieren, welches Format verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="37d0b-109">This structure contains a property set member, a member for specifying the name in either numeric or string format, and a member for identifying which format is used.</span></span> <span data-ttu-id="37d0b-110">Da Eigenschaftensatzes Teil der Name der Eigenschaft ist, ist nicht optional.</span><span class="sxs-lookup"><span data-stu-id="37d0b-110">Because the property set is part of the property's name, it is not optional.</span></span> <span data-ttu-id="37d0b-111">MAPI hat mehrere Eigenschaftensätze für die Verwendung durch Clients und Dienstanbieter definiert, aber wenn ein vorhandene Eigenschaftensatz nicht geeignet ist, kann ein neuen Eigenschaftensatz definiert werden.</span><span class="sxs-lookup"><span data-stu-id="37d0b-111">MAPI has defined several property sets for use by clients and service providers, but if an existing property set is inappropriate, a new property set can be defined.</span></span> <span data-ttu-id="37d0b-112">Clients und Dienstanbieter können ihre eigenen Eigenschaftensätze definieren, indem [CoCreateGUID](http://msdn.microsoft.com/en-us/library/ms688568.aspx) -Funktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="37d0b-112">Clients and service providers can define their own property sets by calling [CoCreateGUID](http://msdn.microsoft.com/en-us/library/ms688568.aspx) function.</span></span> <span data-ttu-id="37d0b-113">In der Regel werden die folgenden Eigenschaftensätze für benutzerdefinierter Clientanwendungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="37d0b-113">Typically these property sets are created for custom client applications.</span></span> 
  
<span data-ttu-id="37d0b-114">MAPI Eigenschaftensätze werden durch die folgenden Konstanten dargestellt:</span><span class="sxs-lookup"><span data-stu-id="37d0b-114">MAPI's property sets are represented by the following constants:</span></span>
  
<span data-ttu-id="37d0b-115">PS_MAPI</span><span class="sxs-lookup"><span data-stu-id="37d0b-115">PS_MAPI</span></span>
  
<span data-ttu-id="37d0b-116">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="37d0b-116">PS_PUBLIC_STRINGS</span></span>
  
<span data-ttu-id="37d0b-117">PS_ROUTING_EMAIL_ADDRESSES</span><span class="sxs-lookup"><span data-stu-id="37d0b-117">PS_ROUTING_EMAIL_ADDRESSES</span></span>
  
<span data-ttu-id="37d0b-118">PS_ROUTING_ADDRTYPE</span><span class="sxs-lookup"><span data-stu-id="37d0b-118">PS_ROUTING_ADDRTYPE</span></span>
  
<span data-ttu-id="37d0b-119">PS_ROUTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="37d0b-119">PS_ROUTING_SEARCH_KEY</span></span>
  
<span data-ttu-id="37d0b-120">PS_ROUTING_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="37d0b-120">PS_ROUTING_DISPLAY_NAME</span></span>
  
<span data-ttu-id="37d0b-121">PS_ROUTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="37d0b-121">PS_ROUTING_ENTRYID</span></span>
  
<span data-ttu-id="37d0b-122">Der Eigenschaftensatz PS_MAPI ist reserviert. Es wird von Dienstanbietern verwendet, um Namen für Eigenschaften mit Bezeichnern unterhalb des Bereichs für die benannte Eigenschaft zu generieren.</span><span class="sxs-lookup"><span data-stu-id="37d0b-122">The PS_MAPI property set is reserved; it is used by service providers to generate names for properties with identifiers below the named property range.</span></span> <span data-ttu-id="37d0b-123">Die PS_PUBLIC_STRINGS-Eigenschaft festgelegt wird von Clients für benannte Eigenschaften der IPM-Nachrichten verwendet.</span><span class="sxs-lookup"><span data-stu-id="37d0b-123">The PS_PUBLIC_STRINGS property set is used by clients for named properties of IPM messages.</span></span> <span data-ttu-id="37d0b-124">Da benannte Eigenschaften im Eigenschaftensatz PS_PUBLIC_STRINGS angezeigt in einer Client-Benutzeroberfläche, nicht sichtbare Nachrichten wie erstellen, die die Nachrichtenklasse IPK gehören vermeiden, sollten benannte Eigenschaften diese Eigenschaft festgelegt.</span><span class="sxs-lookup"><span data-stu-id="37d0b-124">Because named properties in the PS_PUBLIC_STRINGS property set appear in a client's user interface, nonvisible messages such as those that belong to the IPC message class should avoid creating named properties with this property set.</span></span> <span data-ttu-id="37d0b-125">In diesem Fall sollten sie Eigenschaften in der Nachricht Klasse-spezifischen Bereich 0x6800 über 0x7FFF erstellen.</span><span class="sxs-lookup"><span data-stu-id="37d0b-125">Instead, they should create properties in the message class-specific range, 0x6800 through 0x7FFF.</span></span>
  
<span data-ttu-id="37d0b-126">Die anderen Eigenschaftensätze halten benannten eigenschaftenauflistung Empfänger an, die in der Regel Mitglieder einer Verteilerliste sind.</span><span class="sxs-lookup"><span data-stu-id="37d0b-126">The other property sets hold named properties describing recipients that are typically members of a routing list.</span></span> <span data-ttu-id="37d0b-127">Enthält die gleiche Art von Informationen als die Eigenschaften, die Empfängerliste Eigenschaften zugeordnet sind, werden Eigenschaften in dieser Eigenschaftensätze Gateways verständlich Zuordnung für ein Ziel Messagingsystem erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="37d0b-127">Containing the same type of information as the properties that are associated with recipient list properties, properties in these property sets are understood by gateways to require mapping for a target messaging system.</span></span> <span data-ttu-id="37d0b-128">Da fünf Arten von Informationen für die Beschreibung der Eigenschaften vorhanden sind, hat fünf verschiedenen Eigenschaftensätze MAPI definiert ist.</span><span class="sxs-lookup"><span data-stu-id="37d0b-128">Because there are five types of information for describing properties, MAPI has defined five different property sets.</span></span> <span data-ttu-id="37d0b-129">Ein Client sendet, dass eine Nachricht, die eine Adresse und den Adresstyp für Membern Liste routing umfassen muss eine benannte Eigenschaft für jedes Mitglied in der PS_ROUTING_EMAIL_ADDRESSES und PS_ROUTING_ADDRTYPE-Eigenschaft weist festgelegt.</span><span class="sxs-lookup"><span data-stu-id="37d0b-129">A client sending a message that must include an address and address type for its routing list members assigns a named property for each member in the PS_ROUTING_EMAIL_ADDRESSES and PS_ROUTING_ADDRTYPE property sets.</span></span> <span data-ttu-id="37d0b-130">Dadurch wird sichergestellt, dass die Adresse und den Adresstyp verwendbar, wenn an einem fremden Messagingsystem gesendet bleiben.</span><span class="sxs-lookup"><span data-stu-id="37d0b-130">This ensures that the address and address type remain viable when sent to a foreign messaging system.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="37d0b-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37d0b-131">See also</span></span>



[<span data-ttu-id="37d0b-132">Benannte Eigenschaften MAPI</span><span class="sxs-lookup"><span data-stu-id="37d0b-132">MAPI Named Properties</span></span>](mapi-named-properties.md)

