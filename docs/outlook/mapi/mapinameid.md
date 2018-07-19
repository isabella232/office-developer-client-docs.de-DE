---
title: MAPINAMEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPINAMEID
api_type:
- COM
ms.assetid: 9a92e9cd-8282-4cf0-93af-4089b3763594
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c3a21e8a6e69cae9d8b757a60fe56d63e079b3ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793121"
---
# <a name="mapinameid"></a><span data-ttu-id="3f1ca-103">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="3f1ca-103">MAPINAMEID</span></span>

  
  
<span data-ttu-id="3f1ca-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3f1ca-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3f1ca-105">Beschreibt eine benannte Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="3f1ca-105">Describes a named property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3f1ca-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="3f1ca-106">Header file:</span></span>  <br/> |<span data-ttu-id="3f1ca-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3f1ca-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _MAPINAMEID
{
  LPGUID lpguid;
  ULONG ulKind;
  union
  {
    LONG lID;
    LPWSTR lpwstrName;
  } Kind;
} MAPINAMEID, FAR *LPMAPINAMEID;

```

## <a name="members"></a><span data-ttu-id="3f1ca-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="3f1ca-108">Members</span></span>

 <span data-ttu-id="3f1ca-109">**x lpguid**</span><span class="sxs-lookup"><span data-stu-id="3f1ca-109">**lpguid**</span></span>
  
> <span data-ttu-id="3f1ca-110">Zeiger auf eine [GUID](guid.md) -Struktur definieren eine bestimmte Eigenschaft festgelegt. Dieser Member darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="3f1ca-110">Pointer to a [GUID](guid.md) structure defining a particular property set; this member cannot be NULL.</span></span> <span data-ttu-id="3f1ca-111">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="3f1ca-111">Valid values are as follows:</span></span> 
    
<span data-ttu-id="3f1ca-112">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="3f1ca-112">PS_PUBLIC_STRINGS</span></span>
  
> 
    
<span data-ttu-id="3f1ca-113">PS_MAPI</span><span class="sxs-lookup"><span data-stu-id="3f1ca-113">PS_MAPI</span></span>
  
> 
    
<span data-ttu-id="3f1ca-114">Ein Client definierten Wert</span><span class="sxs-lookup"><span data-stu-id="3f1ca-114">A client-defined value</span></span>
  
> 
    
 <span data-ttu-id="3f1ca-115">**ulKind**</span><span class="sxs-lookup"><span data-stu-id="3f1ca-115">**ulKind**</span></span>
  
> <span data-ttu-id="3f1ca-116">Wert, der den Typ von Wert in die **Kind** -Member beschreibt.</span><span class="sxs-lookup"><span data-stu-id="3f1ca-116">Value describing the type of value in the **Kind** member.</span></span> <span data-ttu-id="3f1ca-117">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="3f1ca-117">Valid values are as follows:</span></span> 
    
<span data-ttu-id="3f1ca-118">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="3f1ca-118">MNID_ID</span></span> 
  
> <span data-ttu-id="3f1ca-119">Der **Kind** -Member enthält einen Integer-Wert, der Name der Eigenschaft darstellt.</span><span class="sxs-lookup"><span data-stu-id="3f1ca-119">The **Kind** member contains an integer value that represents the property name.</span></span> 
    
<span data-ttu-id="3f1ca-120">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="3f1ca-120">MNID_STRING</span></span> 
  
> <span data-ttu-id="3f1ca-121">Der **Kind** -Member enthält eine Unicode-Zeichenfolge, die der Name der Eigenschaft darstellt.</span><span class="sxs-lookup"><span data-stu-id="3f1ca-121">The **Kind** member contains a Unicode character string representing the property name.</span></span> 
    
 <span data-ttu-id="3f1ca-122">**Kind**</span><span class="sxs-lookup"><span data-stu-id="3f1ca-122">**Kind**</span></span>
  
> <span data-ttu-id="3f1ca-123">Beschreibung des Namens, der die benannte Eigenschaft Union.</span><span class="sxs-lookup"><span data-stu-id="3f1ca-123">Union describing the name of the named property.</span></span> <span data-ttu-id="3f1ca-124">Der Name kann einen ganzzahligen Wert, der in **Abdeckung**, gespeichert oder ein Unicode-Zeichenfolge, die in **LpwstrName**gespeichert sein.</span><span class="sxs-lookup"><span data-stu-id="3f1ca-124">The name can be either an integer value, stored in **lID**, or a Unicode character string, stored in **lpwstrName**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3f1ca-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3f1ca-125">Remarks</span></span>

<span data-ttu-id="3f1ca-126">Die Struktur **MAPINAMEID** wird verwendet, um benannte Eigenschaften Eigenschaften zu beschreiben, die über 0 x 8000 Bezeichner aufweisen.</span><span class="sxs-lookup"><span data-stu-id="3f1ca-126">The **MAPINAMEID** structure is used to describe named properties properties that have identifiers over 0x8000.</span></span> <span data-ttu-id="3f1ca-127">Ein Eigenschaftensatz stellen einen wichtigen Bestandteil einer benannten Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="3f1ca-127">A property set is an important part a named property.</span></span> <span data-ttu-id="3f1ca-128">Beispielsweise sind PS_PUBLIC_STRINGS oder PS_ROUTING_ADDRTYPE Eigenschaftensätze MAPI definiert.</span><span class="sxs-lookup"><span data-stu-id="3f1ca-128">For example PS_PUBLIC_STRINGS or PS_ROUTING_ADDRTYPE are property sets defined by MAPI.</span></span> 
  
<span data-ttu-id="3f1ca-129">Benannte Eigenschaften ermöglichen Clients zum Definieren von benutzerdefinierter Eigenschaften in einem größeren Namespace als im Bereich Bezeichner definierte MAPI Eigenschaft verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="3f1ca-129">Named properties enable clients to define custom properties in a larger namespace than is available in the MAPI-defined property identifier range.</span></span> <span data-ttu-id="3f1ca-130">Eigenschaftennamen können nicht direkt abrufen von Eigenschaftswerten verwendet werden. Sie müssen zuerst Eigenschaftenbezeichner über die [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) -Methode zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="3f1ca-130">Property names cannot be used to obtain property values directly; they must first be mapped to property identifiers through the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> <span data-ttu-id="3f1ca-131">Für bestimmte Objekte wie Nachrichten reserviert MAPI einen Bereich von IDs für benutzerdefinierte Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3f1ca-131">For particular objects such as messages, MAPI reserves a range of property identifiers for custom properties.</span></span> <span data-ttu-id="3f1ca-132">Aus diesem Grund für diese Objekte Clients müssen keine benannte Eigenschaften verwenden, und das zugeordnete speichern können Aufwand.</span><span class="sxs-lookup"><span data-stu-id="3f1ca-132">Therefore, for these objects, clients do not have to use named properties and can save the associated overhead.</span></span> 
  
<span data-ttu-id="3f1ca-133">Weitere Informationen zu benannten Eigenschaften finden Sie unter [Eigenschaften mit dem Namen](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="3f1ca-133">For more information about named properties, see [Named Properties](mapi-named-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3f1ca-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f1ca-134">See also</span></span>



[<span data-ttu-id="3f1ca-135">GUID</span><span class="sxs-lookup"><span data-stu-id="3f1ca-135">GUID</span></span>](guid.md)
  
[<span data-ttu-id="3f1ca-136">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="3f1ca-136">IMAPIProp::GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md)


[<span data-ttu-id="3f1ca-137">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="3f1ca-137">MAPI Structures</span></span>](mapi-structures.md)

