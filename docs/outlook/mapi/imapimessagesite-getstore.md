---
title: IMAPIMessageSiteGetStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetStore
api_type:
- COM
ms.assetid: d1ca619e-8bdc-417b-aed6-23dd30e6eafa
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1f4e6c49ca1c537f78ccce708c4a0b00f81ad7e4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567930"
---
# <a name="imapimessagesitegetstore"></a><span data-ttu-id="c35d4-103">IMAPIMessageSite::GetStore</span><span class="sxs-lookup"><span data-stu-id="c35d4-103">IMAPIMessageSite::GetStore</span></span>

  
  
<span data-ttu-id="c35d4-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c35d4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c35d4-105">Gibt den Nachrichtenspeicher, der die aktuelle Nachricht enthält zurück, wenn eine solche ein Speicher vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c35d4-105">Returns the message store that contains the current message, if such a store exists.</span></span> <span data-ttu-id="c35d4-106">Diese Methode gibt NULL im Parameter _PpStore_ für eingebettete Nachrichten zurück, die in eine andere Nachricht anstatt direkt in einem Nachrichtenspeicher gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="c35d4-106">This method will return NULL in the  _ppStore_ parameter for embedded messages, which are stored in another message instead of directly in a message store.</span></span> 
  
```cpp
HRESULT GetStore(
  LPMDB FAR * ppStore
);
```

## <a name="parameters"></a><span data-ttu-id="c35d4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c35d4-107">Parameters</span></span>

 <span data-ttu-id="c35d4-108">_ppStore_</span><span class="sxs-lookup"><span data-stu-id="c35d4-108">_ppStore_</span></span>
  
> <span data-ttu-id="c35d4-109">[out] Ein Zeiger auf einen Zeiger auf den Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="c35d4-109">[out] A pointer to a pointer to the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c35d4-110">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="c35d4-110">Return value</span></span>

<span data-ttu-id="c35d4-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="c35d4-111">S_OK</span></span> 
  
> <span data-ttu-id="c35d4-112">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="c35d4-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="c35d4-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="c35d4-113">S_FALSE</span></span> 
  
> <span data-ttu-id="c35d4-114">Es ist kein Speicher, die die Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="c35d4-114">There is no store that contains the message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c35d4-115">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="c35d4-115">Remarks</span></span>

<span data-ttu-id="c35d4-116">Eine Liste der Schnittstellen im Zusammenhang mit der Formular-Servern finden Sie unter [MAPI-Formulars Schnittstellen](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="c35d4-116">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c35d4-117">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="c35d4-117">MFCMAPI reference</span></span>

<span data-ttu-id="c35d4-118">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c35d4-118">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c35d4-119">**Datei**</span><span class="sxs-lookup"><span data-stu-id="c35d4-119">**File**</span></span>|<span data-ttu-id="c35d4-120">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="c35d4-120">**Function**</span></span>|<span data-ttu-id="c35d4-121">**Comment**</span><span class="sxs-lookup"><span data-stu-id="c35d4-121">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c35d4-122">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="c35d4-122">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="c35d4-123">CMyMAPIFormViewer::GetStore</span><span class="sxs-lookup"><span data-stu-id="c35d4-123">CMyMAPIFormViewer::GetStore</span></span>  <br/> |<span data-ttu-id="c35d4-124">MFCMAPI (engl.) verwendet die **IMAPIMessageSite::GetStore** -Methode den aktuell zwischengespeicherten Zeiger auf den angegebenen Speicher, abgerufen, sofern es vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c35d4-124">MFCMAPI uses the **IMAPIMessageSite::GetStore** method to get the currently cached pointer to the specified store, if it is available.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c35d4-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c35d4-125">See also</span></span>



[<span data-ttu-id="c35d4-126">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c35d4-126">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="c35d4-127">MFCMAPI als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="c35d4-127">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="c35d4-128">MAPI-Formularoberflächen</span><span class="sxs-lookup"><span data-stu-id="c35d4-128">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

