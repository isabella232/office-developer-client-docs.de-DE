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
ms.openlocfilehash: a84698ccc132c750cbd071c05160117c40e352a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792210"
---
# <a name="imapiformmgrresolvemessageclass"></a><span data-ttu-id="11a7b-103">IMAPIFormMgr::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="11a7b-103">IMAPIFormMgr::ResolveMessageClass</span></span>

  
  
<span data-ttu-id="11a7b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="11a7b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="11a7b-105">Eine Nachrichtenklasse in seiner Form innerhalb eines Containers Formular aufgelöst wird, und gibt ein Formular Informationen-Objekt für das Formular zurück.</span><span class="sxs-lookup"><span data-stu-id="11a7b-105">Resolves a message class to its form within a form container, and returns a form information object for that form.</span></span>
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMsgClass,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPMAPIFORMINFO FAR * ppResult
);
```

## <a name="parameters"></a><span data-ttu-id="11a7b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="11a7b-106">Parameters</span></span>

 <span data-ttu-id="11a7b-107">_szMsgClass_</span><span class="sxs-lookup"><span data-stu-id="11a7b-107">_szMsgClass_</span></span>
  
> <span data-ttu-id="11a7b-108">[in] Eine Zeichenfolge, die den Namen die Nachrichtenklasse aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="11a7b-108">[in] A string that names the message class being resolved.</span></span>
    
 <span data-ttu-id="11a7b-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="11a7b-109">_ulFlags_</span></span>
  
> <span data-ttu-id="11a7b-110">[in] Eine Bitmaske aus Flags, die steuert, wie die Nachrichtenklasse aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="11a7b-110">[in] A bitmask of flags that controls how the message class is resolved.</span></span> <span data-ttu-id="11a7b-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="11a7b-111">The following flag can be set:</span></span>
    
<span data-ttu-id="11a7b-112">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="11a7b-112">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="11a7b-113">Nur Nachricht Klasse Zeichenfolgen, die eine genaue Übereinstimmung sollten aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="11a7b-113">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="11a7b-114">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="11a7b-114">_pFolderFocus_</span></span>
  
> <span data-ttu-id="11a7b-115">[in] Ein Zeiger auf den Ordner mit der Nachricht aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="11a7b-115">[in] A pointer to the folder that contains the message being resolved.</span></span> <span data-ttu-id="11a7b-116">Der Parameter _pFolderFocus_ kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="11a7b-116">The  _pFolderFocus_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="11a7b-117">_ppResult_</span><span class="sxs-lookup"><span data-stu-id="11a7b-117">_ppResult_</span></span>
  
> <span data-ttu-id="11a7b-118">[out] Ein Zeiger auf einen Zeiger auf ein Formular zurückgegebenen Informationen-Objekt.</span><span class="sxs-lookup"><span data-stu-id="11a7b-118">[out] A pointer to a pointer to a returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="11a7b-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="11a7b-119">Return value</span></span>

<span data-ttu-id="11a7b-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="11a7b-120">S_OK</span></span> 
  
> <span data-ttu-id="11a7b-121">Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="11a7b-121">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="11a7b-122">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="11a7b-122">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="11a7b-123">Die Nachrichtenklasse in der _SzMsgClass_ -Parameter übergeben stimmt nicht mit die Nachrichtenklasse für jedes Formular in der Formularbibliothek überein.</span><span class="sxs-lookup"><span data-stu-id="11a7b-123">The message class passed in the  _szMsgClass_ parameter does not match the message class for any form in the form library.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="11a7b-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="11a7b-124">Remarks</span></span>

<span data-ttu-id="11a7b-125">Formular Viewer rufen Sie die **IMAPIFormMgr::ResolveMessageClass** -Methode, um auf die Form in einem Formular Container eine Nachrichtenklasse zu beheben.</span><span class="sxs-lookup"><span data-stu-id="11a7b-125">Form viewers call the **IMAPIFormMgr::ResolveMessageClass** method to resolve a message class to its form within a form container.</span></span> <span data-ttu-id="11a7b-126">Das Formular Informationen-Objekt zurückgegeben, die im Parameter _PpResult_ bietet weitere Zugriff auf die Eigenschaften des Formulars, das die angegebenen Nachrichtenklasse hat.</span><span class="sxs-lookup"><span data-stu-id="11a7b-126">The form information object returned in the  _ppResult_ parameter provides further access to the properties of the form that has the given message class.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="11a7b-127">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="11a7b-127">Notes to callers</span></span>

<span data-ttu-id="11a7b-128">Um eine Nachrichtenklasse zu einem Formular zu beheben, ein Formular Viewer übergibt den Namen der Nachrichtenklasse aufgelöst, z. B. " `IPM.HelpDesk.Software`".</span><span class="sxs-lookup"><span data-stu-id="11a7b-128">To resolve a message class to a form, a form viewer passes in the name of the message class to be resolved, such as " `IPM.HelpDesk.Software`".</span></span> <span data-ttu-id="11a7b-129">So erzwingen Sie die Auflösung genau sein (d. h., um auf eine Basisklasse der Nachrichtenklasse, wenn ein Formular genau übereinstimmenden Lösung zu verhindern Server ist nicht verfügbar), die Kennzeichen MAPIFORM_EXACTMATCH im _UlFlags_ -Parameter übergeben werden können.</span><span class="sxs-lookup"><span data-stu-id="11a7b-129">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class when an exactly matching form server is not available), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="11a7b-130">Wenn der Parameter _pFolderFocus_ NULL ist, führt der Nachrichtenklasse Auflösungsprozess keine Ordnercontainer Suche.</span><span class="sxs-lookup"><span data-stu-id="11a7b-130">If the  _pFolderFocus_ parameter is NULL, the message-class resolution process does not search a folder container.</span></span> 
  
<span data-ttu-id="11a7b-131">Die Reihenfolge der Container durchsucht, hängt von der Implementierung des Anbieters Bibliothek Formular ab.</span><span class="sxs-lookup"><span data-stu-id="11a7b-131">The order of the containers searched depends on the implementation of the form library provider.</span></span> <span data-ttu-id="11a7b-132">Der Formular Bibliothek Standardanbieter sucht zunächst den lokalen Container, und klicken Sie dann auf den Ordnercontainer für die übergebenen Ordner, den persönlichen Formular Container und schließlich Organisations-Container.</span><span class="sxs-lookup"><span data-stu-id="11a7b-132">The default form library provider searches first the local container, then the folder container for the passed-in folder, the personal form container and, finally, the organization container.</span></span>
  
<span data-ttu-id="11a7b-133">Nachrichtenklassennamen sind immer noch nie Unicode-ANSI-Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="11a7b-133">Message class names are always ANSI strings, never Unicode.</span></span>
  
<span data-ttu-id="11a7b-134">Die Klassen-ID für die Nachrichtenklasse aufgelöst wird als Teil des Formulars Informationen-Objekts zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="11a7b-134">The class identifier for the resolved message class is returned as part of the form information object.</span></span> <span data-ttu-id="11a7b-135">Ein Formular Viewer sollte nicht auf der Annahme verwendet werden, dass die Klassen-ID in der OLE-Bibliothek erst vorhanden ist, nachdem der Formular-Viewer die [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) -Methode oder die [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) -Methode aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="11a7b-135">A form viewer should not work on the assumption that the class identifier exists in the OLE library until after the form viewer has called either the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) method or the [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="11a7b-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11a7b-136">See also</span></span>



[<span data-ttu-id="11a7b-137">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="11a7b-137">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)
  
[<span data-ttu-id="11a7b-138">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="11a7b-138">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="11a7b-139">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="11a7b-139">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="11a7b-140">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="11a7b-140">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

