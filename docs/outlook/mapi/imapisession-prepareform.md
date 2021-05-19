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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3d8b1901123743b25b5bb9df174b297398c953b8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335764"
---
# <a name="imapisessionprepareform"></a><span data-ttu-id="2d916-103">IMAPISession::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="2d916-103">IMAPISession::PrepareForm</span></span>

  
  
<span data-ttu-id="2d916-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d916-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2d916-105">Erstellt ein numerisches Token, das von der [IMAPISession::ShowForm-Methode](imapisession-showform.md) für den Zugriff auf eine Nachricht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2d916-105">Creates a numeric token that the [IMAPISession::ShowForm](imapisession-showform.md) method uses to access a message.</span></span> 
  
```cpp
HRESULT PrepareForm(
  LPCIID lpInterface,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMessageToken
);
```

## <a name="parameters"></a><span data-ttu-id="2d916-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d916-106">Parameters</span></span>

 <span data-ttu-id="2d916-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="2d916-107">_lpInterface_</span></span>
  
> <span data-ttu-id="2d916-108">[in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), die die Schnittstelle darstellt, die für den Zugriff auf die Nachricht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2d916-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message.</span></span> <span data-ttu-id="2d916-109">Das **Übergeben von Null** führt dazu, dass die Standardschnittstelle oder [IMessage](imessageimapiprop.md)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2d916-109">Passing **null** results in the standard interface, or [IMessage](imessageimapiprop.md), being used.</span></span> <span data-ttu-id="2d916-110">Der  _lpInterface-Parameter_ muss **null oder** IID_IMessage.</span><span class="sxs-lookup"><span data-stu-id="2d916-110">The  _lpInterface_ parameter must be **null** or IID_IMessage.</span></span> 
    
 <span data-ttu-id="2d916-111">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="2d916-111">_lpMessage_</span></span>
  
> <span data-ttu-id="2d916-112">[in] Ein Zeiger auf die Nachricht, die im Formular angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2d916-112">[in] A pointer to the message to be displayed in the form.</span></span>
    
 <span data-ttu-id="2d916-113">_lpulMessageToken_</span><span class="sxs-lookup"><span data-stu-id="2d916-113">_lpulMessageToken_</span></span>
  
> <span data-ttu-id="2d916-114">[out] Ein Zeiger auf ein Nachrichtentoken, das von der **IMAPISession::ShowForm-Methode** verwendet wird, um auf die Nachricht zu zugreifen, auf die _von lpMessage verwiesen wird._</span><span class="sxs-lookup"><span data-stu-id="2d916-114">[out] A pointer to a message token, which is used by the **IMAPISession::ShowForm** method to access the message pointed to by  _lpMessage_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2d916-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2d916-115">Return value</span></span>

<span data-ttu-id="2d916-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="2d916-116">S_OK</span></span> 
  
> <span data-ttu-id="2d916-117">Die Formularvorbereitung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="2d916-117">The form preparation was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2d916-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2d916-118">Remarks</span></span>

<span data-ttu-id="2d916-119">Die **IMAPISession::P repareForm-Methode** erstellt ein Nachrichtentoken für die Nachricht, auf die der  _lpMessage-Parameter_ verweist, und ruft die [IUnknown::AddRef-Methode](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) der Nachricht auf.</span><span class="sxs-lookup"><span data-stu-id="2d916-119">The **IMAPISession::PrepareForm** method creates a message token for the message pointed to by the  _lpMessage_ parameter and calls the message's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="2d916-120">Dieses Token wird im _ulMessageToken-Parameter_ an **IMAPISession::ShowForm übergeben.**</span><span class="sxs-lookup"><span data-stu-id="2d916-120">This token is passed in the  _ulMessageToken_ parameter to **IMAPISession::ShowForm**.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2d916-121">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="2d916-121">Notes to callers</span></span>

<span data-ttu-id="2d916-122">Wenn der Aufruf von **PrepareForm** erfolgreich ist, lassen Sie die Nachricht los, auf die _von lpMessage_ verwiesen wird, indem Sie die [IUnknown::Release-Methode](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) aufrufen, bevor Sie **ShowForm aufrufen.**</span><span class="sxs-lookup"><span data-stu-id="2d916-122">If the call to **PrepareForm** succeeds, release the message pointed to by  _lpMessage_ by calling its [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method before you call **ShowForm**.</span></span> <span data-ttu-id="2d916-123">Wenn die Nachricht nicht freigegeben wird, bevor Sie **ShowForm aufrufen,** kann es zu Speicherverlusten führen.</span><span class="sxs-lookup"><span data-stu-id="2d916-123">Failure to release the message before you call **ShowForm** can cause memory leaks.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2d916-124">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="2d916-124">MFCMAPI reference</span></span>

<span data-ttu-id="2d916-125">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="2d916-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2d916-126">**Datei**</span><span class="sxs-lookup"><span data-stu-id="2d916-126">**File**</span></span>|<span data-ttu-id="2d916-127">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="2d916-127">**Function**</span></span>|<span data-ttu-id="2d916-128">**Comment**</span><span class="sxs-lookup"><span data-stu-id="2d916-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2d916-129">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="2d916-129">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="2d916-130">OpenMessageModal</span><span class="sxs-lookup"><span data-stu-id="2d916-130">OpenMessageModal</span></span>  <br/> |<span data-ttu-id="2d916-131">MFCMAPI verwendet die **IMAPISession::P repareForm-Methode** zusammen mit **IMAPISession::ShowForm,** um eine Nachricht in einem modalen Formular anzeigen.</span><span class="sxs-lookup"><span data-stu-id="2d916-131">MFCMAPI uses the **IMAPISession::PrepareForm** method, along with **IMAPISession::ShowForm**, to display a message in a modal form.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2d916-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d916-132">See also</span></span>



[<span data-ttu-id="2d916-133">IMAPISession::ShowForm</span><span class="sxs-lookup"><span data-stu-id="2d916-133">IMAPISession::ShowForm</span></span>](imapisession-showform.md)
  
[<span data-ttu-id="2d916-134">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2d916-134">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="2d916-135">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="2d916-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

