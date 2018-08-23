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
ms.openlocfilehash: ee004bdfb8d13537fd8823225f155223ebc76ca7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583351"
---
# <a name="sccountprops"></a><span data-ttu-id="596d5-103">ScCountProps</span><span class="sxs-lookup"><span data-stu-id="596d5-103">ScCountProps</span></span>

  
  
<span data-ttu-id="596d5-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="596d5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="596d5-105">Legt fest, der ein Array der Eigenschaft Wert in Byte, und das Array zugeordneten Arbeitsspeicher überprüft.</span><span class="sxs-lookup"><span data-stu-id="596d5-105">Determines the size, in bytes, of a property value array and validates the memory associated with the array.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="596d5-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="596d5-106">Header file:</span></span>  <br/> |<span data-ttu-id="596d5-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="596d5-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="596d5-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="596d5-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="596d5-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="596d5-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="596d5-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="596d5-110">Called by:</span></span>  <br/> |<span data-ttu-id="596d5-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="596d5-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCountProps(
  int cprop,
  LPSPropValue rgprop,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="596d5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="596d5-112">Parameters</span></span>

 <span data-ttu-id="596d5-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="596d5-113">_cprop_</span></span>
  
> <span data-ttu-id="596d5-114">[in] Anzahl der Eigenschaften in das Array, das durch den Parameter _Rgprop_ angegeben.</span><span class="sxs-lookup"><span data-stu-id="596d5-114">[in] Count of properties in the array indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="596d5-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="596d5-115">_rgprop_</span></span>
  
> <span data-ttu-id="596d5-116">[in] Zeiger auf einen Bereich in einem Array von [SPropValue](spropvalue.md) -Strukturen, die die Eigenschaften definiert, deren Größe bestimmt werden soll.</span><span class="sxs-lookup"><span data-stu-id="596d5-116">[in] Pointer to a range in an array of [SPropValue](spropvalue.md) structures that defines the properties whose size is to be determined.</span></span> <span data-ttu-id="596d5-117">In diesem Bereich wird am Anfang des Arrays nicht notwendigerweise gestartet.</span><span class="sxs-lookup"><span data-stu-id="596d5-117">This range does not necessarily start at the beginning of the array.</span></span> 
    
 <span data-ttu-id="596d5-118">_PCB_</span><span class="sxs-lookup"><span data-stu-id="596d5-118">_pcb_</span></span>
  
> <span data-ttu-id="596d5-119">[out] Optional Zeiger auf die Größe des Arrays der Eigenschaft in Bytes.</span><span class="sxs-lookup"><span data-stu-id="596d5-119">[out] Optional pointer to the size, in bytes, of the property array.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="596d5-120">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="596d5-120">Return value</span></span>

<span data-ttu-id="596d5-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="596d5-121">S_OK</span></span> 
  
> <span data-ttu-id="596d5-122">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="596d5-122">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="596d5-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="596d5-123">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="596d5-124">Mindestens eine Eigenschaft im Array-Wert Eigenschaft ist einen Bezeichner vom PROP_ID_NULL oder PROP_ID_INVALID, oder das Array-Eigenschaft enthält eine mehrwertige Eigenschaft keine-Eigenschaft Werte.</span><span class="sxs-lookup"><span data-stu-id="596d5-124">At least one property in the property value array has an identifier of PROP_ID_NULL or PROP_ID_INVALID, or the property array contains a multivalued property with no property values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="596d5-125">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="596d5-125">Remarks</span></span>

<span data-ttu-id="596d5-126">Wenn NULL in der _pcb_ -Parameter übergeben wird, wird die Funktion **ScCountProps** überprüft das Array von Benachrichtigungen, aber keine zählen erfolgt.</span><span class="sxs-lookup"><span data-stu-id="596d5-126">If NULL is passed in the  _pcb_ parameter, the **ScCountProps** function validates the array of notifications but no counting is done.</span></span> <span data-ttu-id="596d5-127">Wenn Sie ein nicht-Nullwert _pcb_übergeben wird, wird die **ScCountNotifications** -Funktion bestimmt die Größe des Arrays und speichert die Ursache _pcb_.</span><span class="sxs-lookup"><span data-stu-id="596d5-127">If a non-null value is passed in  _pcb_, the **ScCountNotifications** function determines the size of the array and stores the cause  _pcb_.</span></span> <span data-ttu-id="596d5-128">Der Parameter _pcb_ muss groß genug für das gesamte Array sein.</span><span class="sxs-lookup"><span data-stu-id="596d5-128">The  _pcb_ parameter must be large enough to contain the entire array.</span></span> 
  
<span data-ttu-id="596d5-129">Wie zählt, überprüft **ScCountProps** das Array zugeordneten Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="596d5-129">As it is counting, **ScCountProps** validates the memory associated with the array.</span></span> <span data-ttu-id="596d5-130">**ScCountProps** funktioniert nur mit Eigenschaften zu denen MAPI Informationen verfügt.</span><span class="sxs-lookup"><span data-stu-id="596d5-130">**ScCountProps** only works with properties about which MAPI has information.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="596d5-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="596d5-131">See also</span></span>



[<span data-ttu-id="596d5-132">PropCopyMore</span><span class="sxs-lookup"><span data-stu-id="596d5-132">PropCopyMore</span></span>](propcopymore.md)

