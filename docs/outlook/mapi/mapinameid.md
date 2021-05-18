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
# <a name="mapinameid"></a><span data-ttu-id="ec5d7-103">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="ec5d7-103">MAPINAMEID</span></span>

  
  
<span data-ttu-id="ec5d7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ec5d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ec5d7-105">Beschreibt eine benannte Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ec5d7-105">Describes a named property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ec5d7-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="ec5d7-106">Header file:</span></span>  <br/> |<span data-ttu-id="ec5d7-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ec5d7-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="ec5d7-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="ec5d7-108">Members</span></span>

 <span data-ttu-id="ec5d7-109">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="ec5d7-109">**lpguid**</span></span>
  
> <span data-ttu-id="ec5d7-110">Zeiger auf eine [GUID-Struktur,](guid.md) die einen bestimmten Eigenschaftensatz definiert; Dieses Element darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="ec5d7-110">Pointer to a [GUID](guid.md) structure defining a particular property set; this member cannot be NULL.</span></span> <span data-ttu-id="ec5d7-111">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="ec5d7-111">Valid values are as follows:</span></span> 
    
<span data-ttu-id="ec5d7-112">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="ec5d7-112">PS_PUBLIC_STRINGS</span></span>
  
> 
    
<span data-ttu-id="ec5d7-113">PS_MAPI</span><span class="sxs-lookup"><span data-stu-id="ec5d7-113">PS_MAPI</span></span>
  
> 
    
<span data-ttu-id="ec5d7-114">Ein clientdefinierter Wert</span><span class="sxs-lookup"><span data-stu-id="ec5d7-114">A client-defined value</span></span>
  
> 
    
 <span data-ttu-id="ec5d7-115">**ulKind**</span><span class="sxs-lookup"><span data-stu-id="ec5d7-115">**ulKind**</span></span>
  
> <span data-ttu-id="ec5d7-116">Wert, der den Typ des Werts im **Element Kind** beschreibt.</span><span class="sxs-lookup"><span data-stu-id="ec5d7-116">Value describing the type of value in the **Kind** member.</span></span> <span data-ttu-id="ec5d7-117">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="ec5d7-117">Valid values are as follows:</span></span> 
    
<span data-ttu-id="ec5d7-118">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="ec5d7-118">MNID_ID</span></span> 
  
> <span data-ttu-id="ec5d7-119">Das **Element Kind** enthält einen ganzzahligen Wert, der den Eigenschaftennamen darstellt.</span><span class="sxs-lookup"><span data-stu-id="ec5d7-119">The **Kind** member contains an integer value that represents the property name.</span></span> 
    
<span data-ttu-id="ec5d7-120">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="ec5d7-120">MNID_STRING</span></span> 
  
> <span data-ttu-id="ec5d7-121">Das **Kind-Element** enthält eine Unicode-Zeichenzeichenfolge, die den Eigenschaftennamen darstellt.</span><span class="sxs-lookup"><span data-stu-id="ec5d7-121">The **Kind** member contains a Unicode character string representing the property name.</span></span> 
    
 <span data-ttu-id="ec5d7-122">**Kind**</span><span class="sxs-lookup"><span data-stu-id="ec5d7-122">**Kind**</span></span>
  
> <span data-ttu-id="ec5d7-123">Union, die den Namen der benannten Eigenschaft beschreibt.</span><span class="sxs-lookup"><span data-stu-id="ec5d7-123">Union describing the name of the named property.</span></span> <span data-ttu-id="ec5d7-124">Der Name kann entweder ein ganzzahliger Wert sein, der in **lID** gespeichert ist, oder eine Unicode-Zeichenzeichenfolge, die in **lpwstrName gespeichert ist.**</span><span class="sxs-lookup"><span data-stu-id="ec5d7-124">The name can be either an integer value, stored in **lID**, or a Unicode character string, stored in **lpwstrName**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ec5d7-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ec5d7-125">Remarks</span></span>

<span data-ttu-id="ec5d7-126">Die **MAPINAMEID-Struktur** wird verwendet, um benannte Eigenschaften zu beschreiben, die bezeichner über 0x8000.</span><span class="sxs-lookup"><span data-stu-id="ec5d7-126">The **MAPINAMEID** structure is used to describe named properties properties that have identifiers over 0x8000.</span></span> <span data-ttu-id="ec5d7-127">Ein Eigenschaftensatz ist ein wichtiger Teil einer benannten Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ec5d7-127">A property set is an important part a named property.</span></span> <span data-ttu-id="ec5d7-128">Beispielsweise sind PS_PUBLIC_STRINGS oder PS_ROUTING_ADDRTYPE von MAPI definierte Eigenschaftssätze.</span><span class="sxs-lookup"><span data-stu-id="ec5d7-128">For example PS_PUBLIC_STRINGS or PS_ROUTING_ADDRTYPE are property sets defined by MAPI.</span></span> 
  
<span data-ttu-id="ec5d7-129">Mit benannten Eigenschaften können Clients benutzerdefinierte Eigenschaften in einem größeren Namespace definieren, als im MAPI-definierten Eigenschaftenbezeichnerbereich verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="ec5d7-129">Named properties enable clients to define custom properties in a larger namespace than is available in the MAPI-defined property identifier range.</span></span> <span data-ttu-id="ec5d7-130">Eigenschaftsnamen können nicht direkt zum Abrufen von Eigenschaftswerten verwendet werden. Sie müssen zunächst eigenschaftenbezeichnern über die [IMAPIProp::GetIDsFromNames-Methode zugeordnet](imapiprop-getidsfromnames.md) werden.</span><span class="sxs-lookup"><span data-stu-id="ec5d7-130">Property names cannot be used to obtain property values directly; they must first be mapped to property identifiers through the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> <span data-ttu-id="ec5d7-131">Für bestimmte Objekte wie Nachrichten reserviert MAPI einen Bereich von Eigenschaftenbezeichnern für benutzerdefinierte Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ec5d7-131">For particular objects such as messages, MAPI reserves a range of property identifiers for custom properties.</span></span> <span data-ttu-id="ec5d7-132">Daher müssen Clients für diese Objekte keine benannten Eigenschaften verwenden und können den damit verbundenen Aufwand sparen.</span><span class="sxs-lookup"><span data-stu-id="ec5d7-132">Therefore, for these objects, clients do not have to use named properties and can save the associated overhead.</span></span> 
  
<span data-ttu-id="ec5d7-133">Weitere Informationen zu benannten Eigenschaften finden Sie unter [Named Properties](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="ec5d7-133">For more information about named properties, see [Named Properties](mapi-named-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ec5d7-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec5d7-134">See also</span></span>



[<span data-ttu-id="ec5d7-135">GUID</span><span class="sxs-lookup"><span data-stu-id="ec5d7-135">GUID</span></span>](guid.md)
  
[<span data-ttu-id="ec5d7-136">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="ec5d7-136">IMAPIProp::GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md)


[<span data-ttu-id="ec5d7-137">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="ec5d7-137">MAPI Structures</span></span>](mapi-structures.md)

