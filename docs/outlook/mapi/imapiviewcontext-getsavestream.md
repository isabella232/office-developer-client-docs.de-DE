---
title: IMAPIViewContextGetSaveStream
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetSaveStream
api_type:
- COM
ms.assetid: 8316bfa1-3077-401f-aa1e-e9492aca12a8
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7981dc8550485aa22859c4a8dc25541bedf1217c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792502"
---
# <a name="imapiviewcontextgetsavestream"></a><span data-ttu-id="10673-103">IMAPIViewContext::GetSaveStream</span><span class="sxs-lookup"><span data-stu-id="10673-103">IMAPIViewContext::GetSaveStream</span></span>

  
  
<span data-ttu-id="10673-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="10673-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="10673-105">Ruft einen Datenstrom zum Speichern der aktuellen Nachricht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="10673-105">Retrieves a stream to be used for saving the current message.</span></span>
  
```cpp
HRESULT GetSaveStream(
ULONG FAR * pulFlags,
ULONG FAR * pulFormat,
LPSTREAM FAR * ppstm
);
```

## <a name="parameters"></a><span data-ttu-id="10673-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="10673-106">Parameters</span></span>

 <span data-ttu-id="10673-107">_pulFlags_</span><span class="sxs-lookup"><span data-stu-id="10673-107">_pulFlags_</span></span>
  
> <span data-ttu-id="10673-108">[out] Zeiger auf eine Bitmaske aus Flags, die steuert, wie der Nachrichtentext gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="10673-108">[out] Pointer to a bitmask of flags that controls how the message text should be saved.</span></span> <span data-ttu-id="10673-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="10673-109">The following flag can be set:</span></span>
    
<span data-ttu-id="10673-110">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="10673-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="10673-111">Der Meldungstext wird im Unicode-Format gespeichert.</span><span class="sxs-lookup"><span data-stu-id="10673-111">The message text is saved in Unicode format.</span></span> <span data-ttu-id="10673-112">Wenn die Option MAPI_UNICODE nicht festgelegt ist, wird der Text im ANSI-Format gespeichert.</span><span class="sxs-lookup"><span data-stu-id="10673-112">If the MAPI_UNICODE flag is not set, the text is saved in ANSI format.</span></span>
    
 <span data-ttu-id="10673-113">_pulFormat_</span><span class="sxs-lookup"><span data-stu-id="10673-113">_pulFormat_</span></span>
  
> <span data-ttu-id="10673-114">[out] Zeiger auf eine Bitmaske aus Flags, die das Format des gespeicherten Texts steuert.</span><span class="sxs-lookup"><span data-stu-id="10673-114">[out] Pointer to a bitmask of flags that controls the format of the saved text.</span></span> <span data-ttu-id="10673-115">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="10673-115">The following flags can be set:</span></span>
    
<span data-ttu-id="10673-116">SAVE_FORMAT_RICHTEXT</span><span class="sxs-lookup"><span data-stu-id="10673-116">SAVE_FORMAT_RICHTEXT</span></span> 
  
> <span data-ttu-id="10673-117">Der Nachrichtentext wird als formatierter Text im Rich Text Format (RTF) gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="10673-117">The message text is to be saved as formatted text in the Rich Text Format (RTF).</span></span> 
    
<span data-ttu-id="10673-118">SAVE_FORMAT_TEXT</span><span class="sxs-lookup"><span data-stu-id="10673-118">SAVE_FORMAT_TEXT</span></span> 
  
> <span data-ttu-id="10673-119">Der Nachrichtentext wird als nur-Text gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="10673-119">The message text is to be saved as plain text.</span></span> 
    
 <span data-ttu-id="10673-120">_ppstm_</span><span class="sxs-lookup"><span data-stu-id="10673-120">_ppstm_</span></span>
  
> <span data-ttu-id="10673-121">[out] Zeiger auf einen Zeiger in das Stream-Objekt, das die gespeicherte Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="10673-121">[out] Pointer to a pointer to the stream that will contain the saved message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="10673-122">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="10673-122">Return value</span></span>

<span data-ttu-id="10673-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="10673-123">S_OK</span></span> 
  
> <span data-ttu-id="10673-124">Der Stream wurde erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="10673-124">The stream was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="10673-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="10673-125">Remarks</span></span>

<span data-ttu-id="10673-126">Formularobjekte aufrufen, die **IMAPIViewContext::GetSaveStream** -Methode, um einen Datenstrom ein Objekt abzurufen, die zur Unterstützung der der Handhabung des Verbs speichern unter im Formular-Viewer die **IStream** -Schnittstelle implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="10673-126">Form objects call the **IMAPIViewContext::GetSaveStream** method to retrieve a stream an object that implements the **IStream** interface to support the handling of the Save As verb in the form viewer.</span></span> <span data-ttu-id="10673-127">Die [IMAPIForm::DoVerb](imapiform-doverb.md) -Methode, die in dem Formular Server implementiert und von der Formular-Viewer zum Aufrufen eines Verbs aufgerufen, sollten keine zurückgegeben, bis die Nachricht vollständig in die entsprechenden Textformat konvertiert und in den entsprechenden Stream platziert.</span><span class="sxs-lookup"><span data-stu-id="10673-127">The [IMAPIForm::DoVerb](imapiform-doverb.md) method, which is implemented in the form server and called by the form viewer to invoke a verb, should not return until the message is fully converted into the appropriate text format and placed into the appropriate stream.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="10673-128">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="10673-128">Notes to callers</span></span>

<span data-ttu-id="10673-129">Nicht in das Stream-Objekt, auf die _Ppstm_ vor dem Aufruf von **GetSaveStream**schreiben.</span><span class="sxs-lookup"><span data-stu-id="10673-129">Do not write to the stream pointed to by  _ppstm_ before calling **GetSaveStream**.</span></span> <span data-ttu-id="10673-130">Wenn **GetSaveStream** zurückgegeben wird, sollten Sie die Position des Mauszeigers Seek nicht zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="10673-130">When **GetSaveStream** returns, do not reset the position of the seek pointer.</span></span> <span data-ttu-id="10673-131">Dieser Zeiger muss am Ende des Texts gespeicherte Nachricht bleiben.</span><span class="sxs-lookup"><span data-stu-id="10673-131">This pointer must remain at the end of the saved message text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="10673-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10673-132">See also</span></span>



[<span data-ttu-id="10673-133">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="10673-133">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)

