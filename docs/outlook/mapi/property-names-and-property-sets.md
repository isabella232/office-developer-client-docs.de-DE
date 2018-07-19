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
ms.openlocfilehash: c586d70054542e8d20c90a8caceafabbbb408de8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795354"
---
# <a name="property-names-and-property-sets"></a><span data-ttu-id="85dac-103">Eigenschaftennamen und Eigenschaftensätze</span><span class="sxs-lookup"><span data-stu-id="85dac-103">Property Names and Property Sets</span></span>

  
  
<span data-ttu-id="85dac-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="85dac-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="85dac-105">Der Name jeder benannten Eigenschaft besteht aus zwei Teilen:</span><span class="sxs-lookup"><span data-stu-id="85dac-105">The name of every named property has two parts:</span></span>
  
- <span data-ttu-id="85dac-106">Einen global eindeutigen Bezeichner oder um eine GUID, die einen Eigenschaftensatz angibt.</span><span class="sxs-lookup"><span data-stu-id="85dac-106">A globally unique identifier, or GUID, that specifies a property set.</span></span>
    
- <span data-ttu-id="85dac-107">Eine Unicode-Zeichenfolge oder eine 32-Bit-numerischen Wert.</span><span class="sxs-lookup"><span data-stu-id="85dac-107">A Unicode character string or 32-bit numeric value.</span></span> 
    
<span data-ttu-id="85dac-108">Namen der benannten Eigenschaften werden durch eine [MAPINAMEID](mapinameid.md) Struktur beschrieben.</span><span class="sxs-lookup"><span data-stu-id="85dac-108">Names of named properties are described using a [MAPINAMEID](mapinameid.md) structure.</span></span> <span data-ttu-id="85dac-109">Diese Struktur enthält ein Eigenschaft Set-Element, ein Element zum Angeben des Namens im Format numerischen oder Zeichenfolgenwerten und Mitglied zum Identifizieren, welches Format verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="85dac-109">This structure contains a property set member, a member for specifying the name in either numeric or string format, and a member for identifying which format is used.</span></span> <span data-ttu-id="85dac-110">Da Eigenschaftensatzes Teil der Name der Eigenschaft ist, ist nicht optional.</span><span class="sxs-lookup"><span data-stu-id="85dac-110">Because the property set is part of the property's name, it is not optional.</span></span> <span data-ttu-id="85dac-111">MAPI hat mehrere Eigenschaftensätze für die Verwendung durch Clients und Dienstanbieter definiert, aber wenn ein vorhandene Eigenschaftensatz nicht geeignet ist, kann ein neuen Eigenschaftensatz definiert werden.</span><span class="sxs-lookup"><span data-stu-id="85dac-111">MAPI has defined several property sets for use by clients and service providers, but if an existing property set is inappropriate, a new property set can be defined.</span></span> <span data-ttu-id="85dac-112">Clients und Dienstanbieter können ihre eigenen Eigenschaftensätze definieren, indem [CoCreateGUID](http://msdn.microsoft.com/de-de/library/ms688568.aspx) -Funktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="85dac-112">Clients and service providers can define their own property sets by calling [CoCreateGUID](http://msdn.microsoft.com/de-de/library/ms688568.aspx) function.</span></span> <span data-ttu-id="85dac-113">In der Regel werden die folgenden Eigenschaftensätze für benutzerdefinierter Clientanwendungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="85dac-113">Typically these property sets are created for custom client applications.</span></span> 
  
<span data-ttu-id="85dac-114">MAPI Eigenschaftensätze werden durch die folgenden Konstanten dargestellt:</span><span class="sxs-lookup"><span data-stu-id="85dac-114">MAPI's property sets are represented by the following constants:</span></span>
  
<span data-ttu-id="85dac-115">PS_MAPI</span><span class="sxs-lookup"><span data-stu-id="85dac-115">PS_MAPI</span></span>
  
<span data-ttu-id="85dac-116">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="85dac-116">PS_PUBLIC_STRINGS</span></span>
  
<span data-ttu-id="85dac-117">PS_ROUTING_EMAIL_ADDRESSES</span><span class="sxs-lookup"><span data-stu-id="85dac-117">PS_ROUTING_EMAIL_ADDRESSES</span></span>
  
<span data-ttu-id="85dac-118">PS_ROUTING_ADDRTYPE</span><span class="sxs-lookup"><span data-stu-id="85dac-118">PS_ROUTING_ADDRTYPE</span></span>
  
<span data-ttu-id="85dac-119">PS_ROUTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="85dac-119">PS_ROUTING_SEARCH_KEY</span></span>
  
