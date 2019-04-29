---
title: IMAPIFormContainerResolveMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.ResolveMessageClass
api_type:
- COM
ms.assetid: 9ce13f11-5787-4ea5-a84f-b1e3824529ee
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c0954d6f8b14b4088ece2ac276b045b6c163ed98
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408551"
---
# <a name="imapiformcontainerresolvemessageclass"></a><span data-ttu-id="a54e2-103">IMAPIFormContainer::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="a54e2-103">IMAPIFormContainer::ResolveMessageClass</span></span>

  
  
<span data-ttu-id="a54e2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a54e2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a54e2-105">Löst eine Nachrichtenklasse in Ihrem Formular in einem Formular Container auf und gibt ein Formular Informationsobjekt für dieses Formular zurück.</span><span class="sxs-lookup"><span data-stu-id="a54e2-105">Resolves a message class to its form in a form container and returns a form information object for that form.</span></span>
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMessageClass,
  ULONG ulFlags,
  LPMAPIFORMINFO FAR * ppforminfo
);
```

## <a name="parameters"></a><span data-ttu-id="a54e2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a54e2-106">Parameters</span></span>

 <span data-ttu-id="a54e2-107">_szMessageClass_</span><span class="sxs-lookup"><span data-stu-id="a54e2-107">_szMessageClass_</span></span>
  
> <span data-ttu-id="a54e2-108">in Eine Zeichenfolge, die die zu lösende Nachrichtenklasse benennt.</span><span class="sxs-lookup"><span data-stu-id="a54e2-108">[in] A string that names the message class being resolved.</span></span> <span data-ttu-id="a54e2-109">Nachrichtenklassennamen sind immer ANSI-Zeichenfolgen, nie Unicode.</span><span class="sxs-lookup"><span data-stu-id="a54e2-109">Message class names are always ANSI strings, never Unicode.</span></span>
    
 <span data-ttu-id="a54e2-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a54e2-110">_ulFlags_</span></span>
  
> <span data-ttu-id="a54e2-111">in Eine Bitmaske von Flags, die die Auflösung der Nachrichtenklasse steuert.</span><span class="sxs-lookup"><span data-stu-id="a54e2-111">[in] A bitmask of flags that controls how the message class is resolved.</span></span> <span data-ttu-id="a54e2-112">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="a54e2-112">The following flag can be set:</span></span>
    
<span data-ttu-id="a54e2-113">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="a54e2-113">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="a54e2-114">Nur Nachrichtenklassen Zeichenfolgen, die exakt übereinstimmen, sollten aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="a54e2-114">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="a54e2-115">_ppforminfo_</span><span class="sxs-lookup"><span data-stu-id="a54e2-115">_ppforminfo_</span></span>
  
> <span data-ttu-id="a54e2-116">Out Ein Zeiger auf einen Zeiger auf das zurückgegebene Formular Informationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="a54e2-116">[out] A pointer to a pointer to the returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a54e2-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a54e2-117">Return value</span></span>

<span data-ttu-id="a54e2-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="a54e2-118">S_OK</span></span> 
  
> <span data-ttu-id="a54e2-119">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="a54e2-119">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="a54e2-120">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="a54e2-120">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="a54e2-121">Die Nachrichtenklasse, die im _szMessageClass_ -Parameter übergeben wird, stimmt nicht mit der Nachrichtenklasse für alle Formulare im Formular Container überein.</span><span class="sxs-lookup"><span data-stu-id="a54e2-121">The message class passed in the  _szMessageClass_ parameter does not match the message class for any form in the form container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a54e2-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a54e2-122">Remarks</span></span>

<span data-ttu-id="a54e2-123">Client Anwendungen rufen die **IMAPIFormContainer:: ResolveMessageClass** -Methode auf, um eine Nachrichtenklasse in ein Formular in einem Formular Container aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="a54e2-123">Client applications call the **IMAPIFormContainer::ResolveMessageClass** method to resolve a message class to a form within a form container.</span></span> <span data-ttu-id="a54e2-124">Das im _ppforminfo_ -Parameter zurückgegebene Formular Informationsobjekt bietet weiteren Zugriff auf die Eigenschaften des Formulars mit der angegebenen Nachrichtenklasse.</span><span class="sxs-lookup"><span data-stu-id="a54e2-124">The form information object returned in the  _ppforminfo_ parameter provides further access to the properties of the form with the given message class.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a54e2-125">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="a54e2-125">Notes to callers</span></span>

<span data-ttu-id="a54e2-126">Um eine Nachrichtenklasse in ein Formular aufzulösen, geben Sie den Namen der zu lösenden Nachrichtenklasse ein (beispielsweise `IPM.HelpDesk.Software`).</span><span class="sxs-lookup"><span data-stu-id="a54e2-126">To resolve a message class to a form, pass in the name of the message class to be resolved (for example,  `IPM.HelpDesk.Software`).</span></span> <span data-ttu-id="a54e2-127">Um die Genauigkeit der Auflösung zu erzwingen (das heißt, um eine Lösung für eine Basisklasse der Nachrichtenklasse zu verhindern), kann das MAPIFORM_EXACTMATCH-Flag im _ulFlags_ -Parameter übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="a54e2-127">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="a54e2-128">Der Klassenbezeichner für die aufgelöste Nachrichtenklasse wird als Teil des Form Information-Objekts zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a54e2-128">The class identifier for the resolved message class is returned as part of the form information object.</span></span> <span data-ttu-id="a54e2-129">Gehen Sie nicht davon aus, dass der Klassenbezeichner in der OLE-Bibliothek vorhanden ist, bis Sie die [IMAPIFormMgr::P repareform](imapiformmgr-prepareform.md) -oder [IMAPIFormMgr:: CreateForm](imapiformmgr-createform.md) -Methode aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="a54e2-129">Do not assume that the class identifier exists in the OLE library until after you call either the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) or [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a54e2-130">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="a54e2-130">MFCMAPI reference</span></span>

<span data-ttu-id="a54e2-131">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a54e2-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a54e2-132">**Datei**</span><span class="sxs-lookup"><span data-stu-id="a54e2-132">**File**</span></span>|<span data-ttu-id="a54e2-133">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="a54e2-133">**Function**</span></span>|<span data-ttu-id="a54e2-134">**Comment**</span><span class="sxs-lookup"><span data-stu-id="a54e2-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a54e2-135">FormContainerDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="a54e2-135">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="a54e2-136">CFormContainerDlg:: OnResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="a54e2-136">CFormContainerDlg::OnResolveMessageClass</span></span>  <br/> |<span data-ttu-id="a54e2-137">MFCMAPI verwendet die **IMAPIFormContainer:: ResolveMessageClass** -Methode, um ein Formular zu suchen, das einer Nachrichtenklasse zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a54e2-137">MFCMAPI uses the **IMAPIFormContainer::ResolveMessageClass** method to locate a form that is associated with a message class.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a54e2-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a54e2-138">See also</span></span>



[<span data-ttu-id="a54e2-139">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a54e2-139">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)
  
[<span data-ttu-id="a54e2-140">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="a54e2-140">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="a54e2-141">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="a54e2-141">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="a54e2-142">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a54e2-142">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)

