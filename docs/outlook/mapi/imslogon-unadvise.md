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
ms.openlocfilehash: 9172d4956e78ac31cd15d69e70d05c127a474ca5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317276"
---
# <a name="imslogonunadvise"></a><span data-ttu-id="bcb6b-103">IMSLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="bcb6b-103">IMSLogon::Unadvise</span></span>

  
  
<span data-ttu-id="bcb6b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bcb6b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bcb6b-105">Entfernt die Registrierung eines Objekts zur Benachrichtigung über Nachrichtenspeicheränderungen, die zuvor mithilfe eines Aufrufs der [IMSLogon::Advise-Methode erstellt](imslogon-advise.md) wurden.</span><span class="sxs-lookup"><span data-stu-id="bcb6b-105">Removes an object's registration for notification of message store changes previously established by using a call to the [IMSLogon::Advise](imslogon-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="bcb6b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bcb6b-106">Parameters</span></span>

 <span data-ttu-id="bcb6b-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="bcb6b-107">_ulConnection_</span></span>
  
> <span data-ttu-id="bcb6b-108">[in] Die Nummer der Registrierungsverbindung, die von einem Aufruf von **IMSLogon::Advise zurückgegeben wird.**</span><span class="sxs-lookup"><span data-stu-id="bcb6b-108">[in] The number of the registration connection returned by a call to **IMSLogon::Advise**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bcb6b-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bcb6b-109">Return value</span></span>

<span data-ttu-id="bcb6b-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="bcb6b-110">S_OK</span></span> 
  
> <span data-ttu-id="bcb6b-111">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="bcb6b-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bcb6b-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bcb6b-112">Remarks</span></span>

<span data-ttu-id="bcb6b-113">Nachrichtenspeicheranbieter implementieren die **IMSLogon::Unadvise-Methode,** um den Zeiger auf das im  _lpAdviseSink-Parameter_ im vorherigen Aufruf von **IMSLogon::Advise** übergebene Advise-Sink-Objekt frei zu geben, wodurch eine Benachrichtigungsregistrierung abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="bcb6b-113">Message store providers implement the **IMSLogon::Unadvise** method to release the pointer to the advise sink object passed in the  _lpAdviseSink_ parameter in the previous call to **IMSLogon::Advise**, thereby canceling a notification registration.</span></span> <span data-ttu-id="bcb6b-114">Im Rahmen des Verwerfens des Zeigers auf das advise-Sink-Objekt wird die [IUnknown::Release-Methode des](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) Objekts aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="bcb6b-114">As part of discarding the pointer to the advise sink object, the object's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method is called.</span></span> <span data-ttu-id="bcb6b-115">Im Allgemeinen **wird Release** während des **Unadvise-Aufrufs** aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="bcb6b-115">Generally, **Release** is called during the **Unadvise** call.</span></span> <span data-ttu-id="bcb6b-116">Wenn jedoch ein anderer Thread die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) für das Advise Sink-Objekt aufruft, wird der **Release-Aufruf** verzögert, bis die **OnNotify-Methode** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="bcb6b-116">However, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bcb6b-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bcb6b-117">See also</span></span>



[<span data-ttu-id="bcb6b-118">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="bcb6b-118">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="bcb6b-119">IMSLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="bcb6b-119">IMSLogon::Advise</span></span>](imslogon-advise.md)
  
[<span data-ttu-id="bcb6b-120">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bcb6b-120">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

