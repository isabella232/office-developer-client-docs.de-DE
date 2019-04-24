---
title: IMAPIFormUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.Unadvise
api_type:
- COM
ms.assetid: fdda45e2-631d-404c-8af4-bce68df0968b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 770ceb7af98f5271baad65043e013feb353d231a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329470"
---
# <a name="imapiformunadvise"></a><span data-ttu-id="b012c-103">IMAPIForm::Unadvise</span><span class="sxs-lookup"><span data-stu-id="b012c-103">IMAPIForm::Unadvise</span></span>

  
  
<span data-ttu-id="b012c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b012c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b012c-105">Bricht eine Registrierung für Benachrichtigungen mit einem Formular Betrachter ab, der zuvor durch Aufrufen von [IMAPIForm:: Advise](imapiform-advise.md)eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="b012c-105">Cancels a registration for notifications with a form viewer previously established by calling [IMAPIForm::Advise](imapiform-advise.md).</span></span>
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="b012c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b012c-106">Parameters</span></span>

 <span data-ttu-id="b012c-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="b012c-107">_ulConnection_</span></span>
  
> <span data-ttu-id="b012c-108">in Eine Verbindungsnummer, die die zu abgebrochene Benachrichtigungs Registrierung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="b012c-108">[in] A connection number that identifies the notification registration to be canceled.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b012c-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b012c-109">Return value</span></span>

<span data-ttu-id="b012c-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="b012c-110">S_OK</span></span> 
  
> <span data-ttu-id="b012c-111">Die Registrierung wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="b012c-111">The registration was canceled.</span></span>
    
<span data-ttu-id="b012c-112">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="b012c-112">E_INVALIDARG</span></span> 
  
> <span data-ttu-id="b012c-113">Die im _ulConnection_ -Parameter übergebene Verbindungsnummer stellt keine gültige Registrierung dar.</span><span class="sxs-lookup"><span data-stu-id="b012c-113">The connection number passed in the  _ulConnection_ parameter does not represent a valid registration.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b012c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b012c-114">Remarks</span></span>

<span data-ttu-id="b012c-115">Formular Betrachter rufen die **IMAPIForm:: Unadvise** -Methode auf, um eine Registrierung für eine Benachrichtigung abzubrechen, die Sie zuerst durch Aufrufen der **IMAPIForm:: Advise** -Methode festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="b012c-115">Form viewers call the **IMAPIForm::Unadvise** method to cancel a registration for notification that they first established by calling the **IMAPIForm::Advise** method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="b012c-116">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="b012c-116">Notes to implementers</span></span>

<span data-ttu-id="b012c-117">VerWerfen Sie den Zeiger, den Sie in der View Advise-Senke des Formular Viewers halten, durch Aufrufen der [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) -Methode.</span><span class="sxs-lookup"><span data-stu-id="b012c-117">Discard the pointer that you are holding to the form viewer's view advise sink by calling its [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="b012c-118">Im Allgemeinen wird die **Freigabe** während des **Unadvise** -Aufrufs aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="b012c-118">Generally, **Release** is called during the **Unadvise** call.</span></span> <span data-ttu-id="b012c-119">Wenn jedoch ein anderer Thread gerade eine der [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) -Methoden für die View Advise-Senke aufruft, verzögern Sie den **Release** -Aufruf, bis die **IMAPIViewAdviseSink** -Methode zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b012c-119">However, if another thread is in the process of calling one of the [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) methods for the view advise sink, delay the **Release** call until the **IMAPIViewAdviseSink** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b012c-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b012c-120">See also</span></span>



[<span data-ttu-id="b012c-121">IMAPIForm::Advise</span><span class="sxs-lookup"><span data-stu-id="b012c-121">IMAPIForm::Advise</span></span>](imapiform-advise.md)
  
[<span data-ttu-id="b012c-122">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b012c-122">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)
  
[<span data-ttu-id="b012c-123">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b012c-123">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)

