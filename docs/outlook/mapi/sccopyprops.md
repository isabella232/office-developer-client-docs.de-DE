---
title: ScCopyProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCopyProps
api_type:
- COM
ms.assetid: 08bc256c-9706-4f3e-9a12-3e9cca5e4caa
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1afd922459be2ec4bbbd27a61fdf6fcb425548c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411008"
---
# <a name="sccopyprops"></a><span data-ttu-id="5624c-103">ScCopyProps</span><span class="sxs-lookup"><span data-stu-id="5624c-103">ScCopyProps</span></span>

  
  
<span data-ttu-id="5624c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5624c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5624c-105">Kopiert die durch ein Array von [SPropValue-Strukturen definierten Eigenschaften](spropvalue.md) in ein neues Ziel.</span><span class="sxs-lookup"><span data-stu-id="5624c-105">Copies the properties defined by an array of [SPropValue](spropvalue.md) structures to a new destination.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5624c-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="5624c-106">Header file:</span></span>  <br/> |<span data-ttu-id="5624c-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="5624c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="5624c-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="5624c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5624c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5624c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5624c-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="5624c-110">Called by:</span></span>  <br/> |<span data-ttu-id="5624c-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="5624c-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCopyProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="5624c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5624c-112">Parameters</span></span>

 <span data-ttu-id="5624c-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="5624c-113">_cprop_</span></span>
  
> <span data-ttu-id="5624c-114">[in] Anzahl der zu kopierenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5624c-114">[in] Count of properties to be copied.</span></span> 
    
 <span data-ttu-id="5624c-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="5624c-115">_rgprop_</span></span>
  
> <span data-ttu-id="5624c-116">[in] Zeiger auf ein Array von [SPropValue-Strukturen,](spropvalue.md) die die zu kopierenden Eigenschaften definieren.</span><span class="sxs-lookup"><span data-stu-id="5624c-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures that define the properties to be copied.</span></span> <span data-ttu-id="5624c-117">Der  _rgprop-Parameter_ muss nicht auf den Anfang des Arrays verweisen, sondern auf den Anfang einer **der SPropValue-Strukturen** im Array.</span><span class="sxs-lookup"><span data-stu-id="5624c-117">The  _rgprop_ parameter does not have to point to the beginning of the array, but it must point to the beginning of one of the **SPropValue** structures in the array.</span></span> 
    
 <span data-ttu-id="5624c-118">_pvDst_</span><span class="sxs-lookup"><span data-stu-id="5624c-118">_pvDst_</span></span>
  
> <span data-ttu-id="5624c-119">[in] Zeiger auf die Ausgangsposition im Arbeitsspeicher, in die diese Funktion die Eigenschaften kopiert.</span><span class="sxs-lookup"><span data-stu-id="5624c-119">[in] Pointer to the initial position in memory to which this function copies the properties.</span></span> 
    
 <span data-ttu-id="5624c-120">_leiterplatte_</span><span class="sxs-lookup"><span data-stu-id="5624c-120">_pcb_</span></span>
  
> <span data-ttu-id="5624c-121">[out] Optionaler Zeiger auf die Größe des Speicherblocks in Bytes, auf den der  _pvDst-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="5624c-121">[out] Optional pointer to the size, in bytes, of the block of memory pointed to by the  _pvDst_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5624c-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5624c-122">Return value</span></span>

<span data-ttu-id="5624c-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="5624c-123">S_OK</span></span>
  
> <span data-ttu-id="5624c-124">Eigenschaften wurden erfolgreich kopiert.</span><span class="sxs-lookup"><span data-stu-id="5624c-124">Properties were copied successfully.</span></span>
    
<span data-ttu-id="5624c-125">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5624c-125">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="5624c-126">Es wurde ein unbekannter Eigenschaftstyp gefunden.</span><span class="sxs-lookup"><span data-stu-id="5624c-126">An unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5624c-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5624c-127">Remarks</span></span>

<span data-ttu-id="5624c-128">Das neue Array und seine Daten befinden sich in einem Puffer, der mit einer einzigen Zuordnung erstellt wurde, und die [ScRelocProps-Funktion](screlocprops.md) kann verwendet werden, um die Zeiger in den einzelnen [SPropValue-Strukturen anzupassen.](spropvalue.md)</span><span class="sxs-lookup"><span data-stu-id="5624c-128">The new array and its data reside in a buffer created with a single allocation, and the [ScRelocProps](screlocprops.md) function can be used to adjust the pointers in the individual [SPropValue](spropvalue.md) structures.</span></span> <span data-ttu-id="5624c-129">Vor dieser Anpassung sind die Zeiger gültig.</span><span class="sxs-lookup"><span data-stu-id="5624c-129">Prior to this adjustment, the pointers are valid.</span></span> 
  
 <span data-ttu-id="5624c-130">**ScCopyProps** behält die ursprüngliche Eigenschaftsreihenfolge für das kopierte Eigenschaftenarray bei.</span><span class="sxs-lookup"><span data-stu-id="5624c-130">**ScCopyProps** maintains the original property order for the copied property array.</span></span> 
  
<span data-ttu-id="5624c-131">Der  _#A0_ ist optional. Wenn er nicht NULL ist, wird er auf die Anzahl der Bytes festgelegt, die im  _pvDst-Parameter gespeichert_ sind.</span><span class="sxs-lookup"><span data-stu-id="5624c-131">The  _pcb_ parameter is optional; if it is not NULL, it is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5624c-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5624c-132">See also</span></span>



[<span data-ttu-id="5624c-133">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="5624c-133">ScDupPropset</span></span>](scduppropset.md)

