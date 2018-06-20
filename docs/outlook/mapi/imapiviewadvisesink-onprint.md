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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bf3eee43a70fbc4abf32b60379fc7b191bd9d513
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792481"
---
# <a name="imapiviewadvisesinkonprint"></a><span data-ttu-id="01784-103">IMAPIViewAdviseSink::OnPrint</span><span class="sxs-lookup"><span data-stu-id="01784-103">IMAPIViewAdviseSink::OnPrint</span></span>

  
  
<span data-ttu-id="01784-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="01784-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="01784-105">Benachrichtigt den Formular-Viewer des Status eines Formulars drucken.</span><span class="sxs-lookup"><span data-stu-id="01784-105">Notifies the form viewer of the printing status of a form.</span></span>
  
```cpp
HRESULT OnPrint(
ULONG dwPageNumber,
HRESULT hrStatus
);
```

## <a name="parameters"></a><span data-ttu-id="01784-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="01784-106">Parameters</span></span>

 <span data-ttu-id="01784-107">_dwPageNumber_</span><span class="sxs-lookup"><span data-stu-id="01784-107">_dwPageNumber_</span></span>
  
> <span data-ttu-id="01784-108">[in] Nummer der letzten Seite gedruckt.</span><span class="sxs-lookup"><span data-stu-id="01784-108">[in] Number of the last page printed.</span></span>
    
 <span data-ttu-id="01784-109">_hrStatus_</span><span class="sxs-lookup"><span data-stu-id="01784-109">_hrStatus_</span></span>
  
> <span data-ttu-id="01784-110">[in] Ein HRESULT-Wert, der den Status des Auftrags drucken.</span><span class="sxs-lookup"><span data-stu-id="01784-110">[in] An HRESULT value indicating the status of the print job.</span></span> <span data-ttu-id="01784-111">Die folgenden Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="01784-111">Possible values are:</span></span>
    
<span data-ttu-id="01784-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="01784-112">S_FALSE</span></span> 
  
> <span data-ttu-id="01784-113">Der Druckauftrag wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="01784-113">The printing job has finished successfully.</span></span>
    
<span data-ttu-id="01784-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="01784-114">S_OK</span></span> 
  
> <span data-ttu-id="01784-115">Der Druckauftrag wird gerade durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="01784-115">The printing job is in progress.</span></span>
    
<span data-ttu-id="01784-116">FEHLER BEI</span><span class="sxs-lookup"><span data-stu-id="01784-116">FAILED</span></span> 
  
> <span data-ttu-id="01784-117">Der Druckauftrag wurde aufgrund eines Fehlers abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="01784-117">The printing job was terminated due to a failure.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="01784-118">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="01784-118">Return value</span></span>

<span data-ttu-id="01784-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="01784-119">S_OK</span></span> 
  
> <span data-ttu-id="01784-120">Die Benachrichtigung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="01784-120">The notification succeeded.</span></span>
    
<span data-ttu-id="01784-121">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="01784-121">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="01784-122">Der Benutzer hat den Vorgang in der Regel durch Klicken auf die Schaltfläche zum Abbrechen in einem Dialogfeld abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="01784-122">The user canceled the operation, typically by clicking the Cancel button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="01784-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="01784-123">Remarks</span></span>

<span data-ttu-id="01784-124">Formularobjekte Aufrufen die **IMAPIViewAdviseSink::OnPrint** -Methode beim Drucken um den Viewer drucken Fortschritt zu informieren.</span><span class="sxs-lookup"><span data-stu-id="01784-124">Form objects call the **IMAPIViewAdviseSink::OnPrint** method while printing to inform the viewer of printing progress.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="01784-125">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="01784-125">Notes to callers</span></span>

<span data-ttu-id="01784-126">Wenn der Druckauftrag mehrere Seiten umfasst, können Sie **OnPrint** aufrufen, nachdem jeder Seite gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="01784-126">If the printing job involves multiple pages, you can call **OnPrint** after each page is printed.</span></span> <span data-ttu-id="01784-127">Legen Sie _DwPageNumber_ zur gegenwärtig gedruckte Seite und _HrStatus_ auf S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="01784-127">Set  _dwPageNumber_ to the page currently being printed and  _hrStatus_ to S_OK.</span></span> <span data-ttu-id="01784-128">Wenn der Druckauftrag abgeschlossen ist, legen Sie Anruf festgelegten **OnPrint** mit _DwPageNumber_ auf die letzte Seite gedruckt und _HrStatus_ auf S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="01784-128">When the printing job is complete, call **OnPrint** with  _dwPageNumber_ set to the last page printed and  _hrStatus_ set to S_FALSE.</span></span> 
  
<span data-ttu-id="01784-129">Weitere Informationen zum Formular Benachrichtigungen finden Sie unter [Senden und Empfangen von Formular Benachrichtigungen](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="01784-129">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="01784-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01784-130">See also</span></span>



[<span data-ttu-id="01784-131">IMAPIViewAdviseSink: IUnknown</span><span class="sxs-lookup"><span data-stu-id="01784-131">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)
