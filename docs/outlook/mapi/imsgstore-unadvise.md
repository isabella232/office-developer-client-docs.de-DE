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
ms.openlocfilehash: 72a26875802b2b7f94261f11e78fe560e9cc49d3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583428"
---
# <a name="imsgstoreunadvise"></a><span data-ttu-id="bea57-103">IMsgStore::Unadvise</span><span class="sxs-lookup"><span data-stu-id="bea57-103">IMsgStore::Unadvise</span></span>

  
  
<span data-ttu-id="bea57-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bea57-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bea57-105">Bricht ab, das Senden von Benachrichtigungen, die zuvor mit einem Aufruf der Methode [IMsgStore::Advise](imsgstore-advise.md) eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="bea57-105">Cancels the sending of notifications previously set up with a call to the [IMsgStore::Advise](imsgstore-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="bea57-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bea57-106">Parameters</span></span>

 <span data-ttu-id="bea57-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="bea57-107">_ulConnection_</span></span>
  
> <span data-ttu-id="bea57-108">[in] Die Nummer eines aktiven benachrichtigungsregistrierung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="bea57-108">[in] The connection number associated with an active notification registration.</span></span> <span data-ttu-id="bea57-109">Der Wert der _UlConnection_ muss von einem vorherigen Aufruf der **IMsgStore::Advise** -Methode zurückgegeben wurde, haben.</span><span class="sxs-lookup"><span data-stu-id="bea57-109">The value of  _ulConnection_ must have been returned by a previous call to the **IMsgStore::Advise** method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="bea57-110">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="bea57-110">Return value</span></span>

<span data-ttu-id="bea57-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="bea57-111">S_OK</span></span> 
  
> <span data-ttu-id="bea57-112">Die Registrierung wurde erfolgreich abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="bea57-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bea57-113">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="bea57-113">Remarks</span></span>

<span data-ttu-id="bea57-114">Die **IMsgStore::Unadvise** -Methode hebt die Registrierung ein für die Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="bea57-114">The **IMsgStore::Unadvise** method cancels a registration for notification.</span></span> <span data-ttu-id="bea57-115">**Unadvise** -Versionen der Zeiger auf des Anrufers advise-Empfänger, die sie in der **Advise** -Aufruf für die Registrierung verwendet erhalten.</span><span class="sxs-lookup"><span data-stu-id="bea57-115">**Unadvise** releases its pointer to the caller's advise sink, which it received in the **Advise** call used for registration.</span></span> 
  
<span data-ttu-id="bea57-116">Im Allgemeinen ruft **Unadvise** Advise-Empfänger [IUnknown](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) -Methode während des Anrufs **Unadvise** .</span><span class="sxs-lookup"><span data-stu-id="bea57-116">Generally, **Unadvise** calls the advise sink's [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) method during the **Unadvise** call.</span></span> <span data-ttu-id="bea57-117">Wenn ein anderer Thread wird gerade Advise-Empfänger [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode aufrufen, wird jedoch **Release** -Aufruf verzögert, bis die **OnNotify** -Methode zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="bea57-117">However, if another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bea57-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bea57-118">See also</span></span>



[<span data-ttu-id="bea57-119">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="bea57-119">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="bea57-120">IMsgStore::Advise</span><span class="sxs-lookup"><span data-stu-id="bea57-120">IMsgStore::Advise</span></span>](imsgstore-advise.md)
  
[<span data-ttu-id="bea57-121">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="bea57-121">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

