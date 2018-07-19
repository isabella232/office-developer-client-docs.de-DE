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
ms.openlocfilehash: 713a177d5ceddf5fd4d97a0e35d87b2250748faf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792152"
---
# <a name="imapiformcontainerresolvemessageclass"></a><span data-ttu-id="3c8a1-103">IMAPIFormContainer::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="3c8a1-103">IMAPIFormContainer::ResolveMessageClass</span></span>

  
  
<span data-ttu-id="3c8a1-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3c8a1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3c8a1-105">Löst eine Nachrichtenklasse in seiner Form in einem Formular Container und ein Formular Informationen-Objekt für dieses Formular zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3c8a1-105">Resolves a message class to its form in a form container and returns a form information object for that form.</span></span>
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMessageClass,
  ULONG ulFlags,
  LPMAPIFORMINFO FAR * ppforminfo
);
```

## <a name="parameters"></a><span data-ttu-id="3c8a1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3c8a1-106">Parameters</span></span>

 <span data-ttu-id="3c8a1-107">_szMessageClass_</span><span class="sxs-lookup"><span data-stu-id="3c8a1-107">_szMessageClass_</span></span>
  
> <span data-ttu-id="3c8a1-108">[in] Eine Zeichenfolge, die den Namen die Nachrichtenklasse aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="3c8a1-108">[in] A string that names the message class being resolved.</span></span> <span data-ttu-id="3c8a1-109">Nachrichtenklassennamen sind immer noch nie Unicode-ANSI-Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="3c8a1-109">Message class names are always ANSI strings, never Unicode.</span></span>
    
 <span data-ttu-id="3c8a1-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3c8a1-110">_ulFlags_</span></span>
  
> <span data-ttu-id="3c8a1-111">[in] Eine Bitmaske aus Flags, die steuert, wie die Nachrichtenklasse aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="3c8a1-111">[in] A bitmask of flags that controls how the message class is resolved.</span></span> <span data-ttu-id="3c8a1-112">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="3c8a1-112">The following flag can be set:</span></span>
    
<span data-ttu-id="3c8a1-113">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="3c8a1-113">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="3c8a1-114">Nur Nachricht Klasse Zeichenfolgen, die eine genaue Übereinstimmung sollten aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="3c8a1-114">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="3c8a1-115">_ppforminfo_</span><span class="sxs-lookup"><span data-stu-id="3c8a1-115">_ppforminfo_</span></span>
  
> <span data-ttu-id="3c8a1-116">[out] Ein Zeiger auf einen Zeiger auf das zurückgegebene Informationen Formularobjekt.</span><span class="sxs-lookup"><span data-stu-id="3c8a1-116">[out] A pointer to a pointer to the returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3c8a1-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3c8a1-117">Return value</span></span>

<span data-ttu-id="3c8a1-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="3c8a1-118">S_OK</span></span> 
  
> <span data-ttu-id="3c8a1-119">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="3c8a1-119">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="3c8a1-120">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="3c8a1-120">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="3c8a1-121">Die Nachrichtenklasse in der _SzMessageClass_ -Parameter übergeben entspricht nicht die Nachrichtenklasse für jedes Formular im Formular-Container.</span><span class="sxs-lookup"><span data-stu-id="3c8a1-121">The message class passed in the  _szMessageClass_ parameter does not match the message class for any form in the form container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3c8a1-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3c8a1-122">Remarks</span></span>

<span data-ttu-id="3c8a1-123">Clientanwendungen rufen Sie die **IMAPIFormContainer::ResolveMessageClass** -Methode, um eine Nachrichtenklasse zu einem Formular in einem Formular Container zu beheben.</span><span class="sxs-lookup"><span data-stu-id="3c8a1-123">Client applications call the **IMAPIFormContainer::ResolveMessageClass** method to resolve a message class to a form within a form container.</span></span> <span data-ttu-id="3c8a1-124">Das Formular Informationen-Objekt zurückgegeben, die im Parameter _Ppforminfo_ bietet weitere Zugriff auf die Eigenschaften des Formulars mit der angegebenen Nachrichtenklasse.</span><span class="sxs-lookup"><span data-stu-id="3c8a1-124">The form information object returned in the  _ppforminfo_ parameter provides further access to the properties of the form with the given message class.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3c8a1-125">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="3c8a1-125">Notes to callers</span></span>

<span data-ttu-id="3c8a1-126">Um eine Nachrichtenklasse zu einem Formular zu beheben, übergeben Sie den Namen der Nachrichtenklasse aufgelöst werden (beispielsweise `IPM.HelpDesk.Software`).</span><span class="sxs-lookup"><span data-stu-id="3c8a1-126">To resolve a message class to a form, pass in the name of the message class to be resolved (for example,  `IPM.HelpDesk.Software`).</span></span> <span data-ttu-id="3c8a1-127">So erzwingen Sie die Auflösung genau sein (d. h., um auf eine Basisklasse der Nachrichtenklasse Lösung zu verhindern), die Kennzeichen MAPIFORM_EXACTMATCH im _UlFlags_ -Parameter übergeben werden können.</span><span class="sxs-lookup"><span data-stu-id="3c8a1-127">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="3c8a1-128">Die Klassen-ID für die Nachrichtenklasse aufgelöst wird als Teil des Formulars Informationen-Objekts zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3c8a1-128">The class identifier for the resolved message class is returned as part of the form information object.</span></span> <span data-ttu-id="3c8a1-129">Nehmen Sie nicht an, dass die Klassen-ID in der OLE-Bibliothek erst vorhanden ist, nachdem Sie die [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) oder [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) -Methode aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="3c8a1-129">Do not assume that the class identifier exists in the OLE library until after you call either the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) or [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3c8a1-130">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="3c8a1-130">MFCMAPI reference</span></span>

<span data-ttu-id="3c8a1-131">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="3c8a1-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3c8a1-132">**Datei**</span><span class="sxs-lookup"><span data-stu-id="3c8a1-132">**File**</span></span>|<span data-ttu-id="3c8a1-133">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="3c8a1-133">**Function**</span></span>|<span data-ttu-id="3c8a1-134">**Comment**</span><span class="sxs-lookup"><span data-stu-id="3c8a1-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3c8a1-135">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="3c8a1-135">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="3c8a1-136">CFormContainerDlg::OnResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="3c8a1-136">CFormContainerDlg::OnResolveMessageClass</span></span>  <br/> |<span data-ttu-id="3c8a1-137">MFCMAPI (engl.) verwendet die **IMAPIFormContainer::ResolveMessageClass** -Methode, um ein Formular zu suchen, die mit einer Nachrichtenklasse zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3c8a1-137">MFCMAPI uses the **IMAPIFormContainer::ResolveMessageClass** method to locate a form that is associated with a message class.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3c8a1-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c8a1-138">See also</span></span>



[<span data-ttu-id="3c8a1-139">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="3c8a1-139">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)
  
[<span data-ttu-id="3c8a1-140">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="3c8a1-140">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="3c8a1-141">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="3c8a1-141">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="3c8a1-142">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3c8a1-142">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)

