---
title: IMAPIViewContextGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetLastError
api_type:
- COM
ms.assetid: 3306e37a-2500-4281-96c3-ca0d5c81909d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bcd8e977d924bae170dcad27c672b963189cfa94
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424427"
---
# <a name="imapiviewcontextgetlasterror"></a><span data-ttu-id="15d84-103">IMAPIViewContext::GetLastError</span><span class="sxs-lookup"><span data-stu-id="15d84-103">IMAPIViewContext::GetLastError</span></span>

  
  
<span data-ttu-id="15d84-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15d84-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="15d84-105">Gibt eine [MAPIERROR](mapierror.md) -Struktur zurück, die Informationen über den vorherigen Fehler enthält, der für das View-Kontextobjekt auftritt.</span><span class="sxs-lookup"><span data-stu-id="15d84-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the view context object.</span></span> 
  
```cpp
HRESULT GetLastError(
HRESULT hResult,
ULONG ulFlags,
LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="15d84-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="15d84-106">Parameters</span></span>

 <span data-ttu-id="15d84-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="15d84-107">_hResult_</span></span>
  
> <span data-ttu-id="15d84-108">in HRESULT-Datentyp, der den im vorherigen Methodenaufruf generierten Fehlerwert enthält.</span><span class="sxs-lookup"><span data-stu-id="15d84-108">[in] HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="15d84-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="15d84-109">_ulFlags_</span></span>
  
> <span data-ttu-id="15d84-110">in Bitmaske von Flags, die den Typ der zurückgegebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="15d84-110">[in] Bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="15d84-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="15d84-111">The following flag can be set:</span></span>
    
<span data-ttu-id="15d84-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="15d84-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="15d84-113">Die Zeichenfolgen in der **MAPIERROR** -Struktur, die im _lppMAPIError_ -Parameter zurückgegeben werden, sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="15d84-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="15d84-114">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="15d84-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="15d84-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="15d84-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="15d84-116">Out Zeiger auf einen Zeiger auf die zurückgegebene **MAPIERROR** -Struktur, die Versions-, Komponenten-und Kontextinformationen für den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="15d84-116">[out] Pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="15d84-117">Dieser Parameter kann auf NULL festgelegt werden, wenn keine **MAPIERROR** -Struktur zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="15d84-117">This parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="15d84-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="15d84-118">Return value</span></span>

<span data-ttu-id="15d84-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="15d84-119">S_OK</span></span> 
  
> <span data-ttu-id="15d84-120">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="15d84-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="15d84-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="15d84-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="15d84-122">Entweder wurde das MAPI_UNICODE-Flag festgelegt, und **getlasterroraufzurufen** unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und **getlasterroraufzurufen** unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="15d84-122">Either the MAPI_UNICODE flag was set and **GetLastError** does not support Unicode, or MAPI_UNICODE was not set and **GetLastError** only supports Unicode.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="15d84-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15d84-123">Remarks</span></span>

<span data-ttu-id="15d84-124">Die **IMAPIViewContext:: getlasterroraufzurufen** -Methode liefert Informationen zu einem vorherigen Methodenaufruf, der fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="15d84-124">The **IMAPIViewContext::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="15d84-125">Aufrufer können Ihren Benutzern detaillierte Informationen zum Fehler bereitstellen, indem Sie die Daten aus der **MAPIERROR** -Struktur in ein Dialogfeld einschließen.</span><span class="sxs-lookup"><span data-stu-id="15d84-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="15d84-126">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="15d84-126">Notes to callers</span></span>

<span data-ttu-id="15d84-127">Sie können die **MAPIERROR** -Struktur verwenden, auf die durch den _lppMAPIError_ -Parameter verwiesen wird, wenn MAPI nur dann bereitstellt, wenn **getlasterroraufzurufen** S_OK zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="15d84-127">You can make use of the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter if MAPI supplies one only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="15d84-128">Manchmal kann MAPI nicht ermitteln, was der letzte Fehler war oder nicht mehr über den Fehler berichtet hat.</span><span class="sxs-lookup"><span data-stu-id="15d84-128">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="15d84-129">In dieser Situation wird stattdessen ein Zeiger auf NULL in _lppMAPIError_ zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="15d84-129">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="15d84-130">Weitere Informationen zur **getlasterroraufzurufen** -Methode finden Sie unter [MAPI Extended Errors](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="15d84-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="15d84-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15d84-131">See also</span></span>



[<span data-ttu-id="15d84-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="15d84-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="15d84-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="15d84-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="15d84-134">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="15d84-134">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)

