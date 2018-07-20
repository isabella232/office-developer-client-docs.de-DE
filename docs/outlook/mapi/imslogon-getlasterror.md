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
ms.openlocfilehash: a865a751f3e274008c7004315906d6705ba55161
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792690"
---
# <a name="imslogongetlasterror"></a><span data-ttu-id="fbc35-103">IMSLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="fbc35-103">IMSLogon::GetLastError</span></span>

  
  
<span data-ttu-id="fbc35-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fbc35-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fbc35-105">Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen über den letzten Fehler enthält, die für das Store-Nachrichtenspeicherobjekt aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="fbc35-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for the message store object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="fbc35-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fbc35-106">Parameters</span></span>

 <span data-ttu-id="fbc35-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="fbc35-107">_hResult_</span></span>
  
> <span data-ttu-id="fbc35-108">[in] Ein HRESULT-Datentyp, der den Fehlerwert generiert, die in der vorherigen Aufruf-Methode für die Nachricht Store-Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="fbc35-108">[in] An HRESULT data type that contains the error value generated in the previous method call for the message store object.</span></span>
    
 <span data-ttu-id="fbc35-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fbc35-109">_ulFlags_</span></span>
  
> <span data-ttu-id="fbc35-110">[in] Eine Bitmaske aus Flags, die den Typ des zurückgegebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="fbc35-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="fbc35-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="fbc35-111">The following flag can be set:</span></span>
    
<span data-ttu-id="fbc35-112">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fbc35-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="fbc35-113">Die Zeichenfolgen in der **MAPIERROR** -Struktur zurückgegeben, die im Parameter _LppMAPIError_ sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="fbc35-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="fbc35-114">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="fbc35-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="fbc35-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="fbc35-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="fbc35-116">[out] Ein Zeiger auf einen Zeiger auf das zurückgegebene **MAPIERROR** -Struktur, die Angaben zu Version, Komponente und Kontext für den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="fbc35-116">[out] A pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="fbc35-117">Der Parameter _LppMAPIError_ kann auf NULL festgelegt werden, wenn es keine **MAPIERROR ist** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fbc35-117">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fbc35-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fbc35-118">Return value</span></span>

<span data-ttu-id="fbc35-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="fbc35-119">S_OK</span></span> 
  
> <span data-ttu-id="fbc35-120">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="fbc35-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="fbc35-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="fbc35-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="fbc35-122">Entweder die Option MAPI_UNICODE festgelegt wurde und die Implementierung unterstützt keine Unicode oder Parameter MAPI_UNICODE nicht festgelegt wurde und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="fbc35-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fbc35-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fbc35-123">Remarks</span></span>

<span data-ttu-id="fbc35-124">Verwenden Sie die **IMSLogon::GetLastError** -Methode zum Abrufen von Informationen in einer Nachricht an den Benutzer über den letzten Fehler zurückgegeben, die von einem Methodenaufruf für das Objekt "Message" Store angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fbc35-124">Use the **IMSLogon::GetLastError** method to retrieve information to display in a message to the user regarding the last error returned from a method call for the message store object.</span></span> 
  
<span data-ttu-id="fbc35-125">Um alle für die zurückgegebene **MAPIERROR** -Struktur von MAPI reservierten Arbeitsspeicher freizugeben, müssen Clientanwendungen nur die Funktion [MAPIFreeBuffer](mapifreebuffer.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="fbc35-125">To release all the memory allocated by MAPI for the returned **MAPIERROR** structure, client applications need to call only the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="fbc35-126">Der Rückgabewert von **GetLastError** muss S_OK für eine Anwendung für die **MAPIERROR**verwenden.</span><span class="sxs-lookup"><span data-stu-id="fbc35-126">The return value from **GetLastError** must be S_OK for an application to use the **MAPIERROR**.</span></span> <span data-ttu-id="fbc35-127">Selbst wenn der Rückgabewert S_OK ist, kann ein **MAPIERROR** nicht zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="fbc35-127">Even if the return value is S_OK, a **MAPIERROR** might not be returned.</span></span> <span data-ttu-id="fbc35-128">Wenn die Implementierung nicht bestimmen kann, was letzten Fehlers wurde oder wenn ein **MAPIERROR** ist nicht verfügbar für Fehler; **GetLastError** einen Zeiger auf NULL in _LppMAPIError_ stattdessen zurück.</span><span class="sxs-lookup"><span data-stu-id="fbc35-128">If the implementation cannot determine what the last error was, or if a **MAPIERROR** is not available for that error, **GetLastError** returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fbc35-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fbc35-129">See also</span></span>



[<span data-ttu-id="fbc35-130">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="fbc35-130">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="fbc35-131">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="fbc35-131">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="fbc35-132">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fbc35-132">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

