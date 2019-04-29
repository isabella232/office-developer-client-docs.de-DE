---
title: ValidateParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ValidateParms
api_type:
- COM
ms.assetid: 3ede1a35-4acc-4b8f-a1bd-027f35798a37
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f2669f703827924493387c4beac0b64b25672860
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436804"
---
# <a name="validateparms"></a><span data-ttu-id="14d57-103">ValidateParms</span><span class="sxs-lookup"><span data-stu-id="14d57-103">ValidateParms</span></span>

  
  
<span data-ttu-id="14d57-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="14d57-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="14d57-105">Ruft eine interne Funktion auf, um die Parameter zu überprüfen, die Clientanwendungen an Dienstanbieter übergeben haben.</span><span class="sxs-lookup"><span data-stu-id="14d57-105">Calls an internal function to check the parameters client applications have passed to service providers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="14d57-106">Headerdatei:</span><span class="sxs-lookup"><span data-stu-id="14d57-106">Header file:</span></span>  <br/> |<span data-ttu-id="14d57-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="14d57-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="14d57-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="14d57-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="14d57-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="14d57-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="14d57-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="14d57-110">Called by:</span></span>  <br/> |<span data-ttu-id="14d57-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="14d57-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT ValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="14d57-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="14d57-112">Parameters</span></span>

 <span data-ttu-id="14d57-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="14d57-113">_eMethod_</span></span>
  
> <span data-ttu-id="14d57-114">in Gibt die zu überprüfende Methode an.</span><span class="sxs-lookup"><span data-stu-id="14d57-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="14d57-115">_First_</span><span class="sxs-lookup"><span data-stu-id="14d57-115">_First_</span></span>
  
> <span data-ttu-id="14d57-116">in Zeiger auf das erste Argument im Stapel.</span><span class="sxs-lookup"><span data-stu-id="14d57-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="14d57-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="14d57-117">Return value</span></span>

<span data-ttu-id="14d57-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="14d57-118">S_OK</span></span> 
  
> <span data-ttu-id="14d57-119">Alle Parameter sind gültig.</span><span class="sxs-lookup"><span data-stu-id="14d57-119">All of the parameters are valid.</span></span> 
    
<span data-ttu-id="14d57-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="14d57-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="14d57-121">Mindestens einer der Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="14d57-121">One or more of the parameters are not valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="14d57-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="14d57-122">Remarks</span></span>

<span data-ttu-id="14d57-123">Parameter, die zwischen MAPI-und Dienstanbietern übergeben werden, werden als richtig angenommen und werden nur mit dem [CheckParms](checkparms.md) -Makro überprüft.</span><span class="sxs-lookup"><span data-stu-id="14d57-123">Parameters passed between MAPI and service providers are assumed to be correct and undergo only debug validation with the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="14d57-124">Anbieter sollten alle Parameter überprüfen, die von Clientanwendungen übergeben wurden, aber Clients sollten davon ausgehen, dass MAPI-und Anbieter Parameter korrekt sind.</span><span class="sxs-lookup"><span data-stu-id="14d57-124">Providers should check all parameters passed in by client applications, but clients should assume that MAPI and provider parameters are correct.</span></span> <span data-ttu-id="14d57-125">Verwenden Sie das **HR_FAILED** -Makro, um Rückgabewerte zu testen.</span><span class="sxs-lookup"><span data-stu-id="14d57-125">Use the **HR_FAILED** macro to test return values.</span></span> 
  
 <span data-ttu-id="14d57-126">**ValidateParms** wird unterschiedlich aufgerufen, je nachdem, ob der Aufrufcode C oder C++ ist.</span><span class="sxs-lookup"><span data-stu-id="14d57-126">**ValidateParms** is called differently depending on whether the calling code is C or C++.</span></span> <span data-ttu-id="14d57-127">C++ übergibt einen impliziten Parameter, der als _this_ bezeichnet wird, an jeden Methodenaufruf, der in C explizit wird und die Adresse des Objekts ist.</span><span class="sxs-lookup"><span data-stu-id="14d57-127">C++ passes an implicit parameter known as  _this_ to each method call, which becomes explicit in C and is the address of the object.</span></span> <span data-ttu-id="14d57-128">Der erste Parameter, _eMethod_, ist ein Enumerator aus der Schnittstelle und der Methode, die validiert wird, und gibt an, welche Parameter im Stapel zu finden sind.</span><span class="sxs-lookup"><span data-stu-id="14d57-128">The first parameter,  _eMethod_, is an enumerator made from the interface and method being validated and tells what parameters to expect to find on the stack.</span></span> <span data-ttu-id="14d57-129">Der zweite Parameter ist für C und C++ unterschiedlich.</span><span class="sxs-lookup"><span data-stu-id="14d57-129">The second parameter is different for C and C++.</span></span> <span data-ttu-id="14d57-130">In C++ wird es _zuerst_aufgerufen und ist der erste Parameter für die validierte Methode.</span><span class="sxs-lookup"><span data-stu-id="14d57-130">In C++ it is called  _First_, and it is the first parameter to the method being validated.</span></span> <span data-ttu-id="14d57-131">Der zweite Parameter für die Sprache C, _ppThis_, ist die Adresse des ersten Parameters der Methode, bei der es sich immer um einen Objektzeiger handelt.</span><span class="sxs-lookup"><span data-stu-id="14d57-131">The second parameter for the C language,  _ppThis_, is the address of the first parameter to the method which is always an object pointer.</span></span> <span data-ttu-id="14d57-132">In beiden Fällen gibt der zweite Parameter die Adresse des Beginns der Parameterliste der Methode an und basiert auf _eMethod_, verschiebt den Stapel nach unten und überprüft die Parameter.</span><span class="sxs-lookup"><span data-stu-id="14d57-132">In both cases, the second parameter gives the address of the beginning of the method's parameter list, and based on  _eMethod_, moves down the stack and validates the parameters.</span></span> 
  
