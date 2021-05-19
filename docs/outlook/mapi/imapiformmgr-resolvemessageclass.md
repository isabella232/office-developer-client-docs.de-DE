---
title: IMAPIFormMgrResolveMessageClass
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.ResolveMessageClass
api_type:
- COM
ms.assetid: c2af7516-3a97-4422-874d-b1e3a0d4f316
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e99cff77fe872018722395c53c605e4d8fabfdde
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426394"
---
# <a name="imapiformmgrresolvemessageclass"></a><span data-ttu-id="838ca-103">IMAPIFormMgr::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="838ca-103">IMAPIFormMgr::ResolveMessageClass</span></span>

  
  
<span data-ttu-id="838ca-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="838ca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="838ca-105">Löst eine Nachrichtenklasse in ihr Formular in einem Formularcontainer auf und gibt ein Formularinformationsobjekt für dieses Formular zurück.</span><span class="sxs-lookup"><span data-stu-id="838ca-105">Resolves a message class to its form within a form container, and returns a form information object for that form.</span></span>
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMsgClass,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPMAPIFORMINFO FAR * ppResult
);
```

## <a name="parameters"></a><span data-ttu-id="838ca-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="838ca-106">Parameters</span></span>

 <span data-ttu-id="838ca-107">_szMsgClass_</span><span class="sxs-lookup"><span data-stu-id="838ca-107">_szMsgClass_</span></span>
  
> <span data-ttu-id="838ca-108">[in] Eine Zeichenfolge, die die aufgelöste Nachrichtenklasse benennt.</span><span class="sxs-lookup"><span data-stu-id="838ca-108">[in] A string that names the message class being resolved.</span></span>
    
 <span data-ttu-id="838ca-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="838ca-109">_ulFlags_</span></span>
  
> <span data-ttu-id="838ca-110">[in] Eine Bitmaske mit Flags, die steuert, wie die Nachrichtenklasse aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="838ca-110">[in] A bitmask of flags that controls how the message class is resolved.</span></span> <span data-ttu-id="838ca-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="838ca-111">The following flag can be set:</span></span>
    
<span data-ttu-id="838ca-112">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="838ca-112">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="838ca-113">Es sollten nur Nachrichtenklassenzeichenfolgen aufgelöst werden, die eine genaue Übereinstimmung sind.</span><span class="sxs-lookup"><span data-stu-id="838ca-113">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="838ca-114">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="838ca-114">_pFolderFocus_</span></span>
  
> <span data-ttu-id="838ca-115">[in] Ein Zeiger auf den Ordner, der die aufgelöste Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="838ca-115">[in] A pointer to the folder that contains the message being resolved.</span></span> <span data-ttu-id="838ca-116">Der  _pFolderFocus-Parameter_ kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="838ca-116">The  _pFolderFocus_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="838ca-117">_ppResult_</span><span class="sxs-lookup"><span data-stu-id="838ca-117">_ppResult_</span></span>
  
> <span data-ttu-id="838ca-118">[out] Ein Zeiger auf einen Zeiger auf ein zurückgegebenes Formularinformationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="838ca-118">[out] A pointer to a pointer to a returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="838ca-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="838ca-119">Return value</span></span>

<span data-ttu-id="838ca-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="838ca-120">S_OK</span></span> 
  
> <span data-ttu-id="838ca-121">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="838ca-121">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="838ca-122">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="838ca-122">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="838ca-123">Die im  _szMsgClass-Parameter_ übergebene Nachrichtenklasse ist nicht mit der Nachrichtenklasse für ein Formular in der Formularbibliothek übereinstimmend.</span><span class="sxs-lookup"><span data-stu-id="838ca-123">The message class passed in the  _szMsgClass_ parameter does not match the message class for any form in the form library.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="838ca-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="838ca-124">Remarks</span></span>

<span data-ttu-id="838ca-125">Formularbetrachter rufen die **IMAPIFormMgr::ResolveMessageClass-Methode** auf, um eine Nachrichtenklasse in ihr Formular innerhalb eines Formularcontainers zu auflösen.</span><span class="sxs-lookup"><span data-stu-id="838ca-125">Form viewers call the **IMAPIFormMgr::ResolveMessageClass** method to resolve a message class to its form within a form container.</span></span> <span data-ttu-id="838ca-126">Das im  _ppResult-Parameter_ zurückgegebene Formularinformationsobjekt bietet weiteren Zugriff auf die Eigenschaften des Formulars mit der angegebenen Nachrichtenklasse.</span><span class="sxs-lookup"><span data-stu-id="838ca-126">The form information object returned in the  _ppResult_ parameter provides further access to the properties of the form that has the given message class.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="838ca-127">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="838ca-127">Notes to callers</span></span>

<span data-ttu-id="838ca-128">Um eine Nachrichtenklasse in ein Formular zu auflösen, übergibt eine Formularanzeige den Namen der zu auflösenden Nachrichtenklasse, z. B. " `IPM.HelpDesk.Software` ".</span><span class="sxs-lookup"><span data-stu-id="838ca-128">To resolve a message class to a form, a form viewer passes in the name of the message class to be resolved, such as " `IPM.HelpDesk.Software`".</span></span> <span data-ttu-id="838ca-129">Um zu erzwingen, dass die Auflösung exakt ist (d. h. um die Auflösung zu einer Basisklasse der Nachrichtenklasse zu verhindern, wenn kein exakt übereinstimmender Formularserver verfügbar ist), kann das MAPIFORM_EXACTMATCH-Flag im  _ulFlags-Parameter_ übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="838ca-129">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class when an exactly matching form server is not available), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="838ca-130">Wenn der  _pFolderFocus-Parameter_ NULL ist, durchsucht der Nachrichtenklassenauflösungsprozess keinen Ordnercontainer.</span><span class="sxs-lookup"><span data-stu-id="838ca-130">If the  _pFolderFocus_ parameter is NULL, the message-class resolution process does not search a folder container.</span></span> 
  
<span data-ttu-id="838ca-131">Die Reihenfolge der durchsuchten Container hängt von der Implementierung des Formularbibliotheksanbieters ab.</span><span class="sxs-lookup"><span data-stu-id="838ca-131">The order of the containers searched depends on the implementation of the form library provider.</span></span> <span data-ttu-id="838ca-132">Der Standardmäßige Formularbibliotheksanbieter durchsucht zuerst den lokalen Container, dann den Ordnercontainer für den übergebenen Ordner, den persönlichen Formularcontainer und schließlich den Organisationscontainer.</span><span class="sxs-lookup"><span data-stu-id="838ca-132">The default form library provider searches first the local container, then the folder container for the passed-in folder, the personal form container and, finally, the organization container.</span></span>
  
<span data-ttu-id="838ca-133">Nachrichtenklassennamen sind immer ANSI-Zeichenfolgen, nie Unicode.</span><span class="sxs-lookup"><span data-stu-id="838ca-133">Message class names are always ANSI strings, never Unicode.</span></span>
  
<span data-ttu-id="838ca-134">Der Klassenbezeichner für die aufgelöste Nachrichtenklasse wird als Teil des Formularinformationsobjekts zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="838ca-134">The class identifier for the resolved message class is returned as part of the form information object.</span></span> <span data-ttu-id="838ca-135">Eine Formularanzeige sollte erst dann in der Annahme funktionieren, dass der Klassenbezeichner in der OLE-Bibliothek vorhanden ist, nachdem die Formularanzeige entweder die [IMAPIFormMgr::P repareForm-Methode](imapiformmgr-prepareform.md) oder die [IMAPIFormMgr::CreateForm-Methode](imapiformmgr-createform.md) aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="838ca-135">A form viewer should not work on the assumption that the class identifier exists in the OLE library until after the form viewer has called either the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) method or the [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="838ca-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="838ca-136">See also</span></span>



[<span data-ttu-id="838ca-137">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="838ca-137">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)
  
[<span data-ttu-id="838ca-138">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="838ca-138">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="838ca-139">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="838ca-139">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="838ca-140">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="838ca-140">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

