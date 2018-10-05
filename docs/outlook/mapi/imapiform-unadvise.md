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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390471"
---
# <a name="imapiformunadvise"></a><span data-ttu-id="50050-103">IMAPIForm::Unadvise</span><span class="sxs-lookup"><span data-stu-id="50050-103">IMAPIForm::Unadvise</span></span>

  
  
<span data-ttu-id="50050-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50050-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50050-105">Eine Registrierung für Benachrichtigungen mit einem Formular Viewer zuvor durch Aufrufen von [IMAPIForm::Advise](imapiform-advise.md)hergestellt werden abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="50050-105">Cancels a registration for notifications with a form viewer previously established by calling [IMAPIForm::Advise](imapiform-advise.md).</span></span>
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="50050-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="50050-106">Parameters</span></span>

 <span data-ttu-id="50050-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="50050-107">_ulConnection_</span></span>
  
> <span data-ttu-id="50050-108">[in] Eine Verbindungsnummer, die identifiziert die benachrichtigungsregistrierung abgebrochen werden.</span><span class="sxs-lookup"><span data-stu-id="50050-108">[in] A connection number that identifies the notification registration to be canceled.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="50050-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="50050-109">Return value</span></span>

<span data-ttu-id="50050-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="50050-110">S_OK</span></span> 
  
> <span data-ttu-id="50050-111">Die Registrierung wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="50050-111">The registration was canceled.</span></span>
    
<span data-ttu-id="50050-112">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="50050-112">E_INVALIDARG</span></span> 
  
> <span data-ttu-id="50050-113">Die Nummer der _UlConnection_ -Parameter übergebenen stellt keine Registrierung ein gültiges dar.</span><span class="sxs-lookup"><span data-stu-id="50050-113">The connection number passed in the  _ulConnection_ parameter does not represent a valid registration.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="50050-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="50050-114">Remarks</span></span>

<span data-ttu-id="50050-115">Formular Viewer rufen Sie die **IMAPIForm::Unadvise** -Methode, um eine Registrierung für Benachrichtigung abzubrechen, das sie zuerst die **IMAPIForm::Advise** -Methode festgelegt.</span><span class="sxs-lookup"><span data-stu-id="50050-115">Form viewers call the **IMAPIForm::Unadvise** method to cancel a registration for notification that they first established by calling the **IMAPIForm::Advise** method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="50050-116">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="50050-116">Notes to implementers</span></span>

<span data-ttu-id="50050-117">Verwerfen der Zeiger, den Sie zur Ansicht des Formulars-Viewers halten advise-Empfänger durch seine [IUnknown](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="50050-117">Discard the pointer that you are holding to the form viewer's view advise sink by calling its [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="50050-118">Im allgemeinen **Release** aufgerufen wird während des Anrufs **Unadvise** .</span><span class="sxs-lookup"><span data-stu-id="50050-118">Generally, **Release** is called during the **Unadvise** call.</span></span> <span data-ttu-id="50050-119">Wenn ein anderer Thread aufruft, eine der Methoden [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) ist für die Ansicht advise-Empfänger jedoch **Release** -Aufruf Verzögerung, bis die **IMAPIViewAdviseSink** -Methode zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="50050-119">However, if another thread is in the process of calling one of the [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) methods for the view advise sink, delay the **Release** call until the **IMAPIViewAdviseSink** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="50050-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50050-120">See also</span></span>



[<span data-ttu-id="50050-121">IMAPIForm::Advise</span><span class="sxs-lookup"><span data-stu-id="50050-121">IMAPIForm::Advise</span></span>](imapiform-advise.md)
  
[<span data-ttu-id="50050-122">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="50050-122">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)
  
[<span data-ttu-id="50050-123">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="50050-123">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)

