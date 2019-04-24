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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e1ea68a7690a93915cd80ad5406c4d71d3a97400
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321441"
---
# <a name="imapimessagesitegetsession"></a><span data-ttu-id="6c898-103">IMAPIMessageSite::GetSession</span><span class="sxs-lookup"><span data-stu-id="6c898-103">IMAPIMessageSite::GetSession</span></span>

  
  
<span data-ttu-id="6c898-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c898-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c898-105">Gibt die MAPI-Sitzung zurück, in der die aktuelle Nachricht erstellt oder geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="6c898-105">Returns the MAPI session in which the current message was created or opened.</span></span>
  
```cpp
HRESULT GetSession(
  LPMAPISESSION FAR * ppSession
);
```

## <a name="parameters"></a><span data-ttu-id="6c898-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c898-106">Parameters</span></span>

 <span data-ttu-id="6c898-107">_ppSession_</span><span class="sxs-lookup"><span data-stu-id="6c898-107">_ppSession_</span></span>
  
> <span data-ttu-id="6c898-108">Out Ein Zeiger auf einen Zeiger auf das zurückgegebene Session-Objekt.</span><span class="sxs-lookup"><span data-stu-id="6c898-108">[out] A pointer to a pointer to the returned session object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6c898-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6c898-109">Return value</span></span>

<span data-ttu-id="6c898-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="6c898-110">S_OK</span></span> 
  
> <span data-ttu-id="6c898-111">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="6c898-111">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="6c898-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="6c898-112">S_FALSE</span></span> 
  
> <span data-ttu-id="6c898-113">Für die aktuelle Nachricht ist keine Sitzung vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6c898-113">No session exists for the current message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6c898-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6c898-114">Remarks</span></span>

<span data-ttu-id="6c898-115">Eine Liste der Schnittstellen im Zusammenhang mit Formular Servern finden Sie unter [MAPI-Formular Schnittstellen](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="6c898-115">For a list of interfaces that are related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6c898-116">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="6c898-116">MFCMAPI reference</span></span>

<span data-ttu-id="6c898-117">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="6c898-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6c898-118">**Datei**</span><span class="sxs-lookup"><span data-stu-id="6c898-118">**File**</span></span>|<span data-ttu-id="6c898-119">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="6c898-119">**Function**</span></span>|<span data-ttu-id="6c898-120">**Comment**</span><span class="sxs-lookup"><span data-stu-id="6c898-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6c898-121">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="6c898-121">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="6c898-122">CMyMAPIFormViewer:: getSession</span><span class="sxs-lookup"><span data-stu-id="6c898-122">CMyMAPIFormViewer::GetSession</span></span>  <br/> |<span data-ttu-id="6c898-123">MFCMAPI verwendet die **IMAPIMessageSite:: getSession** -Methode, um den derzeit zwischengespeicherten Sitzungs Zeiger zurückzugeben, sofern dieser verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="6c898-123">MFCMAPI uses the **IMAPIMessageSite::GetSession** method to return the currently cached session pointer, if it is available.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6c898-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c898-124">See also</span></span>



[<span data-ttu-id="6c898-125">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6c898-125">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="6c898-126">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="6c898-126">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

