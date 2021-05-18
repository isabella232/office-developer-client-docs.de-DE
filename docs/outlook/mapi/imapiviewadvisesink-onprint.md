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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406171"
---
# <a name="imapiviewadvisesinkonprint"></a><span data-ttu-id="349f0-103">IMAPIViewAdviseSink::OnPrint</span><span class="sxs-lookup"><span data-stu-id="349f0-103">IMAPIViewAdviseSink::OnPrint</span></span>

  
  
<span data-ttu-id="349f0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="349f0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="349f0-105">Benachrichtigt die Formularanzeige über den Druckstatus eines Formulars.</span><span class="sxs-lookup"><span data-stu-id="349f0-105">Notifies the form viewer of the printing status of a form.</span></span>
  
```cpp
HRESULT OnPrint(
ULONG dwPageNumber,
HRESULT hrStatus
);
```

## <a name="parameters"></a><span data-ttu-id="349f0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="349f0-106">Parameters</span></span>

 <span data-ttu-id="349f0-107">_dwPageNumber_</span><span class="sxs-lookup"><span data-stu-id="349f0-107">_dwPageNumber_</span></span>
  
> <span data-ttu-id="349f0-108">[in] Die Nummer der letzten gedruckten Seite.</span><span class="sxs-lookup"><span data-stu-id="349f0-108">[in] Number of the last page printed.</span></span>
    
 <span data-ttu-id="349f0-109">_hrStatus_</span><span class="sxs-lookup"><span data-stu-id="349f0-109">_hrStatus_</span></span>
  
> <span data-ttu-id="349f0-110">[in] Ein HRESULT-Wert, der den Status des Druckauftrags angibt.</span><span class="sxs-lookup"><span data-stu-id="349f0-110">[in] An HRESULT value indicating the status of the print job.</span></span> <span data-ttu-id="349f0-111">Die folgenden Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="349f0-111">Possible values are:</span></span>
    
<span data-ttu-id="349f0-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="349f0-112">S_FALSE</span></span> 
  
> <span data-ttu-id="349f0-113">Der Druckauftrag wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="349f0-113">The printing job has finished successfully.</span></span>
    
<span data-ttu-id="349f0-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="349f0-114">S_OK</span></span> 
  
> <span data-ttu-id="349f0-115">Der Druckauftrag wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="349f0-115">The printing job is in progress.</span></span>
    
<span data-ttu-id="349f0-116">FAILED</span><span class="sxs-lookup"><span data-stu-id="349f0-116">FAILED</span></span> 
  
> <span data-ttu-id="349f0-117">Der Druckauftrag wurde aufgrund eines Fehlers beendet.</span><span class="sxs-lookup"><span data-stu-id="349f0-117">The printing job was terminated due to a failure.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="349f0-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="349f0-118">Return value</span></span>

<span data-ttu-id="349f0-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="349f0-119">S_OK</span></span> 
  
> <span data-ttu-id="349f0-120">Die Benachrichtigung ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="349f0-120">The notification succeeded.</span></span>
    
<span data-ttu-id="349f0-121">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="349f0-121">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="349f0-122">Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die Schaltfläche Abbrechen in einem Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="349f0-122">The user canceled the operation, typically by clicking the Cancel button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="349f0-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="349f0-123">Remarks</span></span>

<span data-ttu-id="349f0-124">Formularobjekte rufen die **IMAPIViewAdviseSink::OnPrint-Methode** beim Drucken auf, um den Betrachter über den Druckfortschritt zu informieren.</span><span class="sxs-lookup"><span data-stu-id="349f0-124">Form objects call the **IMAPIViewAdviseSink::OnPrint** method while printing to inform the viewer of printing progress.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="349f0-125">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="349f0-125">Notes to callers</span></span>

<span data-ttu-id="349f0-126">Wenn der Druckauftrag mehrere Seiten umfasst, können Sie **OnPrint** aufrufen, nachdem jede Seite gedruckt wurde.</span><span class="sxs-lookup"><span data-stu-id="349f0-126">If the printing job involves multiple pages, you can call **OnPrint** after each page is printed.</span></span> <span data-ttu-id="349f0-127">Legen  _Sie dwPageNumber_ auf die Seite, die gerade gedruckt wird, und  _hrStatus_ auf S_OK.</span><span class="sxs-lookup"><span data-stu-id="349f0-127">Set  _dwPageNumber_ to the page currently being printed and  _hrStatus_ to S_OK.</span></span> <span data-ttu-id="349f0-128">Wenn der Druckauftrag abgeschlossen ist, rufen Sie **OnPrint** auf,  _während dwPageNumber_ auf die letzte gedruckte Seite festgelegt ist, und  _hrStatus_ auf S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="349f0-128">When the printing job is complete, call **OnPrint** with  _dwPageNumber_ set to the last page printed and  _hrStatus_ set to S_FALSE.</span></span> 
  
<span data-ttu-id="349f0-129">Weitere Informationen zu Formularbenachrichtigungen finden Sie unter Senden und Empfangen [von Formularbenachrichtigungen](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="349f0-129">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="349f0-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="349f0-130">See also</span></span>



[<span data-ttu-id="349f0-131">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="349f0-131">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

