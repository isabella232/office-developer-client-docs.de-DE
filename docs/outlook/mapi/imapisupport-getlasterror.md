---
title: IMAPISupportGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetLastError
api_type:
- COM
ms.assetid: 5b4290d9-230f-416a-9644-188578565c7b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c34c175c43ada03e982f08a27f675448ea24a567
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438547"
---
# <a name="imapisupportgetlasterror"></a><span data-ttu-id="ac8e3-103">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="ac8e3-103">IMAPISupport::GetLastError</span></span>

  
  
<span data-ttu-id="ac8e3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac8e3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac8e3-105">Gibt eine [MAPIERROR](mapierror.md) -Struktur zurück, die Informationen zum vorherigen Support Objekt Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="ac8e3-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous support object error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="ac8e3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac8e3-106">Parameters</span></span>

 <span data-ttu-id="ac8e3-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="ac8e3-107">_hResult_</span></span>
  
> <span data-ttu-id="ac8e3-108">in Ein Handle für den Fehlerwert, der im vorherigen Methodenaufruf für das Support-Objekt generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="ac8e3-108">[in] A handle to the error value generated in the previous method call for the support object.</span></span>
    
 <span data-ttu-id="ac8e3-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ac8e3-109">_ulFlags_</span></span>
  
> <span data-ttu-id="ac8e3-110">in Eine Bitmaske von Flags, die den Typ der zurückgegebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="ac8e3-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="ac8e3-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="ac8e3-111">The following flag can be set:</span></span>
    
<span data-ttu-id="ac8e3-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ac8e3-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ac8e3-113">Die Zeichenfolgen in der **MAPIERROR** -Struktur, die im _lppMAPIError_ -Parameter zurückgegeben werden, sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="ac8e3-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="ac8e3-114">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="ac8e3-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="ac8e3-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="ac8e3-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="ac8e3-116">Out Ein Zeiger auf einen Zeiger auf die **MAPIERROR** -Struktur, die Versions-, Komponenten-und Kontextinformationen für den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="ac8e3-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="ac8e3-117">Der _lppMAPIError_ -Parameter kann auf NULL festgelegt werden, wenn eine **MAPIERROR** -Struktur mit entsprechenden Fehlerinformationen nicht bereitgestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ac8e3-117">The  _lppMAPIError_ parameter can be set to NULL if a **MAPIERROR** structure with appropriate error information cannot be provided.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ac8e3-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ac8e3-118">Return value</span></span>

<span data-ttu-id="ac8e3-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="ac8e3-119">S_OK</span></span> 
  
> <span data-ttu-id="ac8e3-120">Der Aufruf war erfolgreich, und der erwartete Wert oder die Werte wurden zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ac8e3-120">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="ac8e3-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="ac8e3-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="ac8e3-122">Entweder wurde das MAPI_UNICODE-Flag festgelegt, und MAPI unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und MAPI unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="ac8e3-122">Either the MAPI_UNICODE flag was set and MAPI does not support Unicode, or MAPI_UNICODE was not set and MAPI supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ac8e3-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac8e3-123">Remarks</span></span>

<span data-ttu-id="ac8e3-124">Die **IMAPISupport:: getlasterroraufzurufen** -Methode wird für alle Support-Objekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="ac8e3-124">The **IMAPISupport::GetLastError** method is implemented for all support objects.</span></span> <span data-ttu-id="ac8e3-125">Aufrufer können Ihren Benutzern detaillierte Informationen zum Fehler bereitstellen, indem Sie die Daten aus der **MAPIERROR** -Struktur in ein Dialogfeld einschließen.</span><span class="sxs-lookup"><span data-stu-id="ac8e3-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ac8e3-126">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="ac8e3-126">Notes to callers</span></span>

<span data-ttu-id="ac8e3-127">Sie können den Zeiger auf die **MAPIERROR** -Struktur verwenden, wenn MAPI eine bereitstellt, im Parameter _lppMAPIError_ nur, wenn **getlasterroraufzurufen** S_OK zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="ac8e3-127">You can use the pointer to the **MAPIERROR** structure, if MAPI supplies one, in the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="ac8e3-128">Manchmal kann MAPI nicht ermitteln, was der letzte Fehler war, oder er hat nichts mehr über den Fehler zu berichten.</span><span class="sxs-lookup"><span data-stu-id="ac8e3-128">Sometimes MAPI cannot determine what the last error was or it has nothing more to report about the error.</span></span> <span data-ttu-id="ac8e3-129">In dieser Situation gibt _lppMAPIError_ stattdessen einen Zeiger auf NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="ac8e3-129">In this situation,  _lppMAPIError_ returns a pointer to NULL instead.</span></span> 
  
<span data-ttu-id="ac8e3-130">Weitere Informationen zur **getlasterroraufzurufen** -Methode finden Sie unter [MAPI Extended Errors](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="ac8e3-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
<span data-ttu-id="ac8e3-131">Um den gesamten von MAPI reservierten Arbeitsspeicher freizugeben, rufen Sie die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion für die zurückgeGebene **MAPIERROR** -Struktur auf.</span><span class="sxs-lookup"><span data-stu-id="ac8e3-131">To release all the memory allocated by MAPI, call the [MAPIFreeBuffer](mapifreebuffer.md) function for the returned **MAPIERROR** structure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ac8e3-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac8e3-132">See also</span></span>



[<span data-ttu-id="ac8e3-133">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="ac8e3-133">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="ac8e3-134">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="ac8e3-134">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="ac8e3-135">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ac8e3-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="ac8e3-136">Erweiterte MAPI-Fehler</span><span class="sxs-lookup"><span data-stu-id="ac8e3-136">MAPI Extended Errors</span></span>](mapi-extended-errors.md)