<span data-ttu-id="85dac-120">PS_ROUTING_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="85dac-120">PS_ROUTING_DISPLAY_NAME</span></span>
  
<span data-ttu-id="85dac-121">PS_ROUTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="85dac-121">PS_ROUTING_ENTRYID</span></span>
  
<span data-ttu-id="85dac-122">Der Eigenschaftensatz PS_MAPI ist reserviert. Es wird von Dienstanbietern verwendet, um Namen für Eigenschaften mit Bezeichnern unterhalb des Bereichs für die benannte Eigenschaft zu generieren.</span><span class="sxs-lookup"><span data-stu-id="85dac-122">The PS_MAPI property set is reserved; it is used by service providers to generate names for properties with identifiers below the named property range.</span></span> <span data-ttu-id="85dac-123">Die PS_PUBLIC_STRINGS-Eigenschaft festgelegt wird von Clients für benannte Eigenschaften der IPM-Nachrichten verwendet.</span><span class="sxs-lookup"><span data-stu-id="85dac-123">The PS_PUBLIC_STRINGS property set is used by clients for named properties of IPM messages.</span></span> <span data-ttu-id="85dac-124">Da benannte Eigenschaften im Eigenschaftensatz PS_PUBLIC_STRINGS angezeigt in einer Client-Benutzeroberfläche, nicht sichtbare Nachrichten wie erstellen, die die Nachrichtenklasse IPK gehören vermeiden, sollten benannte Eigenschaften diese Eigenschaft festgelegt.</span><span class="sxs-lookup"><span data-stu-id="85dac-124">Because named properties in the PS_PUBLIC_STRINGS property set appear in a client's user interface, nonvisible messages such as those that belong to the IPC message class should avoid creating named properties with this property set.</span></span> <span data-ttu-id="85dac-125">In diesem Fall sollten sie Eigenschaften in der Nachricht Klasse-spezifischen Bereich 0x6800 über 0x7FFF erstellen.</span><span class="sxs-lookup"><span data-stu-id="85dac-125">Instead, they should create properties in the message class-specific range, 0x6800 through 0x7FFF.</span></span>
  
<span data-ttu-id="85dac-126">Die anderen Eigenschaftensätze halten benannten eigenschaftenauflistung Empfänger an, die in der Regel Mitglieder einer Verteilerliste sind.</span><span class="sxs-lookup"><span data-stu-id="85dac-126">The other property sets hold named properties describing recipients that are typically members of a routing list.</span></span> <span data-ttu-id="85dac-127">Enthält die gleiche Art von Informationen als die Eigenschaften, die Empfängerliste Eigenschaften zugeordnet sind, werden Eigenschaften in dieser Eigenschaftensätze Gateways verständlich Zuordnung für ein Ziel Messagingsystem erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="85dac-127">Containing the same type of information as the properties that are associated with recipient list properties, properties in these property sets are understood by gateways to require mapping for a target messaging system.</span></span> <span data-ttu-id="85dac-128">Da fünf Arten von Informationen für die Beschreibung der Eigenschaften vorhanden sind, hat fünf verschiedenen Eigenschaftensätze MAPI definiert ist.</span><span class="sxs-lookup"><span data-stu-id="85dac-128">Because there are five types of information for describing properties, MAPI has defined five different property sets.</span></span> <span data-ttu-id="85dac-129">Ein Client sendet, dass eine Nachricht, die eine Adresse und den Adresstyp für Membern Liste routing umfassen muss eine benannte Eigenschaft für jedes Mitglied in der PS_ROUTING_EMAIL_ADDRESSES und PS_ROUTING_ADDRTYPE-Eigenschaft weist festgelegt.</span><span class="sxs-lookup"><span data-stu-id="85dac-129">A client sending a message that must include an address and address type for its routing list members assigns a named property for each member in the PS_ROUTING_EMAIL_ADDRESSES and PS_ROUTING_ADDRTYPE property sets.</span></span> <span data-ttu-id="85dac-130">Dadurch wird sichergestellt, dass die Adresse und den Adresstyp verwendbar, wenn an einem fremden Messagingsystem gesendet bleiben.</span><span class="sxs-lookup"><span data-stu-id="85dac-130">This ensures that the address and address type remain viable when sent to a foreign messaging system.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="85dac-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85dac-131">See also</span></span>



[<span data-ttu-id="85dac-132">Benannte Eigenschaften MAPI</span><span class="sxs-lookup"><span data-stu-id="85dac-132">MAPI Named Properties</span></span>](mapi-named-properties.md)

