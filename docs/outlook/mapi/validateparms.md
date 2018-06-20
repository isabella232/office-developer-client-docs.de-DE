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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a22f7628b306707474e4ffb6fdf4525e00bf0771
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795858"
---
# <a name="validateparms"></a><span data-ttu-id="31ab8-103">ValidateParms</span><span class="sxs-lookup"><span data-stu-id="31ab8-103">ValidateParms</span></span>

  
  
<span data-ttu-id="31ab8-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="31ab8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="31ab8-105">Ruft eine interne Funktion, um zu überprüfen, dass die Parameter-Clientanwendungen Dienstanbietern vergangen sind.</span><span class="sxs-lookup"><span data-stu-id="31ab8-105">Calls an internal function to check the parameters client applications have passed to service providers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="31ab8-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="31ab8-106">Header file:</span></span>  <br/> |<span data-ttu-id="31ab8-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="31ab8-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="31ab8-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="31ab8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="31ab8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="31ab8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="31ab8-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="31ab8-110">Called by:</span></span>  <br/> |<span data-ttu-id="31ab8-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="31ab8-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT ValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="31ab8-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="31ab8-112">Parameters</span></span>

 <span data-ttu-id="31ab8-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="31ab8-113">_eMethod_</span></span>
  
> <span data-ttu-id="31ab8-114">[in] Gibt den-Enumeration zurück, die-Methode, um zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="31ab8-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="31ab8-115">_Erster_</span><span class="sxs-lookup"><span data-stu-id="31ab8-115">_First_</span></span>
  
> <span data-ttu-id="31ab8-116">[in] Zeiger auf das erste Argument im Stapel.</span><span class="sxs-lookup"><span data-stu-id="31ab8-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="31ab8-117">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="31ab8-117">Return value</span></span>

<span data-ttu-id="31ab8-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="31ab8-118">S_OK</span></span> 
  
> <span data-ttu-id="31ab8-119">Alle Parameter sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="31ab8-119">All of the parameters are valid.</span></span> 
    
<span data-ttu-id="31ab8-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="31ab8-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="31ab8-121">Eine oder mehrere der Parameter sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="31ab8-121">One or more of the parameters are not valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="31ab8-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="31ab8-122">Remarks</span></span>

<span data-ttu-id="31ab8-123">Übergeben Sie Parameter zwischen MAPI- und Service Provider wird angenommen, dass korrekt und unterzogen werden nur Debug Validierung mit dem Makro [CheckParms](checkparms.md) .</span><span class="sxs-lookup"><span data-stu-id="31ab8-123">Parameters passed between MAPI and service providers are assumed to be correct and undergo only debug validation with the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="31ab8-124">Anbieter sollten alle von Clientanwendungen übergebenen Parameter überprüfen, aber Clients sollten davon ausgehen, dass MAPI und Anbieter Parameter richtig sind.</span><span class="sxs-lookup"><span data-stu-id="31ab8-124">Providers should check all parameters passed in by client applications, but clients should assume that MAPI and provider parameters are correct.</span></span> <span data-ttu-id="31ab8-125">Verwenden Sie das Makro **HR_FAILED** , um Rückgabewerte testen.</span><span class="sxs-lookup"><span data-stu-id="31ab8-125">Use the **HR_FAILED** macro to test return values.</span></span> 
  
 <span data-ttu-id="31ab8-126">**ValidateParms** ist anders aufgerufen, je nachdem, ob der aufrufende Code C oder C++ ist.</span><span class="sxs-lookup"><span data-stu-id="31ab8-126">**ValidateParms** is called differently depending on whether the calling code is C or C++.</span></span> <span data-ttu-id="31ab8-127">C++ übergibt einen impliziten Parameter zu jedem Methodenaufruf, die wird explizite in C# und ist die Adresse des Objekts als _diese_ bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="31ab8-127">C++ passes an implicit parameter known as  _this_ to each method call, which becomes explicit in C and is the address of the object.</span></span> <span data-ttu-id="31ab8-128">Der erste Parameter, _eMethod_, ist ein Enumerator, die aus der Benutzeroberfläche und den validierten-Methode und teilt welche Parameter Sie erwarten, auf dem Stapel zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="31ab8-128">The first parameter,  _eMethod_, is an enumerator made from the interface and method being validated and tells what parameters to expect to find on the stack.</span></span> <span data-ttu-id="31ab8-129">Der zweite Parameter ist für C und C++ unterschiedlich.</span><span class="sxs-lookup"><span data-stu-id="31ab8-129">The second parameter is different for C and C++.</span></span> <span data-ttu-id="31ab8-130">In C++ ist es _ersten_aufgerufen, und es ist der erste Parameter der Methode überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="31ab8-130">In C++ it is called  _First_, and it is the first parameter to the method being validated.</span></span> <span data-ttu-id="31ab8-131">Der zweite Parameter für die Sprache C, _PpThis_, ist die Adresse des ersten Parameters an die-Methode, die immer ein Objektzeiger ist.</span><span class="sxs-lookup"><span data-stu-id="31ab8-131">The second parameter for the C language,  _ppThis_, is the address of the first parameter to the method which is always an object pointer.</span></span> <span data-ttu-id="31ab8-132">In beiden Fällen der zweite Parameter gibt die Adresse des Anfang der Parameterliste der Methode, und basierend auf _eMethod_, wird der Stapel nach unten verschoben und überprüft die Parameter.</span><span class="sxs-lookup"><span data-stu-id="31ab8-132">In both cases, the second parameter gives the address of the beginning of the method's parameter list, and based on  _eMethod_, moves down the stack and validates the parameters.</span></span> 
  
