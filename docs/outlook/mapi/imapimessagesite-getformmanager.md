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
ms.openlocfilehash: 5e3a2224daace9be7f4504a693806ccb3cf4abbe
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570492"
---
# <a name="imapimessagesitegetformmanager"></a><span data-ttu-id="66890-103">IMAPIMessageSite::GetFormManager</span><span class="sxs-lookup"><span data-stu-id="66890-103">IMAPIMessageSite::GetFormManager</span></span>

  
  
<span data-ttu-id="66890-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="66890-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="66890-105">Gibt eine Formular-Manager-Schnittstelle, die ein Formular Server verwenden kann, um ein anderes Formular Server zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="66890-105">Returns a form manager interface, which a form server can use to open another form server.</span></span>
  
```cpp
HRESULT GetFormManager(
  LPMAPIFORMMGR FAR * ppFormMgr
);
```

## <a name="parameters"></a><span data-ttu-id="66890-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="66890-106">Parameters</span></span>

 <span data-ttu-id="66890-107">_ppFormMgr_</span><span class="sxs-lookup"><span data-stu-id="66890-107">_ppFormMgr_</span></span>
  
> <span data-ttu-id="66890-108">[out] Ein Zeiger auf einen Zeiger auf das zurückgegebene Formular-Manager-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="66890-108">[out] A pointer to a pointer to the returned form manager interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="66890-109">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="66890-109">Return value</span></span>

<span data-ttu-id="66890-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="66890-110">S_OK</span></span> 
  
> <span data-ttu-id="66890-111">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="66890-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="66890-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="66890-112">Remarks</span></span>

<span data-ttu-id="66890-113">Eine Liste der Schnittstellen im Zusammenhang mit der Formular-Servern finden Sie unter [MAPI-Formulars Schnittstellen](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="66890-113">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="66890-114">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="66890-114">MFCMAPI reference</span></span>

<span data-ttu-id="66890-115">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="66890-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="66890-116">**Datei**</span><span class="sxs-lookup"><span data-stu-id="66890-116">**File**</span></span>|<span data-ttu-id="66890-117">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="66890-117">**Function**</span></span>|<span data-ttu-id="66890-118">**Comment**</span><span class="sxs-lookup"><span data-stu-id="66890-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="66890-119">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="66890-119">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="66890-120">CMyMAPIFormViewer::GetFormManager</span><span class="sxs-lookup"><span data-stu-id="66890-120">CMyMAPIFormViewer::GetFormManager</span></span>  <br/> |<span data-ttu-id="66890-121">MFCMAPI (engl.) wird die **IMAPIMessageSite::GetFormManager** -Methode verwendet, um [MAPIOpenFormMgr](mapiopenformmgr.md) aufrufen und die Ergebnisse des Aufrufs, dass zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="66890-121">MFCMAPI uses the **IMAPIMessageSite::GetFormManager** method to call [MAPIOpenFormMgr](mapiopenformmgr.md) and return the results of that call.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="66890-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66890-122">See also</span></span>



[<span data-ttu-id="66890-123">MAPIOpenFormMgr</span><span class="sxs-lookup"><span data-stu-id="66890-123">MAPIOpenFormMgr</span></span>](mapiopenformmgr.md)
  
[<span data-ttu-id="66890-124">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="66890-124">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="66890-125">MFCMAPI als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="66890-125">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="66890-126">MAPI-Formularoberflächen</span><span class="sxs-lookup"><span data-stu-id="66890-126">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

