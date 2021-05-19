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
ms.openlocfilehash: 0c78574f213245a5c30ff589ade824e5c5bd84ee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410469"
---
# <a name="imapimessagesitegetstore"></a><span data-ttu-id="68072-103">IMAPIMessageSite::GetStore</span><span class="sxs-lookup"><span data-stu-id="68072-103">IMAPIMessageSite::GetStore</span></span>

  
  
<span data-ttu-id="68072-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="68072-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="68072-105">Gibt den Nachrichtenspeicher zurück, der die aktuelle Nachricht enthält, wenn ein solcher Speicher vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="68072-105">Returns the message store that contains the current message, if such a store exists.</span></span> <span data-ttu-id="68072-106">Diese Methode gibt NULL im  _ppStore-Parameter_ für eingebettete Nachrichten zurück, die in einer anderen Nachricht statt direkt in einem Nachrichtenspeicher gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="68072-106">This method will return NULL in the  _ppStore_ parameter for embedded messages, which are stored in another message instead of directly in a message store.</span></span> 
  
```cpp
HRESULT GetStore(
  LPMDB FAR * ppStore
);
```

## <a name="parameters"></a><span data-ttu-id="68072-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="68072-107">Parameters</span></span>

 <span data-ttu-id="68072-108">_ppStore_</span><span class="sxs-lookup"><span data-stu-id="68072-108">_ppStore_</span></span>
  
> <span data-ttu-id="68072-109">[out] Ein Zeiger auf einen Zeiger auf den Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="68072-109">[out] A pointer to a pointer to the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="68072-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="68072-110">Return value</span></span>

<span data-ttu-id="68072-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="68072-111">S_OK</span></span> 
  
> <span data-ttu-id="68072-112">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="68072-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="68072-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="68072-113">S_FALSE</span></span> 
  
> <span data-ttu-id="68072-114">Es gibt keinen Speicher, der die Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="68072-114">There is no store that contains the message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="68072-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="68072-115">Remarks</span></span>

<span data-ttu-id="68072-116">Eine Liste der Schnittstellen im Zusammenhang mit Formularservern finden Sie unter [MAPI Form Interfaces](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="68072-116">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="68072-117">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="68072-117">MFCMAPI reference</span></span>

<span data-ttu-id="68072-118">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="68072-118">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="68072-119">**Datei**</span><span class="sxs-lookup"><span data-stu-id="68072-119">**File**</span></span>|<span data-ttu-id="68072-120">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="68072-120">**Function**</span></span>|<span data-ttu-id="68072-121">**Comment**</span><span class="sxs-lookup"><span data-stu-id="68072-121">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="68072-122">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="68072-122">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="68072-123">CMyMAPIFormViewer::GetStore</span><span class="sxs-lookup"><span data-stu-id="68072-123">CMyMAPIFormViewer::GetStore</span></span>  <br/> |<span data-ttu-id="68072-124">MFCMAPI verwendet die **IMAPIMessageSite::GetStore-Methode,** um den aktuell zwischengespeicherten Zeiger auf den angegebenen Speicher zu erhalten, sofern er verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="68072-124">MFCMAPI uses the **IMAPIMessageSite::GetStore** method to get the currently cached pointer to the specified store, if it is available.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="68072-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68072-125">See also</span></span>



[<span data-ttu-id="68072-126">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="68072-126">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="68072-127">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="68072-127">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="68072-128">MAPI-Formularschnittstellen</span><span class="sxs-lookup"><span data-stu-id="68072-128">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

