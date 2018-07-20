---
title: IMAPIMessageSiteGetSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetSession
api_type:
- COM
ms.assetid: c35d9e38-f4cf-4908-aaa1-a4263b58f7e8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d5d0f465ecdf4865ca86448448c56d54d5df4505
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792221"
---
# <a name="imapimessagesitegetsession"></a><span data-ttu-id="e24eb-103">IMAPIMessageSite::GetSession</span><span class="sxs-lookup"><span data-stu-id="e24eb-103">IMAPIMessageSite::GetSession</span></span>

  
  
<span data-ttu-id="e24eb-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e24eb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e24eb-105">Gibt die MAPI-Sitzung, in der die aktuelle Nachricht erstellt oder geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="e24eb-105">Returns the MAPI session in which the current message was created or opened.</span></span>
  
```cpp
HRESULT GetSession(
  LPMAPISESSION FAR * ppSession
);
```

## <a name="parameters"></a><span data-ttu-id="e24eb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e24eb-106">Parameters</span></span>

 <span data-ttu-id="e24eb-107">_ppSession_</span><span class="sxs-lookup"><span data-stu-id="e24eb-107">_ppSession_</span></span>
  
> <span data-ttu-id="e24eb-108">[out] Ein Zeiger auf einen Zeiger auf das zurückgegebene Session-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e24eb-108">[out] A pointer to a pointer to the returned session object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e24eb-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e24eb-109">Return value</span></span>

<span data-ttu-id="e24eb-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="e24eb-110">S_OK</span></span> 
  
> <span data-ttu-id="e24eb-111">Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="e24eb-111">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="e24eb-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="e24eb-112">S_FALSE</span></span> 
  
> <span data-ttu-id="e24eb-113">Für die aktuelle Nachricht ist keine Sitzung vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e24eb-113">No session exists for the current message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e24eb-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e24eb-114">Remarks</span></span>

<span data-ttu-id="e24eb-115">Eine Liste der Schnittstellen im Zusammenhang mit Formular Servern, finden Sie unter [MAPI-Formulars Schnittstellen](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="e24eb-115">For a list of interfaces that are related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e24eb-116">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="e24eb-116">MFCMAPI reference</span></span>

<span data-ttu-id="e24eb-117">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e24eb-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e24eb-118">**Datei**</span><span class="sxs-lookup"><span data-stu-id="e24eb-118">**File**</span></span>|<span data-ttu-id="e24eb-119">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="e24eb-119">**Function**</span></span>|<span data-ttu-id="e24eb-120">**Comment**</span><span class="sxs-lookup"><span data-stu-id="e24eb-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e24eb-121">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="e24eb-121">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="e24eb-122">CMyMAPIFormViewer::GetSession</span><span class="sxs-lookup"><span data-stu-id="e24eb-122">CMyMAPIFormViewer::GetSession</span></span>  <br/> |<span data-ttu-id="e24eb-123">MFCMAPI (engl.) verwendet die **IMAPIMessageSite::GetSession** -Methode den aktuell zwischengespeicherten Sitzung Zeiger zurückgegeben, wenn es zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="e24eb-123">MFCMAPI uses the **IMAPIMessageSite::GetSession** method to return the currently cached session pointer, if it is available.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e24eb-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e24eb-124">See also</span></span>



[<span data-ttu-id="e24eb-125">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e24eb-125">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="e24eb-126">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="e24eb-126">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

