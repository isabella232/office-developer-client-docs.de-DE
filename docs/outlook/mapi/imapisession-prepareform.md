---
title: IMAPISessionPrepareForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.PrepareForm
api_type:
- COM
ms.assetid: 98c0eab1-fd7e-46c3-8619-ccd6dc7cf8f7
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 026a120406b714a50a9191e4761021693a250b94
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792319"
---
# <a name="imapisessionprepareform"></a><span data-ttu-id="6068d-103">IMAPISession::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="6068d-103">IMAPISession::PrepareForm</span></span>

  
  
<span data-ttu-id="6068d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6068d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6068d-105">Erstellt eine numerische Token, das die [IMAPISession::ShowForm](imapisession-showform.md) -Methode verwendet, um auf eine Nachricht zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="6068d-105">Creates a numeric token that the [IMAPISession::ShowForm](imapisession-showform.md) method uses to access a message.</span></span> 
  
```cpp
HRESULT PrepareForm(
  LPCIID lpInterface,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMessageToken
);
```

## <a name="parameters"></a><span data-ttu-id="6068d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6068d-106">Parameters</span></span>

 <span data-ttu-id="6068d-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="6068d-107">_lpInterface_</span></span>
  
> <span data-ttu-id="6068d-108">[in] Ein Zeiger auf die Schnittstelle-ID (IID), die die Schnittstelle zum Zugriff auf die Nachricht zu verwendende darstellt.</span><span class="sxs-lookup"><span data-stu-id="6068d-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message.</span></span> <span data-ttu-id="6068d-109">Übergeben von **null** führt in der standard-Benutzeroberfläche oder [IMessage](imessageimapiprop.md), verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6068d-109">Passing **null** results in the standard interface, or [IMessage](imessageimapiprop.md), being used.</span></span> <span data-ttu-id="6068d-110">Der Parameter _LpInterface_ muss **null** oder IID_IMessage sein.</span><span class="sxs-lookup"><span data-stu-id="6068d-110">The  _lpInterface_ parameter must be **null** or IID_IMessage.</span></span> 
    
 <span data-ttu-id="6068d-111">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="6068d-111">_lpMessage_</span></span>
  
> <span data-ttu-id="6068d-112">[in] Ein Zeiger auf die Nachricht, die im Formular angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6068d-112">[in] A pointer to the message to be displayed in the form.</span></span>
    
 <span data-ttu-id="6068d-113">_lpulMessageToken_</span><span class="sxs-lookup"><span data-stu-id="6068d-113">_lpulMessageToken_</span></span>
  
> <span data-ttu-id="6068d-114">[out] Ein Zeiger auf ein Token Nachricht, die von der **IMAPISession::ShowForm** -Methode zum Zugriff auf die Meldung _LpMessage_verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6068d-114">[out] A pointer to a message token, which is used by the **IMAPISession::ShowForm** method to access the message pointed to by  _lpMessage_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6068d-115">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="6068d-115">Return value</span></span>

<span data-ttu-id="6068d-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="6068d-116">S_OK</span></span> 
  
> <span data-ttu-id="6068d-117">Die Vorbereitung Formular war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="6068d-117">The form preparation was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6068d-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6068d-118">Remarks</span></span>

<span data-ttu-id="6068d-119">Die **IMAPISession::PrepareForm** -Methode erstellt eine Nachricht Token für die Meldung über den Parameter _LpMessage_ und die Nachricht [IUnknown:: AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="6068d-119">The **IMAPISession::PrepareForm** method creates a message token for the message pointed to by the  _lpMessage_ parameter and calls the message's [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="6068d-120">Dieses Token wird an **IMAPISession::ShowForm**im _UlMessageToken_ -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="6068d-120">This token is passed in the  _ulMessageToken_ parameter to **IMAPISession::ShowForm**.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6068d-121">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="6068d-121">Notes to callers</span></span>

<span data-ttu-id="6068d-122">Wenn der Aufruf von **PrepareForm** erfolgreich ist, Version der Meldung von _LpMessage_ dessen [IUnknown](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) -Methode aufrufen, bevor Sie **ShowForm aus**aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6068d-122">If the call to **PrepareForm** succeeds, release the message pointed to by  _lpMessage_ by calling its [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) method before you call **ShowForm**.</span></span> <span data-ttu-id="6068d-123">Installationsfehler, die Nachricht freigeben, bevor Sie **ShowForm aus** aufrufen kann Speicherverluste entstehen.</span><span class="sxs-lookup"><span data-stu-id="6068d-123">Failure to release the message before you call **ShowForm** can cause memory leaks.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6068d-124">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="6068d-124">MFCMAPI reference</span></span>

<span data-ttu-id="6068d-125">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="6068d-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6068d-126">**Datei**</span><span class="sxs-lookup"><span data-stu-id="6068d-126">**File**</span></span>|<span data-ttu-id="6068d-127">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="6068d-127">**Function**</span></span>|<span data-ttu-id="6068d-128">**Comment**</span><span class="sxs-lookup"><span data-stu-id="6068d-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6068d-129">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="6068d-129">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="6068d-130">OpenMessageModal</span><span class="sxs-lookup"><span data-stu-id="6068d-130">OpenMessageModal</span></span>  <br/> |<span data-ttu-id="6068d-131">MFCMAPI (engl.) verwendet die **IMAPISession::PrepareForm** -Methode, zusammen mit **IMAPISession::ShowForm**, um eine Nachricht in ein modales Formular anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6068d-131">MFCMAPI uses the **IMAPISession::PrepareForm** method, along with **IMAPISession::ShowForm**, to display a message in a modal form.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6068d-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6068d-132">See also</span></span>



[<span data-ttu-id="6068d-133">IMAPISession::ShowForm</span><span class="sxs-lookup"><span data-stu-id="6068d-133">IMAPISession::ShowForm</span></span>](imapisession-showform.md)
  
[<span data-ttu-id="6068d-134">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="6068d-134">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="6068d-135">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="6068d-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

