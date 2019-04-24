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
# <a name="imsgstoreunadvise"></a><span data-ttu-id="0efce-103">IMsgStore::Unadvise</span><span class="sxs-lookup"><span data-stu-id="0efce-103">IMsgStore::Unadvise</span></span>

  
  
<span data-ttu-id="0efce-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0efce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0efce-105">Bricht das Senden von Benachrichtigungen ab, die zuvor mit einem Aufruf der [IMsgStore:: Advise](imsgstore-advise.md) -Methode eingerichtet wurden.</span><span class="sxs-lookup"><span data-stu-id="0efce-105">Cancels the sending of notifications previously set up with a call to the [IMsgStore::Advise](imsgstore-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="0efce-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0efce-106">Parameters</span></span>

 <span data-ttu-id="0efce-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="0efce-107">_ulConnection_</span></span>
  
> <span data-ttu-id="0efce-108">in Die Verbindungsnummer, die mit einer aktiven Benachrichtigungs Registrierung verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="0efce-108">[in] The connection number associated with an active notification registration.</span></span> <span data-ttu-id="0efce-109">Der Wert von _ulConnection_ muss von einem vorherigen Aufruf der **IMsgStore:: Advise** -Methode zurückgegeben worden sein.</span><span class="sxs-lookup"><span data-stu-id="0efce-109">The value of  _ulConnection_ must have been returned by a previous call to the **IMsgStore::Advise** method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0efce-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0efce-110">Return value</span></span>

<span data-ttu-id="0efce-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="0efce-111">S_OK</span></span> 
  
> <span data-ttu-id="0efce-112">Die Registrierung wurde erfolgreich abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="0efce-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0efce-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0efce-113">Remarks</span></span>

<span data-ttu-id="0efce-114">Die **IMsgStore:: Unadvise** -Methode bricht eine Registrierung für die Benachrichtigung ab.</span><span class="sxs-lookup"><span data-stu-id="0efce-114">The **IMsgStore::Unadvise** method cancels a registration for notification.</span></span> <span data-ttu-id="0efce-115">**Unadvise** gibt den Zeiger auf die Advise-Senke des Anrufers frei, die er im für die Registrierung verwendeten **Advise** -Aufruf erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="0efce-115">**Unadvise** releases its pointer to the caller's advise sink, which it received in the **Advise** call used for registration.</span></span> 
  
<span data-ttu-id="0efce-116">Im allgemeinen \*\*\*\* ruft Unadvise während des Unadvise-Aufrufs die [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) -Methode der Advise-Senke auf. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="0efce-116">Generally, **Unadvise** calls the advise sink's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method during the **Unadvise** call.</span></span> <span data-ttu-id="0efce-117">Wenn jedoch ein anderer Thread gerade die [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) -Methode der Advise-Senke aufruft, wird der **Freigabe** Aufruf verzögert, bis \*\*\*\* die OnNotify-Methode zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0efce-117">However, if another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0efce-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0efce-118">See also</span></span>



[<span data-ttu-id="0efce-119">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="0efce-119">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="0efce-120">IMsgStore::Advise</span><span class="sxs-lookup"><span data-stu-id="0efce-120">IMsgStore::Advise</span></span>](imsgstore-advise.md)
  
[<span data-ttu-id="0efce-121">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="0efce-121">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

