---
title: IMAPITableGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetLastError
api_type:
- COM
ms.assetid: 832e2c18-ddba-4d18-a391-710d21fe23e6
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8b7b1db5bcc718858b01f122f53406c885998741
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593816"
---
# <a name="imapitablegetlasterror"></a><span data-ttu-id="4d4ee-103">IMAPITable::GetLastError</span><span class="sxs-lookup"><span data-stu-id="4d4ee-103">IMAPITable::GetLastError</span></span>

  
  
<span data-ttu-id="4d4ee-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d4ee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d4ee-105">Gibt eine [MAPIERROR](mapierror.md) -Struktur mit Informationen über den vorherigen Fehler in der Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="4d4ee-105">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error on the table.</span></span> 
  
```cpp
HRESULT GetLastError(
HRESULT hResult,
ULONG ulFlags,
LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="4d4ee-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d4ee-106">Parameters</span></span>

 <span data-ttu-id="4d4ee-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="4d4ee-107">_hResult_</span></span>
  
> <span data-ttu-id="4d4ee-108">[in] HRESULT, das den im vorherigen Methodenaufruf generierten Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="4d4ee-108">[in] HRESULT containing the error generated in the previous method call.</span></span>
    
 <span data-ttu-id="4d4ee-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4d4ee-109">_ulFlags_</span></span>
  
> <span data-ttu-id="4d4ee-110">[in] Bitmaske aus Flags, die den Typ des zurückgegebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="4d4ee-110">[in] Bitmask of flags that controls the type of the returned strings.</span></span> <span data-ttu-id="4d4ee-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="4d4ee-111">The following flag can be set:</span></span>
    
<span data-ttu-id="4d4ee-112">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4d4ee-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="4d4ee-113">Die Zeichenfolgen in der **MAPIERROR** -Struktur zurückgegeben, die im Parameter _LppMAPIError_ sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="4d4ee-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="4d4ee-114">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="4d4ee-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="4d4ee-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="4d4ee-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="4d4ee-116">[out] Zeiger auf einen Zeiger auf das zurückgegebene **MAPIERROR** -Struktur, die Angaben zu Version, Komponente und Kontext für den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="4d4ee-116">[out] Pointer to a pointer to the returned **MAPIERROR** structure containing version, component, and context information for the error.</span></span> <span data-ttu-id="4d4ee-117">Der Parameter _LppMAPIError_ kann auf NULL festgelegt werden, wenn eine **MAPIERROR** -Struktur mit den entsprechenden Informationen bereitgestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="4d4ee-117">The  _lppMAPIError_ parameter can be set to NULL if a **MAPIERROR** structure with appropriate information cannot be provided.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4d4ee-118">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="4d4ee-118">Return value</span></span>

<span data-ttu-id="4d4ee-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="4d4ee-119">S_OK</span></span> 
  
> <span data-ttu-id="4d4ee-120">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="4d4ee-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="4d4ee-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="4d4ee-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="4d4ee-122">Entweder die Option MAPI_UNICODE festgelegt wurde und die Implementierung unterstützt keine Unicode oder Parameter MAPI_UNICODE nicht festgelegt wurde und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="4d4ee-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation only supports Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4d4ee-123">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="4d4ee-123">Remarks</span></span>

<span data-ttu-id="4d4ee-124">Die **IMAPITable::GetLastError** -Methode gibt ausführliche Informationen zurück, wenn zu einem Aufruf der vorherigen-Methode, die nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="4d4ee-124">The **IMAPITable::GetLastError** method returns detailed information, if available, about a prior method call that failed.</span></span> <span data-ttu-id="4d4ee-125">Diese Informationen kann in einer Nachricht oder ein Dialogfeld angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4d4ee-125">This information can be displayed in a message or a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="4d4ee-126">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="4d4ee-126">Notes to callers</span></span>

<span data-ttu-id="4d4ee-127">Rufen Sie **GetLastError** , wenn Sie zum Anzeigen von Informationen zu einem Fehler, die dem Benutzer müssen.</span><span class="sxs-lookup"><span data-stu-id="4d4ee-127">Call **GetLastError** whenever you need to display information about an error to the user.</span></span> 
  
<span data-ttu-id="4d4ee-128">Sie können nutzen Sie die [MAPIERROR](mapierror.md) auf die Struktur durch den Parameter _LppMAPIError_ gezeigt, wenn das Table-Objekt eine stellt nur, wenn **GetLastError** gibt S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="4d4ee-128">You can make use of the [MAPIERROR](mapierror.md) structure pointed to by the  _lppMAPIError_ parameter if the table object supplies one only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="4d4ee-129">In einigen Fällen kann nicht die Implementierung der Tabelle ermitteln, was letzten Fehlers wurde oder nicht mehr zu dem Fehler gemeldet wurde.</span><span class="sxs-lookup"><span data-stu-id="4d4ee-129">Sometimes the table implementation cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="4d4ee-130">In diesem Fall wird der Mauszeiger am _LppMAPIError_ auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4d4ee-130">In this situation, the pointer at  _lppMAPIError_ is set to NULL.</span></span> 
  
<span data-ttu-id="4d4ee-131">Rufen Sie die [MAPIFreeBuffer](mapifreebuffer.md) -Funktion, um alle Arbeitsspeichers für die Struktur **MAPIERROR** freizugeben.</span><span class="sxs-lookup"><span data-stu-id="4d4ee-131">To release all the memory allocated for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="4d4ee-132">Weitere Informationen über die **GetLastError** -Methode finden Sie unter [Extended MAPI-Fehler](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="4d4ee-132">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4d4ee-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4d4ee-133">See also</span></span>



[<span data-ttu-id="4d4ee-134">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="4d4ee-134">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="4d4ee-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="4d4ee-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="4d4ee-136">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4d4ee-136">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

