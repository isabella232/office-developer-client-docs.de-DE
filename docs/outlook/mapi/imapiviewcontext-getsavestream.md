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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 68eb74f53d6cee4661c98604ec2ea37609e20ab5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408425"
---
# <a name="imapiviewcontextgetsavestream"></a><span data-ttu-id="526df-103">IMAPIViewContext::GetSaveStream</span><span class="sxs-lookup"><span data-stu-id="526df-103">IMAPIViewContext::GetSaveStream</span></span>

  
  
<span data-ttu-id="526df-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="526df-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="526df-105">Ruft einen Stream ab, der zum Speichern der aktuellen Nachricht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="526df-105">Retrieves a stream to be used for saving the current message.</span></span>
  
```cpp
HRESULT GetSaveStream(
ULONG FAR * pulFlags,
ULONG FAR * pulFormat,
LPSTREAM FAR * ppstm
);
```

## <a name="parameters"></a><span data-ttu-id="526df-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="526df-106">Parameters</span></span>

 <span data-ttu-id="526df-107">_pulFlags_</span><span class="sxs-lookup"><span data-stu-id="526df-107">_pulFlags_</span></span>
  
> <span data-ttu-id="526df-108">Out Zeiger auf eine Bitmaske von Flags, die steuert, wie der Nachrichtentext gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="526df-108">[out] Pointer to a bitmask of flags that controls how the message text should be saved.</span></span> <span data-ttu-id="526df-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="526df-109">The following flag can be set:</span></span>
    
<span data-ttu-id="526df-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="526df-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="526df-111">Der Nachrichtentext wird im Unicode-Format gespeichert.</span><span class="sxs-lookup"><span data-stu-id="526df-111">The message text is saved in Unicode format.</span></span> <span data-ttu-id="526df-112">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, wird der Text im ANSI-Format gespeichert.</span><span class="sxs-lookup"><span data-stu-id="526df-112">If the MAPI_UNICODE flag is not set, the text is saved in ANSI format.</span></span>
    
 <span data-ttu-id="526df-113">_pulFormat_</span><span class="sxs-lookup"><span data-stu-id="526df-113">_pulFormat_</span></span>
  
> <span data-ttu-id="526df-114">Out Zeiger auf eine Bitmaske von Flags, die das Format des gespeicherten Texts steuert.</span><span class="sxs-lookup"><span data-stu-id="526df-114">[out] Pointer to a bitmask of flags that controls the format of the saved text.</span></span> <span data-ttu-id="526df-115">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="526df-115">The following flags can be set:</span></span>
    
<span data-ttu-id="526df-116">SAVE_FORMAT_RICHTEXT</span><span class="sxs-lookup"><span data-stu-id="526df-116">SAVE_FORMAT_RICHTEXT</span></span> 
  
> <span data-ttu-id="526df-117">Der Nachrichtentext soll als formatierter Text im Rich-Text-Format (RTF) gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="526df-117">The message text is to be saved as formatted text in the Rich Text Format (RTF).</span></span> 
    
<span data-ttu-id="526df-118">SAVE_FORMAT_TEXT</span><span class="sxs-lookup"><span data-stu-id="526df-118">SAVE_FORMAT_TEXT</span></span> 
  
> <span data-ttu-id="526df-119">Der Nachrichtentext soll als nur-Text gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="526df-119">The message text is to be saved as plain text.</span></span> 
    
 <span data-ttu-id="526df-120">_ppstm_</span><span class="sxs-lookup"><span data-stu-id="526df-120">_ppstm_</span></span>
  
> <span data-ttu-id="526df-121">Out Zeiger auf einen Zeiger auf den Stream, der die gespeicherte Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="526df-121">[out] Pointer to a pointer to the stream that will contain the saved message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="526df-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="526df-122">Return value</span></span>

<span data-ttu-id="526df-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="526df-123">S_OK</span></span> 
  
> <span data-ttu-id="526df-124">Der Datenstrom wurde erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="526df-124">The stream was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="526df-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="526df-125">Remarks</span></span>

<span data-ttu-id="526df-126">Formularobjekte rufen die **IMAPIViewContext:: GetSaveStream** -Methode auf, um ein Stream-Objekt abzurufen, das die **IStream** -Schnittstelle implementiert, um die Behandlung des Save as-Verbs im Formular-Viewer zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="526df-126">Form objects call the **IMAPIViewContext::GetSaveStream** method to retrieve a stream an object that implements the **IStream** interface to support the handling of the Save As verb in the form viewer.</span></span> <span data-ttu-id="526df-127">Die [IMAPIForm::D overb](imapiform-doverb.md) -Methode, die auf dem Formularserver implementiert und vom Formular Betrachter aufgerufen wird, um ein Verb aufzurufen, sollte erst zurückgegeben werden, wenn die Nachricht vollständig in das entsprechende Text Format konvertiert und in den entsprechenden Stream verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="526df-127">The [IMAPIForm::DoVerb](imapiform-doverb.md) method, which is implemented in the form server and called by the form viewer to invoke a verb, should not return until the message is fully converted into the appropriate text format and placed into the appropriate stream.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="526df-128">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="526df-128">Notes to callers</span></span>

<span data-ttu-id="526df-129">Schreiben Sie nicht in den Stream, auf den von _ppstm_ verwiesen wird, bevor Sie **GetSaveStream**aufrufen.</span><span class="sxs-lookup"><span data-stu-id="526df-129">Do not write to the stream pointed to by  _ppstm_ before calling **GetSaveStream**.</span></span> <span data-ttu-id="526df-130">Wenn **GetSaveStream** zurückgegeben wird, setzen Sie die Position des Seek-Zeigers nicht zurück.</span><span class="sxs-lookup"><span data-stu-id="526df-130">When **GetSaveStream** returns, do not reset the position of the seek pointer.</span></span> <span data-ttu-id="526df-131">Dieser Zeiger muss am Ende des gespeicherten Nachrichtentexts bleiben.</span><span class="sxs-lookup"><span data-stu-id="526df-131">This pointer must remain at the end of the saved message text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="526df-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="526df-132">See also</span></span>



[<span data-ttu-id="526df-133">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="526df-133">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)

