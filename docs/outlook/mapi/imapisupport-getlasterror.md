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
ms.openlocfilehash: 3e641842dd8264c0cd3556c498bd74c77bda32f7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577506"
---
# <a name="imapisupportgetlasterror"></a><span data-ttu-id="f8edb-103">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="f8edb-103">IMAPISupport::GetLastError</span></span>

  
  
<span data-ttu-id="f8edb-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f8edb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f8edb-105">Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen zu dem Fehler der vorherigen Support-Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="f8edb-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous support object error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="f8edb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8edb-106">Parameters</span></span>

 <span data-ttu-id="f8edb-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="f8edb-107">_hResult_</span></span>
  
> <span data-ttu-id="f8edb-108">[in] Ein Handle für den Fehlerwert generiert, die in der vorherigen Aufruf-Methode für das Objekt unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f8edb-108">[in] A handle to the error value generated in the previous method call for the support object.</span></span>
    
 <span data-ttu-id="f8edb-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f8edb-109">_ulFlags_</span></span>
  
> <span data-ttu-id="f8edb-110">[in] Eine Bitmaske aus Flags, die den Typ des zurückgegebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="f8edb-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="f8edb-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="f8edb-111">The following flag can be set:</span></span>
    
<span data-ttu-id="f8edb-112">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f8edb-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="f8edb-113">Die Zeichenfolgen in der **MAPIERROR** -Struktur zurückgegeben, die im Parameter _LppMAPIError_ sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="f8edb-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="f8edb-114">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="f8edb-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="f8edb-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="f8edb-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="f8edb-116">[out] Ein Zeiger auf einen Zeiger auf die **MAPIERROR** -Struktur, die Angaben zu Version, Komponente und Kontext für den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="f8edb-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="f8edb-117">Der Parameter _LppMAPIError_ kann auf NULL festgelegt werden, wenn eine **MAPIERROR** -Struktur mit den entsprechenden Fehlerinformationen bereitgestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="f8edb-117">The  _lppMAPIError_ parameter can be set to NULL if a **MAPIERROR** structure with appropriate error information cannot be provided.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f8edb-118">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="f8edb-118">Return value</span></span>

<span data-ttu-id="f8edb-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="f8edb-119">S_OK</span></span> 
  
> <span data-ttu-id="f8edb-120">Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f8edb-120">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="f8edb-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="f8edb-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="f8edb-122">Entweder die Option MAPI_UNICODE festgelegt wurde und MAPI unterstützt keine Unicode oder Parameter MAPI_UNICODE wurde nicht festgelegt und MAPI unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="f8edb-122">Either the MAPI_UNICODE flag was set and MAPI does not support Unicode, or MAPI_UNICODE was not set and MAPI supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f8edb-123">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="f8edb-123">Remarks</span></span>

<span data-ttu-id="f8edb-124">Die **IMAPISupport::GetLastError** -Methode wird für alle Unterstützungsobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="f8edb-124">The **IMAPISupport::GetLastError** method is implemented for all support objects.</span></span> <span data-ttu-id="f8edb-125">Anrufer können die Benutzer einschließlich der Daten aus der **MAPIERROR** -Struktur in einem Dialogfeld mit ausführlichen Informationen zu dem Fehler bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="f8edb-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f8edb-126">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="f8edb-126">Notes to callers</span></span>

<span data-ttu-id="f8edb-127">Sie können den Zeiger auf die Struktur **MAPIERROR** verwenden, wenn MAPI eine in der _LppMAPIError_ -Parameter stellt nur, wenn **GetLastError** gibt S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="f8edb-127">You can use the pointer to the **MAPIERROR** structure, if MAPI supplies one, in the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="f8edb-128">Manchmal MAPI kann nicht bestimmen, welche letzten Fehlers wurde oder es wurde keine weiteren Bericht zu dem Fehler.</span><span class="sxs-lookup"><span data-stu-id="f8edb-128">Sometimes MAPI cannot determine what the last error was or it has nothing more to report about the error.</span></span> <span data-ttu-id="f8edb-129">In diesem Fall gibt _LppMAPIError_ einen Zeiger stattdessen auf NULL.</span><span class="sxs-lookup"><span data-stu-id="f8edb-129">In this situation,  _lppMAPIError_ returns a pointer to NULL instead.</span></span> 
  
<span data-ttu-id="f8edb-130">Weitere Informationen über die **GetLastError** -Methode finden Sie unter [Extended MAPI-Fehler](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="f8edb-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
<span data-ttu-id="f8edb-131">Um alle durch MAPI Arbeitsspeicher freizugeben, rufen Sie die [MAPIFreeBuffer](mapifreebuffer.md) -Funktion für die zurückgegebene **MAPIERROR** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="f8edb-131">To release all the memory allocated by MAPI, call the [MAPIFreeBuffer](mapifreebuffer.md) function for the returned **MAPIERROR** structure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f8edb-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8edb-132">See also</span></span>



[<span data-ttu-id="f8edb-133">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="f8edb-133">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="f8edb-134">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="f8edb-134">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="f8edb-135">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="f8edb-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="f8edb-136">Fehler Extended MAPI</span><span class="sxs-lookup"><span data-stu-id="f8edb-136">MAPI Extended Errors</span></span>](mapi-extended-errors.md)

