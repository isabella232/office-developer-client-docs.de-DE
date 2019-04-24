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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2d4100d9bcd1b086747d742d9636c4bf7a39f50b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321372"
---
# <a name="imapimessagesitegetformmanager"></a><span data-ttu-id="7d5dc-103">IMAPIMessageSite::GetFormManager</span><span class="sxs-lookup"><span data-stu-id="7d5dc-103">IMAPIMessageSite::GetFormManager</span></span>

  
  
<span data-ttu-id="7d5dc-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d5dc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d5dc-105">Gibt eine Formular-Manager-Schnittstelle zurück, die ein Formularserver zum Öffnen eines anderen Formular Servers verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="7d5dc-105">Returns a form manager interface, which a form server can use to open another form server.</span></span>
  
```cpp
HRESULT GetFormManager(
  LPMAPIFORMMGR FAR * ppFormMgr
);
```

## <a name="parameters"></a><span data-ttu-id="7d5dc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d5dc-106">Parameters</span></span>

 <span data-ttu-id="7d5dc-107">_ppFormMgr_</span><span class="sxs-lookup"><span data-stu-id="7d5dc-107">_ppFormMgr_</span></span>
  
> <span data-ttu-id="7d5dc-108">Out Ein Zeiger auf einen Zeiger auf die zurückgegebene Formular-Manager-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="7d5dc-108">[out] A pointer to a pointer to the returned form manager interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7d5dc-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7d5dc-109">Return value</span></span>

<span data-ttu-id="7d5dc-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="7d5dc-110">S_OK</span></span> 
  
> <span data-ttu-id="7d5dc-111">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="7d5dc-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7d5dc-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7d5dc-112">Remarks</span></span>

<span data-ttu-id="7d5dc-113">Eine Liste der Schnittstellen im Zusammenhang mit Formular Servern finden Sie unter [MAPI-Formular Schnittstellen](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="7d5dc-113">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7d5dc-114">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="7d5dc-114">MFCMAPI reference</span></span>

<span data-ttu-id="7d5dc-115">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7d5dc-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7d5dc-116">**Datei**</span><span class="sxs-lookup"><span data-stu-id="7d5dc-116">**File**</span></span>|<span data-ttu-id="7d5dc-117">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="7d5dc-117">**Function**</span></span>|<span data-ttu-id="7d5dc-118">**Comment**</span><span class="sxs-lookup"><span data-stu-id="7d5dc-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7d5dc-119">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="7d5dc-119">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="7d5dc-120">CMyMAPIFormViewer:: getFormmanager</span><span class="sxs-lookup"><span data-stu-id="7d5dc-120">CMyMAPIFormViewer::GetFormManager</span></span>  <br/> |<span data-ttu-id="7d5dc-121">MFCMAPI verwendet die **IMAPIMessageSite::** getformmanager-Methode, um [MAPIOpenFormMgr](mapiopenformmgr.md) aufzurufen und die Ergebnisse dieses Aufrufs zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="7d5dc-121">MFCMAPI uses the **IMAPIMessageSite::GetFormManager** method to call [MAPIOpenFormMgr](mapiopenformmgr.md) and return the results of that call.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7d5dc-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d5dc-122">See also</span></span>



[<span data-ttu-id="7d5dc-123">MAPIOpenFormMgr</span><span class="sxs-lookup"><span data-stu-id="7d5dc-123">MAPIOpenFormMgr</span></span>](mapiopenformmgr.md)
  
[<span data-ttu-id="7d5dc-124">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7d5dc-124">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="7d5dc-125">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="7d5dc-125">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="7d5dc-126">MAPI-Formular Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="7d5dc-126">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

