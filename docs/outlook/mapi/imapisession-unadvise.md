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
ms.openlocfilehash: 98a5faca00f5877eb10110406875b46a69244d94
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335702"
---
# <a name="imapisessionunadvise"></a><span data-ttu-id="1b099-103">IMAPISession::Unadvise</span><span class="sxs-lookup"><span data-stu-id="1b099-103">IMAPISession::Unadvise</span></span>

  
  
<span data-ttu-id="1b099-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1b099-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1b099-105">Bricht das Senden von Benachrichtigungen ab, die zuvor mit einem Aufruf der [IMAPISession::Advise-Methode eingerichtet](imapisession-advise.md) wurden.</span><span class="sxs-lookup"><span data-stu-id="1b099-105">Cancels the sending of notifications previously set up with a call to the [IMAPISession::Advise](imapisession-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="1b099-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b099-106">Parameters</span></span>

 <span data-ttu-id="1b099-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="1b099-107">_ulConnection_</span></span>
  
> <span data-ttu-id="1b099-108">[in] Eine Verbindungsnummer, die einer aktiven Benachrichtigungsregistrierung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1b099-108">[in] A connection number associated with an active notification registration.</span></span> <span data-ttu-id="1b099-109">Der Wert von _ulConnection_ muss von einem vorherigen Aufruf von **IMAPISession::Advise zurückgegeben worden sein.**</span><span class="sxs-lookup"><span data-stu-id="1b099-109">The value of  _ulConnection_ must have been returned by a previous call to **IMAPISession::Advise**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1b099-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1b099-110">Return value</span></span>

<span data-ttu-id="1b099-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="1b099-111">S_OK</span></span> 
  
> <span data-ttu-id="1b099-112">Die Registrierung wurde erfolgreich abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="1b099-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1b099-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1b099-113">Remarks</span></span>

<span data-ttu-id="1b099-114">Die **IMAPISession::Unadvise-Methode** bricht eine Registrierung zur Benachrichtigung ab.</span><span class="sxs-lookup"><span data-stu-id="1b099-114">The **IMAPISession::Unadvise** method cancels a registration for notification.</span></span> <span data-ttu-id="1b099-115">**Unadvise** gibt seinen Zeiger auf die Ratensenke des Anrufers frei, die er im Zur Registrierung verwendeten **Anruf "Raten"** erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="1b099-115">**Unadvise** releases its pointer to the caller's advise sink, which it received in the **Advise** call used for registration.</span></span> 
  
<span data-ttu-id="1b099-116">Im Allgemeinen **ruft Unadvise** die [IUnknown::Release-Methode](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) der Ratensenke während des **Unadvise-Aufrufs** auf.</span><span class="sxs-lookup"><span data-stu-id="1b099-116">Generally, **Unadvise** calls the advise sink's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method during the **Unadvise** call.</span></span> <span data-ttu-id="1b099-117">Wenn jedoch ein anderer Thread die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) der Ratensenke aufruft, wird der **Release-Aufruf** verzögert, bis die **OnNotify-Methode** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1b099-117">However, if another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1b099-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1b099-118">See also</span></span>



[<span data-ttu-id="1b099-119">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="1b099-119">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="1b099-120">IMAPISession::Advise</span><span class="sxs-lookup"><span data-stu-id="1b099-120">IMAPISession::Advise</span></span>](imapisession-advise.md)
  
[<span data-ttu-id="1b099-121">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1b099-121">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)

