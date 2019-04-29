---
title: IProfAdminGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.GetLastError
api_type:
- COM
ms.assetid: bb161d7b-ae5b-4f8e-a506-8346ac5e583d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b6964ecde3a78bd1e9ce0ae1dcab0342c5a21a03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430773"
---
# <a name="iprofadmingetlasterror"></a><span data-ttu-id="9c60a-103">IProfAdmin::GetLastError</span><span class="sxs-lookup"><span data-stu-id="9c60a-103">IProfAdmin::GetLastError</span></span>

  
  
<span data-ttu-id="9c60a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9c60a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9c60a-105">Gibt eine [MAPIERROR](mapierror.md) -Struktur zurück, die Informationen zum vorherigen Fehler enthält, der in einem Profilverwaltungsobjekt aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="9c60a-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to a profile administration object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="9c60a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c60a-106">Parameters</span></span>

 <span data-ttu-id="9c60a-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="9c60a-107">_hResult_</span></span>
  
> <span data-ttu-id="9c60a-108">in Ein HRESULT-Datentyp, der den im vorherigen Methodenaufruf generierten Fehlerwert enthält.</span><span class="sxs-lookup"><span data-stu-id="9c60a-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="9c60a-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9c60a-109">_ulFlags_</span></span>
  
> <span data-ttu-id="9c60a-110">in Eine Bitmaske von Flags, die den Typ der zurückgegebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="9c60a-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="9c60a-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="9c60a-111">The following flag can be set:</span></span>
    
<span data-ttu-id="9c60a-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9c60a-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="9c60a-113">Die Zeichenfolgen in der [MAPIERROR](mapierror.md) -Struktur, die im _lppMAPIError_ -Parameter zurückgegeben werden, sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="9c60a-113">The strings in the [MAPIERROR](mapierror.md) structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="9c60a-114">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="9c60a-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="9c60a-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="9c60a-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="9c60a-116">Out Ein Zeiger auf einen Zeiger auf die **MAPIERROR** -Struktur, die Versions-, Komponenten-und Kontextinformationen für den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="9c60a-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="9c60a-117">Der _lppMAPIError_ -Parameter kann auf NULL festgelegt werden, wenn keine **MAPIERROR** -Struktur zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="9c60a-117">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9c60a-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9c60a-118">Return value</span></span>

<span data-ttu-id="9c60a-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="9c60a-119">S_OK</span></span> 
  
> <span data-ttu-id="9c60a-120">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="9c60a-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="9c60a-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="9c60a-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="9c60a-122">Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="9c60a-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9c60a-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9c60a-123">Remarks</span></span>

<span data-ttu-id="9c60a-124">Die **IProfAdmin:: getlasterroraufzurufen** -Methode ruft Informationen zum letzten Fehler ab, der von einem Methodenaufruf für das Profilverwaltungsobjekt zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="9c60a-124">The **IProfAdmin::GetLastError** method retrieves information about the last error returned from a method call for the profile administration object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9c60a-125">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="9c60a-125">Notes to callers</span></span>

<span data-ttu-id="9c60a-126">Sie können die **MAPIERROR** -Struktur verwenden, wenn MAPI eine bereitstellt, auf die durch den _lppMAPIError_ -Parameter verwiesen wird, nur, wenn **getlasterroraufzurufen** S_OK zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="9c60a-126">You can use the **MAPIERROR** structure, if MAPI supplies one, pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="9c60a-127">Manchmal kann MAPI nicht ermitteln, was der letzte Fehler war oder nicht mehr über den Fehler berichtet hat.</span><span class="sxs-lookup"><span data-stu-id="9c60a-127">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="9c60a-128">In dieser Situation wird in _lppMAPIError_ein Zeiger auf NULL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9c60a-128">In this situation, a pointer to NULL is returned in  _lppMAPIError_.</span></span> 
  
<span data-ttu-id="9c60a-129">Rufen Sie die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion auf, um den gesamten von MAPI zugeordneten Speicher für die **MAPIERROR** -Struktur freizugeben.</span><span class="sxs-lookup"><span data-stu-id="9c60a-129">To release all the memory allocated by MAPI for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="9c60a-130">Weitere Informationen zur **getlasterroraufzurufen** -Methode finden Sie unter [using Extended Errors](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="9c60a-130">For more information about the **GetLastError** method, see [Using Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9c60a-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c60a-131">See also</span></span>



[<span data-ttu-id="9c60a-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="9c60a-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="9c60a-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="9c60a-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="9c60a-134">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9c60a-134">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

