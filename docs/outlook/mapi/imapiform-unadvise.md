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
# <a name="imapiformunadvise"></a><span data-ttu-id="436ec-103">IMAPIForm::Unadvise</span><span class="sxs-lookup"><span data-stu-id="436ec-103">IMAPIForm::Unadvise</span></span>

  
  
<span data-ttu-id="436ec-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="436ec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="436ec-105">Bricht eine Registrierung für Benachrichtigungen bei einer zuvor durch Aufrufen von [IMAPIForm::Advise](imapiform-advise.md)eingerichteten Formularanzeige ab.</span><span class="sxs-lookup"><span data-stu-id="436ec-105">Cancels a registration for notifications with a form viewer previously established by calling [IMAPIForm::Advise](imapiform-advise.md).</span></span>
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="436ec-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="436ec-106">Parameters</span></span>

 <span data-ttu-id="436ec-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="436ec-107">_ulConnection_</span></span>
  
> <span data-ttu-id="436ec-108">[in] Eine Verbindungsnummer, die die Benachrichtigungsregistrierung identifiziert, die abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="436ec-108">[in] A connection number that identifies the notification registration to be canceled.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="436ec-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="436ec-109">Return value</span></span>

<span data-ttu-id="436ec-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="436ec-110">S_OK</span></span> 
  
> <span data-ttu-id="436ec-111">Die Registrierung wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="436ec-111">The registration was canceled.</span></span>
    
<span data-ttu-id="436ec-112">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="436ec-112">E_INVALIDARG</span></span> 
  
> <span data-ttu-id="436ec-113">Die im  _ulConnection-Parameter übergebene_ Verbindungsnummer stellt keine gültige Registrierung dar.</span><span class="sxs-lookup"><span data-stu-id="436ec-113">The connection number passed in the  _ulConnection_ parameter does not represent a valid registration.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="436ec-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="436ec-114">Remarks</span></span>

<span data-ttu-id="436ec-115">Formularbetrachter rufen die **IMAPIForm::Unadvise-Methode** auf, um eine Registrierung für Benachrichtigungen abbricht, die sie zuerst durch Aufrufen der **IMAPIForm::Advise-Methode eingerichtet** haben.</span><span class="sxs-lookup"><span data-stu-id="436ec-115">Form viewers call the **IMAPIForm::Unadvise** method to cancel a registration for notification that they first established by calling the **IMAPIForm::Advise** method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="436ec-116">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="436ec-116">Notes to implementers</span></span>

<span data-ttu-id="436ec-117">Verwerfen Sie den Zeiger, den Sie an der Ansichtsanzeige der Formularanzeige halten, indem Sie die [IUnknown::Release-Methode](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="436ec-117">Discard the pointer that you are holding to the form viewer's view advise sink by calling its [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="436ec-118">Im Allgemeinen **wird Release** während des **Unadvise-Aufrufs** aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="436ec-118">Generally, **Release** is called during the **Unadvise** call.</span></span> <span data-ttu-id="436ec-119">Wenn jedoch ein anderer Thread eine der [IMAPIViewAdviseSink-Methoden](imapiviewadvisesinkiunknown.md) für die Ansichtssenke aufruft, verzögern Sie den **Release-Aufruf,** bis die **IMAPIViewAdviseSink-Methode** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="436ec-119">However, if another thread is in the process of calling one of the [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) methods for the view advise sink, delay the **Release** call until the **IMAPIViewAdviseSink** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="436ec-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="436ec-120">See also</span></span>



[<span data-ttu-id="436ec-121">IMAPIForm::Advise</span><span class="sxs-lookup"><span data-stu-id="436ec-121">IMAPIForm::Advise</span></span>](imapiform-advise.md)
  
[<span data-ttu-id="436ec-122">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="436ec-122">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)
  
[<span data-ttu-id="436ec-123">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="436ec-123">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)

