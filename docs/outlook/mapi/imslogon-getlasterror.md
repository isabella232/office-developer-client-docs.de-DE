---
title: IMSLogonGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.GetLastError
api_type:
- COM
ms.assetid: 3e296f6d-4833-4c68-9b84-df0b09878474
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 472502d0f033370b06a69596944350152ab794f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425876"
---
# <a name="imslogongetlasterror"></a><span data-ttu-id="bee3d-103">IMSLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="bee3d-103">IMSLogon::GetLastError</span></span>

  
  
<span data-ttu-id="bee3d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bee3d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bee3d-105">Gibt eine [MAPIERROR](mapierror.md) -Struktur zurück, die Informationen zum letzten Fehler enthält, der für das Nachrichtenspeicherobjekt aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="bee3d-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for the message store object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="bee3d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bee3d-106">Parameters</span></span>

 <span data-ttu-id="bee3d-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="bee3d-107">_hResult_</span></span>
  
> <span data-ttu-id="bee3d-108">in Ein HRESULT-Datentyp, der den im vorherigen Methodenaufruf für das Nachrichtenspeicherobjekt generierten Fehlerwert enthält.</span><span class="sxs-lookup"><span data-stu-id="bee3d-108">[in] An HRESULT data type that contains the error value generated in the previous method call for the message store object.</span></span>
    
 <span data-ttu-id="bee3d-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bee3d-109">_ulFlags_</span></span>
  
> <span data-ttu-id="bee3d-110">in Eine Bitmaske von Flags, die den Typ der zurückgegebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="bee3d-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="bee3d-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="bee3d-111">The following flag can be set:</span></span>
    
<span data-ttu-id="bee3d-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bee3d-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="bee3d-113">Die Zeichenfolgen in der **MAPIERROR** -Struktur, die im _lppMAPIError_ -Parameter zurückgegeben werden, sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="bee3d-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="bee3d-114">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="bee3d-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="bee3d-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="bee3d-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="bee3d-116">Out Ein Zeiger auf einen Zeiger auf die zurückgegebene **MAPIERROR** -Struktur, die Versions-, Komponenten-und Kontextinformationen für den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="bee3d-116">[out] A pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="bee3d-117">Der _lppMAPIError_ -Parameter kann auf NULL festgelegt werden, wenn keine **MAPIERROR** zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="bee3d-117">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="bee3d-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bee3d-118">Return value</span></span>

<span data-ttu-id="bee3d-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="bee3d-119">S_OK</span></span> 
  
> <span data-ttu-id="bee3d-120">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="bee3d-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="bee3d-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="bee3d-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="bee3d-122">Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="bee3d-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bee3d-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bee3d-123">Remarks</span></span>

<span data-ttu-id="bee3d-124">Verwenden Sie die **IMSLogon:: getlasterroraufzurufen** -Methode, um Informationen abzurufen, die dem Benutzer in einer Nachricht bezüglich des letzten von einem Methodenaufruf für das Nachrichtenspeicherobjekt zurückgegebenen Fehlers angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bee3d-124">Use the **IMSLogon::GetLastError** method to retrieve information to display in a message to the user regarding the last error returned from a method call for the message store object.</span></span> 
  
<span data-ttu-id="bee3d-125">Um den gesamten von MAPI reservierten Arbeitsspeicher für die zurückgegebene **MAPIERROR** -Struktur freizugeben, müssen Clientanwendungen nur die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="bee3d-125">To release all the memory allocated by MAPI for the returned **MAPIERROR** structure, client applications need to call only the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="bee3d-126">Der Rückgabewert von **getlasterroraufzurufen** muss S_OK sein, damit eine Anwendung den **MAPIERROR**verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="bee3d-126">The return value from **GetLastError** must be S_OK for an application to use the **MAPIERROR**.</span></span> <span data-ttu-id="bee3d-127">Auch wenn der Rückgabewert S_OK ist, wird möglicherweise kein **MAPIERROR** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bee3d-127">Even if the return value is S_OK, a **MAPIERROR** might not be returned.</span></span> <span data-ttu-id="bee3d-128">Wenn die Implementierung nicht ermitteln kann, was der letzte Fehler war, oder wenn ein **MAPIERROR** für diesen Fehler nicht verfügbar ist, gibt **getlasterroraufzurufen** in _LPPMAPIERROR_ stattdessen einen Zeiger auf NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="bee3d-128">If the implementation cannot determine what the last error was, or if a **MAPIERROR** is not available for that error, **GetLastError** returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bee3d-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bee3d-129">See also</span></span>



[<span data-ttu-id="bee3d-130">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="bee3d-130">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="bee3d-131">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="bee3d-131">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="bee3d-132">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bee3d-132">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

