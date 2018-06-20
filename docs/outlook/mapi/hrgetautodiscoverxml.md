---
title: HrGetAutoDiscoverXML
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrGetAutoDiscoverXML
api_type:
- COM
ms.assetid: 03691187-7c65-620b-576f-6ebe62a80830
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: da466fc9add8cbc385014782f31749d3b6522da9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791912"
---
# <a name="hrgetautodiscoverxml"></a><span data-ttu-id="d2444-103">HrGetAutoDiscoverXML</span><span class="sxs-lookup"><span data-stu-id="d2444-103">HrGetAutoDiscoverXML</span></span>

  
  
<span data-ttu-id="d2444-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d2444-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d2444-105">Gibt einen Stream Extensible Markup Language (XML), der Informationen aus den Auto-Discovery-Dienst eines Microsoft Exchange 2007-Servers abgerufen darstellt zurück.</span><span class="sxs-lookup"><span data-stu-id="d2444-105">Returns an Extensible Markup Language (XML) stream that represents information retrieved from the auto-discovery service of a Microsoft Exchange 2007 server.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d2444-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="d2444-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d2444-107">Vom exportiert werden:</span><span class="sxs-lookup"><span data-stu-id="d2444-107">Exported by:</span></span>  <br/> |<span data-ttu-id="d2444-108">olmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="d2444-108">olmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="d2444-109">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="d2444-109">Called by:</span></span>  <br/> |<span data-ttu-id="d2444-110">Client</span><span class="sxs-lookup"><span data-stu-id="d2444-110">Client</span></span>  <br/> |
|<span data-ttu-id="d2444-111">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="d2444-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="d2444-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="d2444-112">Outlook</span></span>  <br/> |
   
```cpp
HRESULT HrGetAutoDiscoverXML( 
    __in_z const WCHAR *pwzAddress, 
    __in_opt_z const WCHAR *pwzPassword, 
    __in_opt HANDLE hCancelEvent, 
    __in_opt ULONG ulFlags, 
    __out IStream** ppXmlStream); 

```

## <a name="parameters"></a><span data-ttu-id="d2444-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2444-113">Parameters</span></span>

 <span data-ttu-id="d2444-114">_pwzAddress_</span><span class="sxs-lookup"><span data-stu-id="d2444-114">_pwzAddress_</span></span>
  
> <span data-ttu-id="d2444-115">[in] Eine Null endende Simple Mail Transfer Protocol (SMTP) e-Mail-Adresse des Kontos ein, für die Sie die automatische Ermittlung Informationen abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="d2444-115">[in] A null-terminated Simple Mail Transfer Protocol (SMTP) email address of the account for which you want to retrieve the auto-discovery information.</span></span>
    
 <span data-ttu-id="d2444-116">_pwzPassword_</span><span class="sxs-lookup"><span data-stu-id="d2444-116">_pwzPassword_</span></span>
  
> <span data-ttu-id="d2444-117">[in] Ein optionales Kennwort für das Konto durch _PwzAddress_angegeben.</span><span class="sxs-lookup"><span data-stu-id="d2444-117">[in] An optional password for the account specified by  _pwzAddress_.</span></span> <span data-ttu-id="d2444-118">Beachten Sie, dass jedes beliebige Kennwort übergeben hat keine Auswirkung, wenn das durch _PwzAddress_ angegebene Konto ein Kennwort nicht erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="d2444-118">Note that passing any password has no effect if the account specified by  _pwzAddress_ does not require a password.</span></span> 
    
 <span data-ttu-id="d2444-119">_hCancelEvent_</span><span class="sxs-lookup"><span data-stu-id="d2444-119">_hCancelEvent_</span></span>
  
> <span data-ttu-id="d2444-120">[in] Ein nicht festgelegte Win32-Ereignishandle, das ist optional und kann verwendet werden, um den Vorgang abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="d2444-120">[in] An unset Win32 event handle that is optional and can be used to cancel the operation.</span></span> <span data-ttu-id="d2444-121">Um den Vorgang abzubrechen, legen Sie das Ereignis, und übergeben Sie das Ereignishandle als _hCancelEvent_; übergeben Sie **null** , wenn Sie nicht, um den Vorgang abzubrechen möchten.</span><span class="sxs-lookup"><span data-stu-id="d2444-121">To cancel the operation, set the event and pass the event handle as  _hCancelEvent_; pass **null** if you do not want to cancel the operation.</span></span> <span data-ttu-id="d2444-122">Beachten Sie, dass ein Wert übergeben, die ein Ereignishandle nicht darstellen hat keine Auswirkung und wird von der Funktion ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d2444-122">Note that passing a value that does not represent an event handle has no effect and is ignored by the function.</span></span> 
    
 <span data-ttu-id="d2444-123">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d2444-123">_ulFlags_</span></span>
  
