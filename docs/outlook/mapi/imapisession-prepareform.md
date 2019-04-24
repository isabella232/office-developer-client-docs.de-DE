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
ms.openlocfilehash: 3d8b1901123743b25b5bb9df174b297398c953b8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335764"
---
# <a name="imapisessionprepareform"></a><span data-ttu-id="55dc5-103">IMAPISession::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="55dc5-103">IMAPISession::PrepareForm</span></span>

  
  
<span data-ttu-id="55dc5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="55dc5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="55dc5-105">Erstellt ein numerisches Token, das von der [IMAPISession:: ShowForm](imapisession-showform.md) -Methode für den Zugriff auf eine Nachricht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="55dc5-105">Creates a numeric token that the [IMAPISession::ShowForm](imapisession-showform.md) method uses to access a message.</span></span> 
  
```cpp
HRESULT PrepareForm(
  LPCIID lpInterface,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMessageToken
);
```

## <a name="parameters"></a><span data-ttu-id="55dc5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="55dc5-106">Parameters</span></span>

 <span data-ttu-id="55dc5-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="55dc5-107">_lpInterface_</span></span>
  
> <span data-ttu-id="55dc5-108">in Ein Zeiger auf die Schnittstellen-ID (IID), die die Schnittstelle darstellt, die für den Zugriff auf die Nachricht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="55dc5-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message.</span></span> <span data-ttu-id="55dc5-109">Übergeben von **null** -Ergebnissen in der Standardschnittstelle oder [IMessage](imessageimapiprop.md), wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="55dc5-109">Passing **null** results in the standard interface, or [IMessage](imessageimapiprop.md), being used.</span></span> <span data-ttu-id="55dc5-110">Der _lpInterface_ -Parameter muss **null** oder IID_IMessage sein.</span><span class="sxs-lookup"><span data-stu-id="55dc5-110">The  _lpInterface_ parameter must be **null** or IID_IMessage.</span></span> 
    
 <span data-ttu-id="55dc5-111">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="55dc5-111">_lpMessage_</span></span>
  
> <span data-ttu-id="55dc5-112">in Ein Zeiger auf die Nachricht, die im Formular angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="55dc5-112">[in] A pointer to the message to be displayed in the form.</span></span>
    
 <span data-ttu-id="55dc5-113">_lpulMessageToken_</span><span class="sxs-lookup"><span data-stu-id="55dc5-113">_lpulMessageToken_</span></span>
  
> <span data-ttu-id="55dc5-114">Out Ein Zeiger auf ein Nachrichten Token, das von der **IMAPISession:: ShowForm** -Methode verwendet wird, um auf die Nachricht zuzugreifen, auf die von _lpMessage_verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="55dc5-114">[out] A pointer to a message token, which is used by the **IMAPISession::ShowForm** method to access the message pointed to by  _lpMessage_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="55dc5-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="55dc5-115">Return value</span></span>

<span data-ttu-id="55dc5-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="55dc5-116">S_OK</span></span> 
  
> <span data-ttu-id="55dc5-117">Die Formular Vorbereitung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="55dc5-117">The form preparation was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="55dc5-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55dc5-118">Remarks</span></span>

<span data-ttu-id="55dc5-119">Die **IMAPISession::P repareform** -Methode erstellt ein Nachrichten Token für die Nachricht, auf die durch den _lpMessage_ -Parameter verwiesen wird, und ruft die [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) -Methode der Nachricht auf.</span><span class="sxs-lookup"><span data-stu-id="55dc5-119">The **IMAPISession::PrepareForm** method creates a message token for the message pointed to by the  _lpMessage_ parameter and calls the message's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="55dc5-120">Dieses Token wird im _ulMessageToken_ -Parameter an **IMAPISession:: ShowForm**übergeben.</span><span class="sxs-lookup"><span data-stu-id="55dc5-120">This token is passed in the  _ulMessageToken_ parameter to **IMAPISession::ShowForm**.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="55dc5-121">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="55dc5-121">Notes to callers</span></span>

<span data-ttu-id="55dc5-122">Wenn der Aufruf von **PrepareForm** erfolgreich ist, veröffentlichen Sie die Nachricht, auf die durch _lpMessage_ verwiesen wird, indem Sie die [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) -Methode aufrufen, bevor Sie **ShowForm**aufrufen.</span><span class="sxs-lookup"><span data-stu-id="55dc5-122">If the call to **PrepareForm** succeeds, release the message pointed to by  _lpMessage_ by calling its [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method before you call **ShowForm**.</span></span> <span data-ttu-id="55dc5-123">Wenn Sie die Nachricht nicht freigeben, bevor Sie **ShowForm** aufrufen, kann dies zu Speicherverlusten führen.</span><span class="sxs-lookup"><span data-stu-id="55dc5-123">Failure to release the message before you call **ShowForm** can cause memory leaks.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="55dc5-124">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="55dc5-124">MFCMAPI reference</span></span>

<span data-ttu-id="55dc5-125">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="55dc5-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="55dc5-126">**Datei**</span><span class="sxs-lookup"><span data-stu-id="55dc5-126">**File**</span></span>|<span data-ttu-id="55dc5-127">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="55dc5-127">**Function**</span></span>|<span data-ttu-id="55dc5-128">**Comment**</span><span class="sxs-lookup"><span data-stu-id="55dc5-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="55dc5-129">MAPIFormFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="55dc5-129">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="55dc5-130">OpenMessageModal</span><span class="sxs-lookup"><span data-stu-id="55dc5-130">OpenMessageModal</span></span>  <br/> |<span data-ttu-id="55dc5-131">MFCMAPI verwendet die **IMAPISession::P repareform** -Methode zusammen mit **IMAPISession:: ShowForm**, um eine Nachricht in einem modalen Formular anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="55dc5-131">MFCMAPI uses the **IMAPISession::PrepareForm** method, along with **IMAPISession::ShowForm**, to display a message in a modal form.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="55dc5-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55dc5-132">See also</span></span>



[<span data-ttu-id="55dc5-133">IMAPISession::ShowForm</span><span class="sxs-lookup"><span data-stu-id="55dc5-133">IMAPISession::ShowForm</span></span>](imapisession-showform.md)
  
[<span data-ttu-id="55dc5-134">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="55dc5-134">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="55dc5-135">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="55dc5-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

