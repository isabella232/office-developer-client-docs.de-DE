---
title: IMAPISessionGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetLastError
api_type:
- COM
ms.assetid: 38cb3692-a5f8-403a-9615-9bd5868af23c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7477213ee854be1ae71b47a0c1b339c4c13b6f04
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338682"
---
# <a name="imapisessiongetlasterror"></a><span data-ttu-id="36ad7-103">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="36ad7-103">IMAPISession::GetLastError</span></span>

  
  
<span data-ttu-id="36ad7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36ad7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36ad7-105">Gibt eine [MAPIERROR](mapierror.md) -Struktur zurück, die Informationen zum vorherigen Sitzungsfehler enthält.</span><span class="sxs-lookup"><span data-stu-id="36ad7-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous session error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="36ad7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="36ad7-106">Parameters</span></span>

 <span data-ttu-id="36ad7-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="36ad7-107">_hResult_</span></span>
  
> <span data-ttu-id="36ad7-108">in Ein Handle für den im vorherigen Methodenaufruf generierten Fehlerwert.</span><span class="sxs-lookup"><span data-stu-id="36ad7-108">[in] A handle to the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="36ad7-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="36ad7-109">_ulFlags_</span></span>
  
> <span data-ttu-id="36ad7-110">in Eine Bitmaske von Flags, die den Typ der zurückgegebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="36ad7-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="36ad7-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="36ad7-111">The following flag can be set:</span></span>
    
<span data-ttu-id="36ad7-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="36ad7-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="36ad7-113">Die Zeichenfolgen in der **MAPIERROR** -Struktur, die im _lppMAPIError_ -Parameter zurückgegeben werden, sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="36ad7-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="36ad7-114">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="36ad7-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="36ad7-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="36ad7-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="36ad7-116">Out Ein Zeiger auf einen Zeiger auf eine **MAPIERROR** -Struktur, die Versions-, Komponenten-und Kontextinformationen für den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="36ad7-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="36ad7-117">Der Parameter _lppMAPIError_ kann auf NULL festgelegt werden, wenn MAPI keine geeigneten Informationen für eine **MAPIERROR** -Struktur bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="36ad7-117">The  _lppMAPIError_ parameter can be set to NULL if MAPI cannot supply appropriate information for a **MAPIERROR** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="36ad7-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="36ad7-118">Return value</span></span>

<span data-ttu-id="36ad7-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="36ad7-119">S_OK</span></span> 
  
> <span data-ttu-id="36ad7-120">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="36ad7-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="36ad7-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="36ad7-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="36ad7-122">Das MAPI_UNICODE-Flag wurde festgelegt, und die Sitzung unterstützt Unicode nicht.</span><span class="sxs-lookup"><span data-stu-id="36ad7-122">The MAPI_UNICODE flag was set and the session does not support Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="36ad7-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="36ad7-123">Remarks</span></span>

<span data-ttu-id="36ad7-124">Die **IMAPISession:: getlasterroraufzurufen** -Methode ruft Informationen zum letzten Fehler ab, der von einem Aufruf der **IMAPISession** -Methode zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="36ad7-124">The **IMAPISession::GetLastError** method retrieves information about the last error that was returned by an **IMAPISession** method call.</span></span> <span data-ttu-id="36ad7-125">Clients können Ihren Benutzern detaillierte Informationen zu dem Fehler bereitstellen, indem Sie diese Informationen in ein Dialogfeld einschließen.</span><span class="sxs-lookup"><span data-stu-id="36ad7-125">Clients can provide their users with detailed information about the error by including this information in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="36ad7-126">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="36ad7-126">Notes to callers</span></span>

<span data-ttu-id="36ad7-127">Sie können die **MAPIERROR** -Struktur verwenden, wenn MAPI eine bereitstellt, auf die durch den _lppMAPIError_ -Parameter verwiesen wird, nur, wenn **getlasterroraufzurufen** S_OK zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="36ad7-127">You can use the **MAPIERROR** structure, if MAPI supplies one, pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="36ad7-128">Manchmal kann MAPI nicht ermitteln, was der letzte Fehler war, oder er hat nichts mehr über den Fehler zu berichten.</span><span class="sxs-lookup"><span data-stu-id="36ad7-128">Sometimes MAPI cannot determine what the last error was, or it has nothing more to report about the error.</span></span> <span data-ttu-id="36ad7-129">In dieser Situation gibt **getlasterroraufzurufen** stattdessen einen Zeiger auf NULL in _lppMAPIError_ zurück.</span><span class="sxs-lookup"><span data-stu-id="36ad7-129">In this situation, **GetLastError** returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="36ad7-130">Weitere Informationen zur **getlasterroraufzurufen** -Methode finden Sie unter [MAPI Extended Errors](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="36ad7-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="36ad7-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="36ad7-131">See also</span></span>



[<span data-ttu-id="36ad7-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="36ad7-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="36ad7-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="36ad7-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="36ad7-134">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="36ad7-134">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="36ad7-135">Erweiterte MAPI-Fehler</span><span class="sxs-lookup"><span data-stu-id="36ad7-135">MAPI Extended Errors</span></span>](mapi-extended-errors.md)