<span data-ttu-id="14d57-133">Anbieter, die gängige Schnittstellen wie **IMAPITable** und **IMAPIProp** implementieren, sollten Parameter mithilfe der **ValidateParms** -Funktion immer überprüfen, um die Konsistenz aller Anbieter sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="14d57-133">Providers implementing common interfaces such as **IMAPITable** and **IMAPIProp** should always check parameters using the **ValidateParms** function in order to make sure consistency across all providers.</span></span> <span data-ttu-id="14d57-134">Es wurden zusätzliche Parameter Validierungsfunktionen für einige komplexe Parametertypen definiert, die stattdessen entsprechend verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="14d57-134">Additional parameter validation functions have been defined for some complex parameter types to be used instead as appropriate.</span></span> <span data-ttu-id="14d57-135">In den Referenzthemen finden Sie die folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="14d57-135">See the reference topics for the following functions:</span></span> 
  
- [<span data-ttu-id="14d57-136">FBadColumnSet</span><span class="sxs-lookup"><span data-stu-id="14d57-136">FBadColumnSet</span></span>](fbadcolumnset.md)
    
- [<span data-ttu-id="14d57-137">FBadEntryList</span><span class="sxs-lookup"><span data-stu-id="14d57-137">FBadEntryList</span></span>](fbadentrylist.md)
    
- [<span data-ttu-id="14d57-138">FBadProp</span><span class="sxs-lookup"><span data-stu-id="14d57-138">FBadProp</span></span>](fbadprop.md)
    
- [<span data-ttu-id="14d57-139">FBadProp</span><span class="sxs-lookup"><span data-stu-id="14d57-139">FBadProp</span></span>](fbadprop.md)
    
- [<span data-ttu-id="14d57-140">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="14d57-140">FBadRestriction</span></span>](fbadrestriction.md)
    
- [<span data-ttu-id="14d57-141">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="14d57-141">FBadRestriction</span></span>](fbadrestriction.md)
    
- [<span data-ttu-id="14d57-142">FBadRglpszW</span><span class="sxs-lookup"><span data-stu-id="14d57-142">FBadRglpszW</span></span>](fbadrglpszw.md)
    
- [<span data-ttu-id="14d57-143">FBadRow</span><span class="sxs-lookup"><span data-stu-id="14d57-143">FBadRow</span></span>](fbadrow.md)
    
- [<span data-ttu-id="14d57-144">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="14d57-144">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="14d57-145">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="14d57-145">FBadSortOrderSet</span></span>](fbadsortorderset.md)
    
<span data-ttu-id="14d57-146">Geerbte Methoden verwenden die gleiche Parametervalidierung wie die Schnittstelle, von der Sie erben.</span><span class="sxs-lookup"><span data-stu-id="14d57-146">Inherited methods use the same parameter validation as the interface from which they inherit.</span></span> <span data-ttu-id="14d57-147">Beispielsweise sollte die Parameterüberprüfung für **IMessage** und **IMAPIProp** identisch sein.</span><span class="sxs-lookup"><span data-stu-id="14d57-147">For example, the parameter checking for **IMessage** and **IMAPIProp** should be the same.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="14d57-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="14d57-148">See also</span></span>



[<span data-ttu-id="14d57-149">UlValidateParms</span><span class="sxs-lookup"><span data-stu-id="14d57-149">UlValidateParms</span></span>](ulvalidateparms.md)

