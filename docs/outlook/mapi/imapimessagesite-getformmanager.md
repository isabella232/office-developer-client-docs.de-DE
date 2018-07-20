---
title: IMAPIMessageSiteGetFormManager
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetFormManager
api_type:
- COM
ms.assetid: d48bd537-c562-4deb-8a4c-011208991054
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: abaf8f665ea7add92a34c2e4d6fcbf9d5fc08d3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792225"
---
# <a name="imapimessagesitegetformmanager"></a><span data-ttu-id="fc34a-103">IMAPIMessageSite::GetFormManager</span><span class="sxs-lookup"><span data-stu-id="fc34a-103">IMAPIMessageSite::GetFormManager</span></span>

  
  
<span data-ttu-id="fc34a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fc34a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fc34a-105">Gibt eine Formular-Manager-Schnittstelle, die ein Formular Server verwenden kann, um ein anderes Formular Server zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="fc34a-105">Returns a form manager interface, which a form server can use to open another form server.</span></span>
  
```cpp
HRESULT GetFormManager(
  LPMAPIFORMMGR FAR * ppFormMgr
);
```

## <a name="parameters"></a><span data-ttu-id="fc34a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc34a-106">Parameters</span></span>

 <span data-ttu-id="fc34a-107">_ppFormMgr_</span><span class="sxs-lookup"><span data-stu-id="fc34a-107">_ppFormMgr_</span></span>
  
> <span data-ttu-id="fc34a-108">[out] Ein Zeiger auf einen Zeiger auf das zurückgegebene Formular-Manager-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="fc34a-108">[out] A pointer to a pointer to the returned form manager interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fc34a-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fc34a-109">Return value</span></span>

<span data-ttu-id="fc34a-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="fc34a-110">S_OK</span></span> 
  
> <span data-ttu-id="fc34a-111">Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="fc34a-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fc34a-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fc34a-112">Remarks</span></span>

<span data-ttu-id="fc34a-113">Eine Liste der Schnittstellen im Zusammenhang mit der Formular-Servern finden Sie unter [MAPI-Formulars Schnittstellen](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="fc34a-113">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="fc34a-114">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="fc34a-114">MFCMAPI reference</span></span>

<span data-ttu-id="fc34a-115">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="fc34a-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="fc34a-116">**Datei**</span><span class="sxs-lookup"><span data-stu-id="fc34a-116">**File**</span></span>|<span data-ttu-id="fc34a-117">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="fc34a-117">**Function**</span></span>|<span data-ttu-id="fc34a-118">**Comment**</span><span class="sxs-lookup"><span data-stu-id="fc34a-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fc34a-119">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="fc34a-119">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="fc34a-120">CMyMAPIFormViewer::GetFormManager</span><span class="sxs-lookup"><span data-stu-id="fc34a-120">CMyMAPIFormViewer::GetFormManager</span></span>  <br/> |<span data-ttu-id="fc34a-121">MFCMAPI (engl.) wird die **IMAPIMessageSite::GetFormManager** -Methode verwendet, um [MAPIOpenFormMgr](mapiopenformmgr.md) aufrufen und die Ergebnisse des Aufrufs, dass zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="fc34a-121">MFCMAPI uses the **IMAPIMessageSite::GetFormManager** method to call [MAPIOpenFormMgr](mapiopenformmgr.md) and return the results of that call.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fc34a-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc34a-122">See also</span></span>



[<span data-ttu-id="fc34a-123">MAPIOpenFormMgr</span><span class="sxs-lookup"><span data-stu-id="fc34a-123">MAPIOpenFormMgr</span></span>](mapiopenformmgr.md)
  
[<span data-ttu-id="fc34a-124">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fc34a-124">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="fc34a-125">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="fc34a-125">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="fc34a-126">MAPI-Formularoberflächen</span><span class="sxs-lookup"><span data-stu-id="fc34a-126">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

