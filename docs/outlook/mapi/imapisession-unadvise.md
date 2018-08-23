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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3b582b48773b9f6f1a6f46f9c0e4c6dcb9782b86
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592066"
---
# <a name="imapisessionunadvise"></a><span data-ttu-id="a8935-103">IMAPISession::Unadvise</span><span class="sxs-lookup"><span data-stu-id="a8935-103">IMAPISession::Unadvise</span></span>

  
  
<span data-ttu-id="a8935-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8935-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8935-105">Bricht ab, das Senden von Benachrichtigungen, die zuvor mit einem Aufruf der Methode [IMAPISession::Advise](imapisession-advise.md) eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="a8935-105">Cancels the sending of notifications previously set up with a call to the [IMAPISession::Advise](imapisession-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="a8935-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8935-106">Parameters</span></span>

 <span data-ttu-id="a8935-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="a8935-107">_ulConnection_</span></span>
  
> <span data-ttu-id="a8935-108">[in] Eine Verbindung Zahl mit einer aktiven benachrichtigungsregistrierung verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="a8935-108">[in] A connection number associated with an active notification registration.</span></span> <span data-ttu-id="a8935-109">Der Wert der _UlConnection_ muss durch einen vorherigen Aufruf von **IMAPISession::Advise**zurückgegeben wurde, haben.</span><span class="sxs-lookup"><span data-stu-id="a8935-109">The value of  _ulConnection_ must have been returned by a previous call to **IMAPISession::Advise**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a8935-110">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="a8935-110">Return value</span></span>

<span data-ttu-id="a8935-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="a8935-111">S_OK</span></span> 
  
> <span data-ttu-id="a8935-112">Die Registrierung wurde erfolgreich abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="a8935-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a8935-113">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="a8935-113">Remarks</span></span>

<span data-ttu-id="a8935-114">Die **IMAPISession::Unadvise** -Methode hebt die Registrierung ein für die Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="a8935-114">The **IMAPISession::Unadvise** method cancels a registration for notification.</span></span> <span data-ttu-id="a8935-115">**Unadvise** -Versionen der Zeiger auf des Anrufers advise-Empfänger, die sie in der **Advise** -Aufruf für die Registrierung verwendet erhalten.</span><span class="sxs-lookup"><span data-stu-id="a8935-115">**Unadvise** releases its pointer to the caller's advise sink, which it received in the **Advise** call used for registration.</span></span> 
  
<span data-ttu-id="a8935-116">Im Allgemeinen ruft **Unadvise** Advise-Empfänger [IUnknown](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) -Methode während des Anrufs **Unadvise** .</span><span class="sxs-lookup"><span data-stu-id="a8935-116">Generally, **Unadvise** calls the advise sink's [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) method during the **Unadvise** call.</span></span> <span data-ttu-id="a8935-117">Wenn ein anderer Thread wird gerade Advise-Empfänger [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode aufrufen, wird jedoch **Release** -Aufruf verzögert, bis die **OnNotify** -Methode zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="a8935-117">However, if another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a8935-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8935-118">See also</span></span>



[<span data-ttu-id="a8935-119">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="a8935-119">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="a8935-120">IMAPISession::Advise</span><span class="sxs-lookup"><span data-stu-id="a8935-120">IMAPISession::Advise</span></span>](imapisession-advise.md)
  
[<span data-ttu-id="a8935-121">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a8935-121">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)

