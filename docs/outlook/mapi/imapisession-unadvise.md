---
title: IMAPISessionUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.Unadvise
api_type:
- COM
ms.assetid: 5e608cb0-808d-4418-8521-71dcbce8cdff
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 25f80ddce60ab5a8966a62761d234accafbb54be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792334"
---
# <a name="imapisessionunadvise"></a><span data-ttu-id="0b879-103">IMAPISession::Unadvise</span><span class="sxs-lookup"><span data-stu-id="0b879-103">IMAPISession::Unadvise</span></span>

  
  
<span data-ttu-id="0b879-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0b879-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0b879-105">Bricht ab, das Senden von Benachrichtigungen, die zuvor mit einem Aufruf der Methode [IMAPISession::Advise](imapisession-advise.md) eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="0b879-105">Cancels the sending of notifications previously set up with a call to the [IMAPISession::Advise](imapisession-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="0b879-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b879-106">Parameters</span></span>

 <span data-ttu-id="0b879-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="0b879-107">_ulConnection_</span></span>
  
> <span data-ttu-id="0b879-108">[in] Eine Verbindung Zahl mit einer aktiven benachrichtigungsregistrierung verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="0b879-108">[in] A connection number associated with an active notification registration.</span></span> <span data-ttu-id="0b879-109">Der Wert der _UlConnection_ muss durch einen vorherigen Aufruf von **IMAPISession::Advise**zurückgegeben wurde, haben.</span><span class="sxs-lookup"><span data-stu-id="0b879-109">The value of  _ulConnection_ must have been returned by a previous call to **IMAPISession::Advise**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0b879-110">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="0b879-110">Return value</span></span>

<span data-ttu-id="0b879-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="0b879-111">S_OK</span></span> 
  
> <span data-ttu-id="0b879-112">Die Registrierung wurde erfolgreich abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="0b879-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0b879-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0b879-113">Remarks</span></span>

<span data-ttu-id="0b879-114">Die **IMAPISession::Unadvise** -Methode hebt die Registrierung ein für die Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="0b879-114">The **IMAPISession::Unadvise** method cancels a registration for notification.</span></span> <span data-ttu-id="0b879-115">**Unadvise** -Versionen der Zeiger auf des Anrufers advise-Empfänger, die sie in der **Advise** -Aufruf für die Registrierung verwendet erhalten.</span><span class="sxs-lookup"><span data-stu-id="0b879-115">**Unadvise** releases its pointer to the caller's advise sink, which it received in the **Advise** call used for registration.</span></span> 
  
<span data-ttu-id="0b879-116">Im Allgemeinen ruft **Unadvise** Advise-Empfänger [IUnknown](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) -Methode während des Anrufs **Unadvise** .</span><span class="sxs-lookup"><span data-stu-id="0b879-116">Generally, **Unadvise** calls the advise sink's [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) method during the **Unadvise** call.</span></span> <span data-ttu-id="0b879-117">Wenn ein anderer Thread wird gerade Advise-Empfänger [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode aufrufen, wird jedoch **Release** -Aufruf verzögert, bis die **OnNotify** -Methode zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="0b879-117">However, if another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0b879-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b879-118">See also</span></span>



[<span data-ttu-id="0b879-119">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="0b879-119">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="0b879-120">IMAPISession::Advise</span><span class="sxs-lookup"><span data-stu-id="0b879-120">IMAPISession::Advise</span></span>](imapisession-advise.md)
  
[<span data-ttu-id="0b879-121">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="0b879-121">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)
