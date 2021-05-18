---
title: IMsgStoreUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.Unadvise
api_type:
- COM
ms.assetid: 1394039b-d509-49a5-8421-b7362d906879
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f85b662b7fe710c66a2e69dd3cd3db22e3283ddb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309723"
---
# <a name="imsgstoreunadvise"></a><span data-ttu-id="df46e-103">IMsgStore::Unadvise</span><span class="sxs-lookup"><span data-stu-id="df46e-103">IMsgStore::Unadvise</span></span>

  
  
<span data-ttu-id="df46e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df46e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df46e-105">Bricht das Senden von Benachrichtigungen ab, die zuvor mit einem Aufruf der [IMsgStore::Advise-Methode eingerichtet](imsgstore-advise.md) wurden.</span><span class="sxs-lookup"><span data-stu-id="df46e-105">Cancels the sending of notifications previously set up with a call to the [IMsgStore::Advise](imsgstore-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="df46e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="df46e-106">Parameters</span></span>

 <span data-ttu-id="df46e-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="df46e-107">_ulConnection_</span></span>
  
> <span data-ttu-id="df46e-108">[in] Die Verbindungsnummer, die einer aktiven Benachrichtigungsregistrierung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="df46e-108">[in] The connection number associated with an active notification registration.</span></span> <span data-ttu-id="df46e-109">Der Wert von  _ulConnection_ muss von einem vorherigen Aufruf der **IMsgStore::Advise-Methode zurückgegeben** worden sein.</span><span class="sxs-lookup"><span data-stu-id="df46e-109">The value of  _ulConnection_ must have been returned by a previous call to the **IMsgStore::Advise** method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="df46e-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="df46e-110">Return value</span></span>

<span data-ttu-id="df46e-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="df46e-111">S_OK</span></span> 
  
> <span data-ttu-id="df46e-112">Die Registrierung wurde erfolgreich abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="df46e-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="df46e-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="df46e-113">Remarks</span></span>

<span data-ttu-id="df46e-114">Die **IMsgStore::Unadvise-Methode** bricht eine Registrierung zur Benachrichtigung ab.</span><span class="sxs-lookup"><span data-stu-id="df46e-114">The **IMsgStore::Unadvise** method cancels a registration for notification.</span></span> <span data-ttu-id="df46e-115">**Unadvise** gibt seinen Zeiger auf die Ratensenke des Anrufers frei, die er im Zur Registrierung verwendeten **Anruf "Raten"** erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="df46e-115">**Unadvise** releases its pointer to the caller's advise sink, which it received in the **Advise** call used for registration.</span></span> 
  
<span data-ttu-id="df46e-116">Im Allgemeinen **ruft Unadvise** die [IUnknown::Release-Methode](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) der Ratensenke während des **Unadvise-Aufrufs** auf.</span><span class="sxs-lookup"><span data-stu-id="df46e-116">Generally, **Unadvise** calls the advise sink's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method during the **Unadvise** call.</span></span> <span data-ttu-id="df46e-117">Wenn jedoch ein anderer Thread die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) der Ratensenke aufruft, wird der **Release-Aufruf** verzögert, bis die **OnNotify-Methode** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="df46e-117">However, if another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="df46e-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df46e-118">See also</span></span>



[<span data-ttu-id="df46e-119">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="df46e-119">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="df46e-120">IMsgStore::Advise</span><span class="sxs-lookup"><span data-stu-id="df46e-120">IMsgStore::Advise</span></span>](imsgstore-advise.md)
  
[<span data-ttu-id="df46e-121">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="df46e-121">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

