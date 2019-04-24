---
title: IMAPIViewAdviseSinkOnPrint
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnPrint
api_type:
- COM
ms.assetid: d16219a0-268c-428d-9f02-4f06eb5b6d7d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e66315042f8b5cd5aff0e4aa076588c9f312376a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328784"
---
# <a name="imapiviewadvisesinkonprint"></a><span data-ttu-id="1563a-103">IMAPIViewAdviseSink::OnPrint</span><span class="sxs-lookup"><span data-stu-id="1563a-103">IMAPIViewAdviseSink::OnPrint</span></span>

  
  
<span data-ttu-id="1563a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1563a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1563a-105">Benachrichtigt den Formular Betrachter über den Druckstatus eines Formulars.</span><span class="sxs-lookup"><span data-stu-id="1563a-105">Notifies the form viewer of the printing status of a form.</span></span>
  
```cpp
HRESULT OnPrint(
ULONG dwPageNumber,
HRESULT hrStatus
);
```

## <a name="parameters"></a><span data-ttu-id="1563a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1563a-106">Parameters</span></span>

 <span data-ttu-id="1563a-107">_dwPageNumber_</span><span class="sxs-lookup"><span data-stu-id="1563a-107">_dwPageNumber_</span></span>
  
> <span data-ttu-id="1563a-108">in Die Nummer der letzten Seite, die gedruckt wurde.</span><span class="sxs-lookup"><span data-stu-id="1563a-108">[in] Number of the last page printed.</span></span>
    
 <span data-ttu-id="1563a-109">_hrStatus_</span><span class="sxs-lookup"><span data-stu-id="1563a-109">_hrStatus_</span></span>
  
> <span data-ttu-id="1563a-110">in Ein HRESULT-Wert, der den Status des Druckauftrags angibt.</span><span class="sxs-lookup"><span data-stu-id="1563a-110">[in] An HRESULT value indicating the status of the print job.</span></span> <span data-ttu-id="1563a-111">Die folgenden Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="1563a-111">Possible values are:</span></span>
    
<span data-ttu-id="1563a-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="1563a-112">S_FALSE</span></span> 
  
> <span data-ttu-id="1563a-113">Der Druckauftrag wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="1563a-113">The printing job has finished successfully.</span></span>
    
<span data-ttu-id="1563a-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="1563a-114">S_OK</span></span> 
  
> <span data-ttu-id="1563a-115">Der Druckauftrag wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1563a-115">The printing job is in progress.</span></span>
    
<span data-ttu-id="1563a-116">NICHT</span><span class="sxs-lookup"><span data-stu-id="1563a-116">FAILED</span></span> 
  
> <span data-ttu-id="1563a-117">Der Druckauftrag wurde aufgrund eines Fehlers abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="1563a-117">The printing job was terminated due to a failure.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1563a-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1563a-118">Return value</span></span>

<span data-ttu-id="1563a-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="1563a-119">S_OK</span></span> 
  
> <span data-ttu-id="1563a-120">Die Benachrichtigung wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1563a-120">The notification succeeded.</span></span>
    
<span data-ttu-id="1563a-121">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="1563a-121">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="1563a-122">Der Benutzer hat den Vorgang abgebrochen, indem er in einem Dialogfeld auf die Schaltfläche Abbrechen geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="1563a-122">The user canceled the operation, typically by clicking the Cancel button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1563a-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1563a-123">Remarks</span></span>

<span data-ttu-id="1563a-124">Formularobjekte rufen beim Drucken die **IMAPIViewAdviseSink:: OnPrint** -Methode auf, um den Betrachter über den Druckfortschritt zu informieren.</span><span class="sxs-lookup"><span data-stu-id="1563a-124">Form objects call the **IMAPIViewAdviseSink::OnPrint** method while printing to inform the viewer of printing progress.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1563a-125">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="1563a-125">Notes to callers</span></span>

<span data-ttu-id="1563a-126">Wenn der Druckauftrag mehrere Seiten umfasst, können Sie **OnPrint** aufrufen, nachdem jede Seite gedruckt wurde.</span><span class="sxs-lookup"><span data-stu-id="1563a-126">If the printing job involves multiple pages, you can call **OnPrint** after each page is printed.</span></span> <span data-ttu-id="1563a-127">Legen Sie _dwPageNumber_ auf die Seite fest, die derzeit gedruckt wird, und _hrStatus_ auf S_OK.</span><span class="sxs-lookup"><span data-stu-id="1563a-127">Set  _dwPageNumber_ to the page currently being printed and  _hrStatus_ to S_OK.</span></span> <span data-ttu-id="1563a-128">Wenn der Druckauftrag abgeschlossen ist, rufen \*\*\*\* Sie OnPrint mit _dwPageNumber_ auf die letzte Seite gedruckt festgelegt und _hrStatus_ auf S_FALSE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1563a-128">When the printing job is complete, call **OnPrint** with  _dwPageNumber_ set to the last page printed and  _hrStatus_ set to S_FALSE.</span></span> 
  
<span data-ttu-id="1563a-129">Weitere Informationen zu Formular Benachrichtigungen finden Sie unter [senden und empfangen von Formular Benachrichtigungen](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="1563a-129">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1563a-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1563a-130">See also</span></span>



[<span data-ttu-id="1563a-131">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1563a-131">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

