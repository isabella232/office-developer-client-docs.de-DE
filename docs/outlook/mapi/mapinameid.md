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
ms.openlocfilehash: baec750a460b3ba9becd2e1dddf967705424ac4e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411680"
---
# <a name="mapinameid"></a><span data-ttu-id="ba5f0-103">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="ba5f0-103">MAPINAMEID</span></span>

  
  
<span data-ttu-id="ba5f0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ba5f0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ba5f0-105">Beschreibt eine benannte Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ba5f0-105">Describes a named property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ba5f0-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="ba5f0-106">Header file:</span></span>  <br/> |<span data-ttu-id="ba5f0-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="ba5f0-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="ba5f0-108">Members</span><span class="sxs-lookup"><span data-stu-id="ba5f0-108">Members</span></span>

 <span data-ttu-id="ba5f0-109">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="ba5f0-109">**lpguid**</span></span>
  
> <span data-ttu-id="ba5f0-110">Zeiger auf eine [GUID](guid.md) -Struktur, die einen bestimmten Eigenschaftensatz definiert; Dieser Member darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="ba5f0-110">Pointer to a [GUID](guid.md) structure defining a particular property set; this member cannot be NULL.</span></span> <span data-ttu-id="ba5f0-111">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="ba5f0-111">Valid values are as follows:</span></span> 
    
<span data-ttu-id="ba5f0-112">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="ba5f0-112">PS_PUBLIC_STRINGS</span></span>
  
> 
    
<span data-ttu-id="ba5f0-113">PS_MAPI</span><span class="sxs-lookup"><span data-stu-id="ba5f0-113">PS_MAPI</span></span>
  
> 
    
<span data-ttu-id="ba5f0-114">Ein Client definierter Wert</span><span class="sxs-lookup"><span data-stu-id="ba5f0-114">A client-defined value</span></span>
  
> 
    
 <span data-ttu-id="ba5f0-115">**ulKind**</span><span class="sxs-lookup"><span data-stu-id="ba5f0-115">**ulKind**</span></span>
  
> <span data-ttu-id="ba5f0-116">Wert, der den Typ des Werts im **Kind** -Element beschreibt.</span><span class="sxs-lookup"><span data-stu-id="ba5f0-116">Value describing the type of value in the **Kind** member.</span></span> <span data-ttu-id="ba5f0-117">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="ba5f0-117">Valid values are as follows:</span></span> 
    
<span data-ttu-id="ba5f0-118">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="ba5f0-118">MNID_ID</span></span> 
  
> <span data-ttu-id="ba5f0-119">Der Member **Kind** enthält einen ganzzahligen Wert, der den Namen der Eigenschaft darstellt.</span><span class="sxs-lookup"><span data-stu-id="ba5f0-119">The **Kind** member contains an integer value that represents the property name.</span></span> 
    
<span data-ttu-id="ba5f0-120">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="ba5f0-120">MNID_STRING</span></span> 
  
> <span data-ttu-id="ba5f0-121">Der Member **Kind** enthält eine Unicode-Zeichenfolge, die den Namen der Eigenschaft darstellt.</span><span class="sxs-lookup"><span data-stu-id="ba5f0-121">The **Kind** member contains a Unicode character string representing the property name.</span></span> 
    
 <span data-ttu-id="ba5f0-122">**Kind**</span><span class="sxs-lookup"><span data-stu-id="ba5f0-122">**Kind**</span></span>
  
> <span data-ttu-id="ba5f0-123">Union, die den Namen der benannten Eigenschaft beschreibt.</span><span class="sxs-lookup"><span data-stu-id="ba5f0-123">Union describing the name of the named property.</span></span> <span data-ttu-id="ba5f0-124">Der Name kann ein ganzzahliger Wert sein, der im **Deckel**gespeichert ist, oder eine Unicode-Zeichenfolge, die in **lpwstrName**gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="ba5f0-124">The name can be either an integer value, stored in **lID**, or a Unicode character string, stored in **lpwstrName**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ba5f0-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ba5f0-125">Remarks</span></span>

<span data-ttu-id="ba5f0-126">Die **MAPINAMEID** -Struktur wird verwendet, um benannte Eigenschaften Eigenschaften mit Bezeichnern über 0X8000 zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="ba5f0-126">The **MAPINAMEID** structure is used to describe named properties properties that have identifiers over 0x8000.</span></span> <span data-ttu-id="ba5f0-127">Ein Eigenschaftensatz ist ein wichtiger Abschnitt einer benannten Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ba5f0-127">A property set is an important part a named property.</span></span> <span data-ttu-id="ba5f0-128">Beispielsweise sind PS_PUBLIC_STRINGS oder PS_ROUTING_ADDRTYPE Eigenschaftensätze, die von MAPI definiert werden.</span><span class="sxs-lookup"><span data-stu-id="ba5f0-128">For example PS_PUBLIC_STRINGS or PS_ROUTING_ADDRTYPE are property sets defined by MAPI.</span></span> 
  
<span data-ttu-id="ba5f0-129">Mit benannten Eigenschaften können Clients benutzerdefinierte Eigenschaften in einem größeren Namespace definieren, als im MAPI-definierten Eigenschafts bezeichnerbereich verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="ba5f0-129">Named properties enable clients to define custom properties in a larger namespace than is available in the MAPI-defined property identifier range.</span></span> <span data-ttu-id="ba5f0-130">Eigenschaftennamen können nicht verwendet werden, um Eigenschaftswerte direkt abzurufen; Sie müssen zunächst Eigenschaftenbezeichnern über die [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) -Methode zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="ba5f0-130">Property names cannot be used to obtain property values directly; they must first be mapped to property identifiers through the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> <span data-ttu-id="ba5f0-131">Für bestimmte Objekte wie Nachrichten reserviert MAPI eine Reihe von Eigenschaftenbezeichnern für benutzerdefinierte Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ba5f0-131">For particular objects such as messages, MAPI reserves a range of property identifiers for custom properties.</span></span> <span data-ttu-id="ba5f0-132">Daher müssen Clients für diese Objekte keine benannten Eigenschaften verwenden und den zugehörigen Overhead speichern.</span><span class="sxs-lookup"><span data-stu-id="ba5f0-132">Therefore, for these objects, clients do not have to use named properties and can save the associated overhead.</span></span> 
  
<span data-ttu-id="ba5f0-133">Weitere Informationen zu benannten Eigenschaften finden Sie unter [benannte Eigenschaften](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="ba5f0-133">For more information about named properties, see [Named Properties](mapi-named-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ba5f0-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba5f0-134">See also</span></span>



[<span data-ttu-id="ba5f0-135">GUID</span><span class="sxs-lookup"><span data-stu-id="ba5f0-135">GUID</span></span>](guid.md)
  
[<span data-ttu-id="ba5f0-136">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="ba5f0-136">IMAPIProp::GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md)


[<span data-ttu-id="ba5f0-137">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="ba5f0-137">MAPI Structures</span></span>](mapi-structures.md)

