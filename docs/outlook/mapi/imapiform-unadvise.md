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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 826863e30ae39d3c8d523bd2dff84731bcf16971
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792151"
---
# <a name="imapiformunadvise"></a><span data-ttu-id="fb48d-103">IMAPIForm::Unadvise</span><span class="sxs-lookup"><span data-stu-id="fb48d-103">IMAPIForm::Unadvise</span></span>

  
  
<span data-ttu-id="fb48d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fb48d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fb48d-105">Eine Registrierung für Benachrichtigungen mit einem Formular Viewer zuvor durch Aufrufen von [IMAPIForm::Advise](imapiform-advise.md)hergestellt werden abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="fb48d-105">Cancels a registration for notifications with a form viewer previously established by calling [IMAPIForm::Advise](imapiform-advise.md).</span></span>
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="fb48d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb48d-106">Parameters</span></span>

 <span data-ttu-id="fb48d-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="fb48d-107">_ulConnection_</span></span>
  
> <span data-ttu-id="fb48d-108">[in] Eine Verbindungsnummer, die identifiziert die benachrichtigungsregistrierung abgebrochen werden.</span><span class="sxs-lookup"><span data-stu-id="fb48d-108">[in] A connection number that identifies the notification registration to be canceled.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fb48d-109">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="fb48d-109">Return value</span></span>

<span data-ttu-id="fb48d-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="fb48d-110">S_OK</span></span> 
  
> <span data-ttu-id="fb48d-111">Die Registrierung wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="fb48d-111">The registration was canceled.</span></span>
    
<span data-ttu-id="fb48d-112">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="fb48d-112">E_INVALIDARG</span></span> 
  
> <span data-ttu-id="fb48d-113">Die Nummer der _UlConnection_ -Parameter übergebenen stellt keine Registrierung ein gültiges dar.</span><span class="sxs-lookup"><span data-stu-id="fb48d-113">The connection number passed in the  _ulConnection_ parameter does not represent a valid registration.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="fb48d-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fb48d-114">Remarks</span></span>

<span data-ttu-id="fb48d-115">Formular Viewer rufen Sie die **IMAPIForm::Unadvise** -Methode, um eine Registrierung für Benachrichtigung abzubrechen, das sie zuerst die **IMAPIForm::Advise** -Methode festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fb48d-115">Form viewers call the **IMAPIForm::Unadvise** method to cancel a registration for notification that they first established by calling the **IMAPIForm::Advise** method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="fb48d-116">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="fb48d-116">Notes to implementers</span></span>

<span data-ttu-id="fb48d-117">Verwerfen der Zeiger, den Sie zur Ansicht des Formulars-Viewers halten advise-Empfänger durch seine [IUnknown](http://msdn.microsoft.com/de-de/library/ms682317%28v=VS.85%29.aspx) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="fb48d-117">Discard the pointer that you are holding to the form viewer's view advise sink by calling its [IUnknown::Release](http://msdn.microsoft.com/de-de/library/ms682317%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="fb48d-118">Im allgemeinen **Release** aufgerufen wird während des Anrufs **Unadvise** .</span><span class="sxs-lookup"><span data-stu-id="fb48d-118">Generally, **Release** is called during the **Unadvise** call.</span></span> <span data-ttu-id="fb48d-119">Wenn ein anderer Thread aufruft, eine der Methoden [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) ist für die Ansicht advise-Empfänger jedoch **Release** -Aufruf Verzögerung, bis die **IMAPIViewAdviseSink** -Methode zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="fb48d-119">However, if another thread is in the process of calling one of the [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) methods for the view advise sink, delay the **Release** call until the **IMAPIViewAdviseSink** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fb48d-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb48d-120">See also</span></span>



[<span data-ttu-id="fb48d-121">IMAPIForm::Advise</span><span class="sxs-lookup"><span data-stu-id="fb48d-121">IMAPIForm::Advise</span></span>](imapiform-advise.md)
  
[<span data-ttu-id="fb48d-122">IMAPIViewAdviseSink: IUnknown</span><span class="sxs-lookup"><span data-stu-id="fb48d-122">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)
  
[<span data-ttu-id="fb48d-123">IMAPIForm: IUnknown</span><span class="sxs-lookup"><span data-stu-id="fb48d-123">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)