<span data-ttu-id="31ab8-133">Anbieter für gemeinsame Schnittstellen wie **IMAPITable** und **IMAPIProp** implementieren sollten immer Parameter mithilfe der **ValidateParms** -Funktion, um Stellen Sie sicher, dass Konsistenz für alle Anbieter überprüfen.</span><span class="sxs-lookup"><span data-stu-id="31ab8-133">Providers implementing common interfaces such as **IMAPITable** and **IMAPIProp** should always check parameters using the **ValidateParms** function in order to make sure consistency across all providers.</span></span> <span data-ttu-id="31ab8-134">Zusätzliche Parameter Validierungsfunktionen wurden für einige komplexen Parametertypen entsprechend verwendet werden muss definiert.</span><span class="sxs-lookup"><span data-stu-id="31ab8-134">Additional parameter validation functions have been defined for some complex parameter types to be used instead as appropriate.</span></span> <span data-ttu-id="31ab8-135">Finden Sie in den Referenzthemen für die folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="31ab8-135">See the reference topics for the following functions:</span></span> 
  
- [<span data-ttu-id="31ab8-136">FBadColumnSet</span><span class="sxs-lookup"><span data-stu-id="31ab8-136">FBadColumnSet</span></span>](fbadcolumnset.md)
    
- [<span data-ttu-id="31ab8-137">FBadEntryList</span><span class="sxs-lookup"><span data-stu-id="31ab8-137">FBadEntryList</span></span>](fbadentrylist.md)
    
- [<span data-ttu-id="31ab8-138">FBadProp</span><span class="sxs-lookup"><span data-stu-id="31ab8-138">FBadProp</span></span>](fbadprop.md)
    
- [<span data-ttu-id="31ab8-139">FBadProp</span><span class="sxs-lookup"><span data-stu-id="31ab8-139">FBadProp</span></span>](fbadprop.md)
    
- [<span data-ttu-id="31ab8-140">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="31ab8-140">FBadRestriction</span></span>](fbadrestriction.md)
    
- [<span data-ttu-id="31ab8-141">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="31ab8-141">FBadRestriction</span></span>](fbadrestriction.md)
    
- [<span data-ttu-id="31ab8-142">FBadRglpszW</span><span class="sxs-lookup"><span data-stu-id="31ab8-142">FBadRglpszW</span></span>](fbadrglpszw.md)
    
- [<span data-ttu-id="31ab8-143">FBadRow</span><span class="sxs-lookup"><span data-stu-id="31ab8-143">FBadRow</span></span>](fbadrow.md)
    
- [<span data-ttu-id="31ab8-144">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="31ab8-144">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="31ab8-145">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="31ab8-145">FBadSortOrderSet</span></span>](fbadsortorderset.md)
    
<span data-ttu-id="31ab8-146">Geerbte Methoden verwenden die gleichen Parameter Überprüfung als Schnittstelle von der sie erben.</span><span class="sxs-lookup"><span data-stu-id="31ab8-146">Inherited methods use the same parameter validation as the interface from which they inherit.</span></span> <span data-ttu-id="31ab8-147">Beispielsweise sollte der Überprüfung der **IMessage** und **IMAPIProp** Parameter identisch sein.</span><span class="sxs-lookup"><span data-stu-id="31ab8-147">For example, the parameter checking for **IMessage** and **IMAPIProp** should be the same.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="31ab8-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31ab8-148">See also</span></span>



[<span data-ttu-id="31ab8-149">UlValidateParms</span><span class="sxs-lookup"><span data-stu-id="31ab8-149">UlValidateParms</span></span>](ulvalidateparms.md)

