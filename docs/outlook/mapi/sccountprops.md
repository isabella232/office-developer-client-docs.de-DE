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
# <a name="sccountprops"></a><span data-ttu-id="a3222-103">ScCountProps</span><span class="sxs-lookup"><span data-stu-id="a3222-103">ScCountProps</span></span>

  
  
<span data-ttu-id="a3222-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a3222-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a3222-105">Bestimmt die Größe eines Eigenschaftswertarrays in Bytes und überprüft den dem Array zugeordneten Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="a3222-105">Determines the size, in bytes, of a property value array and validates the memory associated with the array.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a3222-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="a3222-106">Header file:</span></span>  <br/> |<span data-ttu-id="a3222-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="a3222-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="a3222-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="a3222-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a3222-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a3222-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a3222-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="a3222-110">Called by:</span></span>  <br/> |<span data-ttu-id="a3222-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="a3222-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCountProps(
  int cprop,
  LPSPropValue rgprop,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="a3222-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3222-112">Parameters</span></span>

 <span data-ttu-id="a3222-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="a3222-113">_cprop_</span></span>
  
> <span data-ttu-id="a3222-114">[in] Anzahl der Eigenschaften im Array, das durch den  _rgprop-Parameter angegeben_ wird.</span><span class="sxs-lookup"><span data-stu-id="a3222-114">[in] Count of properties in the array indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="a3222-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="a3222-115">_rgprop_</span></span>
  
> <span data-ttu-id="a3222-116">[in] Zeiger auf einen Bereich in einem Array von [SPropValue-Strukturen,](spropvalue.md) der die Eigenschaften definiert, deren Größe bestimmt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a3222-116">[in] Pointer to a range in an array of [SPropValue](spropvalue.md) structures that defines the properties whose size is to be determined.</span></span> <span data-ttu-id="a3222-117">Dieser Bereich beginnt nicht unbedingt am Anfang des Arrays.</span><span class="sxs-lookup"><span data-stu-id="a3222-117">This range does not necessarily start at the beginning of the array.</span></span> 
    
 <span data-ttu-id="a3222-118">_leiterplatte_</span><span class="sxs-lookup"><span data-stu-id="a3222-118">_pcb_</span></span>
  
> <span data-ttu-id="a3222-119">[out] Optionaler Zeiger auf die Größe des Eigenschaftenarrays in Bytes.</span><span class="sxs-lookup"><span data-stu-id="a3222-119">[out] Optional pointer to the size, in bytes, of the property array.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a3222-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a3222-120">Return value</span></span>

<span data-ttu-id="a3222-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="a3222-121">S_OK</span></span> 
  
> <span data-ttu-id="a3222-122">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="a3222-122">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="a3222-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a3222-123">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="a3222-124">Mindestens eine Eigenschaft im Eigenschaftswertarray hat den Bezeichner PROP_ID_NULL oder PROP_ID_INVALID, oder das Eigenschaftenarray enthält eine mehrwertige Eigenschaft ohne Eigenschaftswerte.</span><span class="sxs-lookup"><span data-stu-id="a3222-124">At least one property in the property value array has an identifier of PROP_ID_NULL or PROP_ID_INVALID, or the property array contains a multivalued property with no property values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a3222-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a3222-125">Remarks</span></span>

<span data-ttu-id="a3222-126">Wenn NULL im  _Parameter "pcb"_ übergeben wird, überprüft die **ScCountProps-Funktion** das Array der Benachrichtigungen, es wird jedoch keine Zählung durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="a3222-126">If NULL is passed in the  _pcb_ parameter, the **ScCountProps** function validates the array of notifications but no counting is done.</span></span> <span data-ttu-id="a3222-127">Wenn ein Nicht-Null-Wert _in_ einer Leiterplatte übergeben wird, bestimmt die **ScCountNotifications-Funktion** die Größe des Arrays und speichert die Ursache _der Leiterplatte._</span><span class="sxs-lookup"><span data-stu-id="a3222-127">If a non-null value is passed in  _pcb_, the **ScCountNotifications** function determines the size of the array and stores the cause  _pcb_.</span></span> <span data-ttu-id="a3222-128">Der  _Parameter "pcb"_ muss groß genug sein, um das gesamte Array enthalten zu können.</span><span class="sxs-lookup"><span data-stu-id="a3222-128">The  _pcb_ parameter must be large enough to contain the entire array.</span></span> 
  
<span data-ttu-id="a3222-129">Während der Zählung **überprüft ScCountProps** den dem Array zugeordneten Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="a3222-129">As it is counting, **ScCountProps** validates the memory associated with the array.</span></span> <span data-ttu-id="a3222-130">**ScCountProps funktioniert** nur mit Eigenschaften, über die MAPI Über Informationen verfügt.</span><span class="sxs-lookup"><span data-stu-id="a3222-130">**ScCountProps** only works with properties about which MAPI has information.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a3222-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a3222-131">See also</span></span>



[<span data-ttu-id="a3222-132">PropCopyMore</span><span class="sxs-lookup"><span data-stu-id="a3222-132">PropCopyMore</span></span>](propcopymore.md)

