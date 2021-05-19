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
ms.openlocfilehash: 2444ea7e05367423e7920be3a871c2ab68aad76d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419002"
---
# <a name="imapitablegetlasterror"></a><span data-ttu-id="cb0d7-103">IMAPITable::GetLastError</span><span class="sxs-lookup"><span data-stu-id="cb0d7-103">IMAPITable::GetLastError</span></span>

  
  
<span data-ttu-id="cb0d7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cb0d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cb0d7-105">Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum vorherigen Fehler in der Tabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="cb0d7-105">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error on the table.</span></span> 
  
```cpp
HRESULT GetLastError(
HRESULT hResult,
ULONG ulFlags,
LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="cb0d7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb0d7-106">Parameters</span></span>

 <span data-ttu-id="cb0d7-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="cb0d7-107">_hResult_</span></span>
  
> <span data-ttu-id="cb0d7-108">[in] HRESULT, das den fehler enthält, der im vorherigen Methodenaufruf generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="cb0d7-108">[in] HRESULT containing the error generated in the previous method call.</span></span>
    
 <span data-ttu-id="cb0d7-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cb0d7-109">_ulFlags_</span></span>
  
> <span data-ttu-id="cb0d7-110">[in] Bitmaske von Flags, die den Typ der zurückgegebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="cb0d7-110">[in] Bitmask of flags that controls the type of the returned strings.</span></span> <span data-ttu-id="cb0d7-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="cb0d7-111">The following flag can be set:</span></span>
    
<span data-ttu-id="cb0d7-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="cb0d7-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="cb0d7-113">Die Zeichenfolgen in der **MAPIERROR-Struktur,** die im  _lppMAPIError-Parameter_ zurückgegeben wird, sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="cb0d7-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="cb0d7-114">Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="cb0d7-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="cb0d7-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="cb0d7-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="cb0d7-116">[out] Zeiger auf einen Zeiger auf die zurückgegebene **MAPIERROR-Struktur,** die Versions-, Komponenten- und Kontextinformationen für den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="cb0d7-116">[out] Pointer to a pointer to the returned **MAPIERROR** structure containing version, component, and context information for the error.</span></span> <span data-ttu-id="cb0d7-117">Der  _lppMAPIError-Parameter_ kann auf NULL festgelegt werden, wenn keine **MAPIERROR-Struktur** mit entsprechenden Informationen bereitgestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="cb0d7-117">The  _lppMAPIError_ parameter can be set to NULL if a **MAPIERROR** structure with appropriate information cannot be provided.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cb0d7-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cb0d7-118">Return value</span></span>

<span data-ttu-id="cb0d7-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="cb0d7-119">S_OK</span></span> 
  
> <span data-ttu-id="cb0d7-120">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="cb0d7-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="cb0d7-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="cb0d7-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="cb0d7-122">Entweder wurde MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt Unicode nicht, oder MAPI_UNICODE nicht festgelegt, und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="cb0d7-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation only supports Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cb0d7-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cb0d7-123">Remarks</span></span>

<span data-ttu-id="cb0d7-124">Die **IMAPITable::GetLastError-Methode** gibt detaillierte Informationen zu einem vorherigen Methodenaufruf zurück, der fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="cb0d7-124">The **IMAPITable::GetLastError** method returns detailed information, if available, about a prior method call that failed.</span></span> <span data-ttu-id="cb0d7-125">Diese Informationen können in einer Nachricht oder in einem Dialogfeld angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="cb0d7-125">This information can be displayed in a message or a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="cb0d7-126">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="cb0d7-126">Notes to callers</span></span>

<span data-ttu-id="cb0d7-127">Rufen **Sie GetLastError** auf, wenn Dem Benutzer Informationen zu einem Fehler anzeigen müssen.</span><span class="sxs-lookup"><span data-stu-id="cb0d7-127">Call **GetLastError** whenever you need to display information about an error to the user.</span></span> 
  
<span data-ttu-id="cb0d7-128">Sie können die [MAPIERROR-Struktur](mapierror.md) verwenden, auf die der  _lppMAPIError-Parameter_ verweist, wenn das Tabellenobjekt nur dann eins liefert, wenn **GetLastError** S_OK.</span><span class="sxs-lookup"><span data-stu-id="cb0d7-128">You can make use of the [MAPIERROR](mapierror.md) structure pointed to by the  _lppMAPIError_ parameter if the table object supplies one only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="cb0d7-129">Manchmal kann die Tabellenimplementierung nicht bestimmen, was der letzte Fehler war oder hat nichts mehr über den Fehler zu melden.</span><span class="sxs-lookup"><span data-stu-id="cb0d7-129">Sometimes the table implementation cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="cb0d7-130">In diesem Fall ist der Zeiger bei  _lppMAPIError_ auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cb0d7-130">In this situation, the pointer at  _lppMAPIError_ is set to NULL.</span></span> 
  
<span data-ttu-id="cb0d7-131">Rufen Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) auf, um den für die **MAPIERROR-Struktur** zugewiesenen Arbeitsspeicher frei zu geben.</span><span class="sxs-lookup"><span data-stu-id="cb0d7-131">To release all the memory allocated for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="cb0d7-132">Weitere Informationen zur **GetLastError-Methode** finden Sie unter [MAPI Extended Errors](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="cb0d7-132">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cb0d7-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb0d7-133">See also</span></span>



[<span data-ttu-id="cb0d7-134">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="cb0d7-134">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="cb0d7-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="cb0d7-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="cb0d7-136">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cb0d7-136">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

