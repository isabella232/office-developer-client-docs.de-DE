---
title: ScCountProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCountProps
api_type:
- COM
ms.assetid: 76e4cc52-e1a0-4e0b-a2a6-a17644f6b2e7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 49634bda487143ddd8d8806b94f6c451ccf57b75
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404974"
---
# <a name="sccountprops"></a><span data-ttu-id="bf414-103">ScCountProps</span><span class="sxs-lookup"><span data-stu-id="bf414-103">ScCountProps</span></span>

  
  
<span data-ttu-id="bf414-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf414-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bf414-105">Bestimmt die Größe eines Eigenschafts Wertarrays in Byte und überprüft den dem Array zugeordneten Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="bf414-105">Determines the size, in bytes, of a property value array and validates the memory associated with the array.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bf414-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="bf414-106">Header file:</span></span>  <br/> |<span data-ttu-id="bf414-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="bf414-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="bf414-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="bf414-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="bf414-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="bf414-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="bf414-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="bf414-110">Called by:</span></span>  <br/> |<span data-ttu-id="bf414-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="bf414-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCountProps(
  int cprop,
  LPSPropValue rgprop,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="bf414-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf414-112">Parameters</span></span>

 <span data-ttu-id="bf414-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="bf414-113">_cprop_</span></span>
  
> <span data-ttu-id="bf414-114">in Die Anzahl der Eigenschaften im durch den _rgprop_ -Parameter angegebenen Array.</span><span class="sxs-lookup"><span data-stu-id="bf414-114">[in] Count of properties in the array indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="bf414-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="bf414-115">_rgprop_</span></span>
  
> <span data-ttu-id="bf414-116">in Zeiger auf einen Bereich in einem Array von [SPropValue](spropvalue.md) -Strukturen, der die Eigenschaften definiert, deren Größe bestimmt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bf414-116">[in] Pointer to a range in an array of [SPropValue](spropvalue.md) structures that defines the properties whose size is to be determined.</span></span> <span data-ttu-id="bf414-117">Dieser Bereich beginnt nicht unbedingt am Anfang des Arrays.</span><span class="sxs-lookup"><span data-stu-id="bf414-117">This range does not necessarily start at the beginning of the array.</span></span> 
    
 <span data-ttu-id="bf414-118">_PCB_</span><span class="sxs-lookup"><span data-stu-id="bf414-118">_pcb_</span></span>
  
> <span data-ttu-id="bf414-119">Out Optionaler Zeiger auf die Größe des Eigenschaften Arrays in Byte.</span><span class="sxs-lookup"><span data-stu-id="bf414-119">[out] Optional pointer to the size, in bytes, of the property array.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bf414-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bf414-120">Return value</span></span>

<span data-ttu-id="bf414-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="bf414-121">S_OK</span></span> 
  
> <span data-ttu-id="bf414-122">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="bf414-122">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="bf414-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="bf414-123">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="bf414-124">Mindestens eine Eigenschaft im Eigenschafts Wertarray hat einen Bezeichner von PROP_ID_NULL oder PROP_ID_INVALID, oder das Eigenschaftenarray enthält eine mehrwertige Eigenschaft ohne Eigenschaftswerte.</span><span class="sxs-lookup"><span data-stu-id="bf414-124">At least one property in the property value array has an identifier of PROP_ID_NULL or PROP_ID_INVALID, or the property array contains a multivalued property with no property values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bf414-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bf414-125">Remarks</span></span>

<span data-ttu-id="bf414-126">Wenn NULL im _PCB_ -Parameter übergeben wird, überprüft die **ScCountProps** -Funktion das Array der Benachrichtigungen, aber es erfolgt keine Zählung.</span><span class="sxs-lookup"><span data-stu-id="bf414-126">If NULL is passed in the  _pcb_ parameter, the **ScCountProps** function validates the array of notifications but no counting is done.</span></span> <span data-ttu-id="bf414-127">Wenn ein Wert ungleich NULL in _PCB_übergeben wird, bestimmt die **ScCountNotifications** -Funktion die Größe des Arrays und speichert die Ursache _PCB_.</span><span class="sxs-lookup"><span data-stu-id="bf414-127">If a non-null value is passed in  _pcb_, the **ScCountNotifications** function determines the size of the array and stores the cause  _pcb_.</span></span> <span data-ttu-id="bf414-128">Der _PCB_ -Parameter muss so hoch sein, dass er das gesamte Array enthält.</span><span class="sxs-lookup"><span data-stu-id="bf414-128">The  _pcb_ parameter must be large enough to contain the entire array.</span></span> 
  
<span data-ttu-id="bf414-129">Wie gezählt, überprüft **ScCountProps** den dem Array zugeordneten Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="bf414-129">As it is counting, **ScCountProps** validates the memory associated with the array.</span></span> <span data-ttu-id="bf414-130">**ScCountProps** funktioniert nur mit Eigenschaften, deren MAPI-Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="bf414-130">**ScCountProps** only works with properties about which MAPI has information.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bf414-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bf414-131">See also</span></span>



[<span data-ttu-id="bf414-132">PropCopyMore</span><span class="sxs-lookup"><span data-stu-id="bf414-132">PropCopyMore</span></span>](propcopymore.md)

