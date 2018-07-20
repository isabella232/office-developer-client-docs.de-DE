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
ms.openlocfilehash: 2787150a9fa0fc41e04c58b4a4310ffa844f3743
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792219"
---
# <a name="imapimessagesitegetstore"></a><span data-ttu-id="22c8b-103">IMAPIMessageSite::GetStore</span><span class="sxs-lookup"><span data-stu-id="22c8b-103">IMAPIMessageSite::GetStore</span></span>

  
  
<span data-ttu-id="22c8b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="22c8b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="22c8b-105">Gibt den Nachrichtenspeicher, der die aktuelle Nachricht enthält zurück, wenn eine solche ein Speicher vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="22c8b-105">Returns the message store that contains the current message, if such a store exists.</span></span> <span data-ttu-id="22c8b-106">Diese Methode gibt NULL im Parameter _PpStore_ für eingebettete Nachrichten zurück, die in eine andere Nachricht anstatt direkt in einem Nachrichtenspeicher gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="22c8b-106">This method will return NULL in the  _ppStore_ parameter for embedded messages, which are stored in another message instead of directly in a message store.</span></span> 
  
```cpp
HRESULT GetStore(
  LPMDB FAR * ppStore
);
```

## <a name="parameters"></a><span data-ttu-id="22c8b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="22c8b-107">Parameters</span></span>

 <span data-ttu-id="22c8b-108">_ppStore_</span><span class="sxs-lookup"><span data-stu-id="22c8b-108">_ppStore_</span></span>
  
> <span data-ttu-id="22c8b-109">[out] Ein Zeiger auf einen Zeiger auf den Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="22c8b-109">[out] A pointer to a pointer to the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="22c8b-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22c8b-110">Return value</span></span>

<span data-ttu-id="22c8b-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="22c8b-111">S_OK</span></span> 
  
> <span data-ttu-id="22c8b-112">Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="22c8b-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="22c8b-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="22c8b-113">S_FALSE</span></span> 
  
> <span data-ttu-id="22c8b-114">Es ist kein Speicher, die die Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="22c8b-114">There is no store that contains the message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="22c8b-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22c8b-115">Remarks</span></span>

<span data-ttu-id="22c8b-116">Eine Liste der Schnittstellen im Zusammenhang mit der Formular-Servern finden Sie unter [MAPI-Formulars Schnittstellen](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="22c8b-116">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="22c8b-117">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="22c8b-117">MFCMAPI reference</span></span>

<span data-ttu-id="22c8b-118">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="22c8b-118">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="22c8b-119">**Datei**</span><span class="sxs-lookup"><span data-stu-id="22c8b-119">**File**</span></span>|<span data-ttu-id="22c8b-120">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="22c8b-120">**Function**</span></span>|<span data-ttu-id="22c8b-121">**Comment**</span><span class="sxs-lookup"><span data-stu-id="22c8b-121">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="22c8b-122">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="22c8b-122">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="22c8b-123">CMyMAPIFormViewer::GetStore</span><span class="sxs-lookup"><span data-stu-id="22c8b-123">CMyMAPIFormViewer::GetStore</span></span>  <br/> |<span data-ttu-id="22c8b-124">MFCMAPI (engl.) verwendet die **IMAPIMessageSite::GetStore** -Methode den aktuell zwischengespeicherten Zeiger auf den angegebenen Speicher, abgerufen, sofern es vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="22c8b-124">MFCMAPI uses the **IMAPIMessageSite::GetStore** method to get the currently cached pointer to the specified store, if it is available.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="22c8b-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22c8b-125">See also</span></span>



[<span data-ttu-id="22c8b-126">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="22c8b-126">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="22c8b-127">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="22c8b-127">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="22c8b-128">MAPI-Formularoberflächen</span><span class="sxs-lookup"><span data-stu-id="22c8b-128">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