> <span data-ttu-id="d2444-124">[in] Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d2444-124">[in] This parameter is not used.</span></span> <span data-ttu-id="d2444-125">Es muss 0 sein.</span><span class="sxs-lookup"><span data-stu-id="d2444-125">It must be 0.</span></span>
    
 <span data-ttu-id="d2444-126">_ppXmlStream_</span><span class="sxs-lookup"><span data-stu-id="d2444-126">_ppXmlStream_</span></span>
  
> <span data-ttu-id="d2444-127">[out] Ein Zeiger auf ein [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) -Objekt, das die AutoErmittlung XML enthält.</span><span class="sxs-lookup"><span data-stu-id="d2444-127">[out] A pointer to an [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) object that contains the autodiscovery XML.</span></span> <span data-ttu-id="d2444-128">Gibt **null** zurück, wenn der AutoErmittlung-Vorgang fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="d2444-128">Returns **null** if the autodiscovery operation fails.</span></span> <span data-ttu-id="d2444-129">Wenn Sie mit ihm fertig sind, müssen Sie [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) -Objekt freigeben.</span><span class="sxs-lookup"><span data-stu-id="d2444-129">You must release the [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) object when you are finished with it.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="d2444-130">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="d2444-130">Return values</span></span>

<span data-ttu-id="d2444-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="d2444-131">S_OK</span></span> 
  
- <span data-ttu-id="d2444-132">Der Funktionsaufruf ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="d2444-132">The function call is successful.</span></span>
    
<span data-ttu-id="d2444-133">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="d2444-133">E_INVALIDARG</span></span> 
  
-  <span data-ttu-id="d2444-134">_PwzAddress_ ist **null** oder ist keine gültige SMTP-Adresse, oder _PpXmlStream_ ist ein **null** -Zeiger auf eine [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="d2444-134">_pwzAddress_ is **null** or is not a valid SMTP address, or  _ppXmlStream_ is a **null** pointer to an [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) object.</span></span> 
    
<span data-ttu-id="d2444-135">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="d2444-135">MAPI_E_NOT_FOUND</span></span> 
  
- <span data-ttu-id="d2444-136">Clientcomputer ist nicht mit dem Netzwerk verbunden, Client-Computer ist nicht mit einem Microsoft Exchange 2007-Server verbunden, _PwzAddress_ ist nicht mit einem Konto auf einem Exchange 2007-Server oder _PwzAddress_ ist ein Konto, das Exchange nicht unterstützt Auto-Discovery-Dienst.</span><span class="sxs-lookup"><span data-stu-id="d2444-136">Client computer is not connected to the network, client computer is not connected to a Microsoft Exchange 2007 server,  _pwzAddress_ is not an account on an Exchange 2007 server, or  _pwzAddress_ is an account that does not support Exchange auto-discovery service.</span></span> 
    
<span data-ttu-id="d2444-137">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="d2444-137">MAPI_E_USER_CANCEL</span></span> 
  
- <span data-ttu-id="d2444-138">Ein Ereignishandle wurde übergeben, _hCancelEvent_ , um den Vorgang abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="d2444-138">An event handle has been passed to  _hCancelEvent_ to cancel the operation.</span></span> 
    
<span data-ttu-id="d2444-139">STRSAFE_E_INSUFFICIENT_BUFFER</span><span class="sxs-lookup"><span data-stu-id="d2444-139">STRSAFE_E_INSUFFICIENT_BUFFER</span></span>
  
- <span data-ttu-id="d2444-140">Der _PwzAddress_ oder _PwzPassword_ übergebene Wert ist zu lang, so, dass er den internen Puffer Größe 256 Bytes überschreitet.</span><span class="sxs-lookup"><span data-stu-id="d2444-140">The value passed to  _pwzAddress_ or  _pwzPassword_ is too long, such that it overflows the internal buffer of size 256 bytes.</span></span> 
    
