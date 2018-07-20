---
title: IMSLogonUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.Unadvise
api_type:
- COM
ms.assetid: 440d61c4-b69a-4010-a22b-0c9c5c376fbc
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 34c15ca4f7d81eeeee71fb0cb7e31085c75e5492
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792701"
---
# <a name="imslogonunadvise"></a><span data-ttu-id="3fab5-103">IMSLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="3fab5-103">IMSLogon::Unadvise</span></span>

  
  
<span data-ttu-id="3fab5-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3fab5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3fab5-105">Entfernt ein Objekt Anmeldungsseite für Benachrichtigung über Message Store Änderungen, die zuvor durch einen Aufruf an die [IMSLogon::Advise](imslogon-advise.md) -Methode festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3fab5-105">Removes an object's registration for notification of message store changes previously established by using a call to the [IMSLogon::Advise](imslogon-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="3fab5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3fab5-106">Parameters</span></span>

 <span data-ttu-id="3fab5-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="3fab5-107">_ulConnection_</span></span>
  
> <span data-ttu-id="3fab5-108">[in] Die Anzahl der Registrierung Verbindung durch einen Aufruf von **IMSLogon::Advise**zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3fab5-108">[in] The number of the registration connection returned by a call to **IMSLogon::Advise**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3fab5-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3fab5-109">Return value</span></span>

<span data-ttu-id="3fab5-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="3fab5-110">S_OK</span></span> 
  
> <span data-ttu-id="3fab5-111">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="3fab5-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3fab5-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3fab5-112">Remarks</span></span>

<span data-ttu-id="3fab5-113">Nachricht von nachrichtenspeicheranbietern implementierte die **IMSLogon::Unadvise** -Methode, um den Zeiger auf den im Parameter _LpAdviseSink_ im vorherigen Aufruf **IMSLogon::Advise**, wodurch Stornieren einer benachrichtigungs übergeben Advise-Empfängerobjekt freigeben Registrierung.</span><span class="sxs-lookup"><span data-stu-id="3fab5-113">Message store providers implement the **IMSLogon::Unadvise** method to release the pointer to the advise sink object passed in the  _lpAdviseSink_ parameter in the previous call to **IMSLogon::Advise**, thereby canceling a notification registration.</span></span> <span data-ttu-id="3fab5-114">Im Rahmen des Zeigers auf das Empfängerobjekt Advise verwerfen wird das Objekt [IUnknown](http://msdn.microsoft.com/de-de/library/ms682317%28v=VS.85%29.aspx) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="3fab5-114">As part of discarding the pointer to the advise sink object, the object's [IUnknown::Release](http://msdn.microsoft.com/de-de/library/ms682317%28v=VS.85%29.aspx) method is called.</span></span> <span data-ttu-id="3fab5-115">Im allgemeinen **Release** aufgerufen wird während des Anrufs **Unadvise** .</span><span class="sxs-lookup"><span data-stu-id="3fab5-115">Generally, **Release** is called during the **Unadvise** call.</span></span> <span data-ttu-id="3fab5-116">Ist ein anderer Thread die [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode für das Empfängerobjekt Advise aufruft, wird jedoch **Release** -Aufruf verzögert, bis die **OnNotify** -Methode zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="3fab5-116">However, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3fab5-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3fab5-117">See also</span></span>



[<span data-ttu-id="3fab5-118">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="3fab5-118">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="3fab5-119">IMSLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="3fab5-119">IMSLogon::Advise</span></span>](imslogon-advise.md)
  
[<span data-ttu-id="3fab5-120">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3fab5-120">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

