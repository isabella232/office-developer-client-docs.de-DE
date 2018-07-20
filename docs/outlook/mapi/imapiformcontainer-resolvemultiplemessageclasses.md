---
title: IMAPIFormContainerResolveMultipleMessageClasses
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.ResolveMultipleMessageCla
api_type:
- COM
ms.assetid: f18c2dd1-366f-48b4-b335-ebbc0651f467
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c1da292943d6e4d9625c6ce37019c630471e200b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792157"
---
# <a name="imapiformcontainerresolvemultiplemessageclasses"></a><span data-ttu-id="5f9a2-103">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="5f9a2-103">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>

  
  
<span data-ttu-id="5f9a2-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5f9a2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5f9a2-105">Eine Gruppe von Nachrichtenklassen in Formularen in einem Formular Container aufgelöst wird, und gibt ein Array von Formular Informationen Objekte für diese Formulare.</span><span class="sxs-lookup"><span data-stu-id="5f9a2-105">Resolves a group of message classes to their forms in a form container and returns an array of form information objects for those forms.</span></span>
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClassArray,
  ULONG ulFlags,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a><span data-ttu-id="5f9a2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f9a2-106">Parameters</span></span>

 <span data-ttu-id="5f9a2-107">_pMsgClassArray_</span><span class="sxs-lookup"><span data-stu-id="5f9a2-107">_pMsgClassArray_</span></span>
  
> <span data-ttu-id="5f9a2-108">[in] Ein Zeiger auf ein Array, das die Namen der Nachrichtenklassen aufzulösende enthält.</span><span class="sxs-lookup"><span data-stu-id="5f9a2-108">[in] A pointer to an array that contains the names of the message classes to resolve.</span></span> <span data-ttu-id="5f9a2-109">Nachrichtenklassennamen sind immer noch nie Unicode-ANSI-Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="5f9a2-109">Message class names are always ANSI strings, never Unicode.</span></span>
    
 <span data-ttu-id="5f9a2-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5f9a2-110">_ulFlags_</span></span>
  
> <span data-ttu-id="5f9a2-111">[in] Eine Bitmaske aus Flags, die steuert, wie die Nachrichtenklassen aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="5f9a2-111">[in] A bitmask of flags that controls how the message classes are resolved.</span></span> <span data-ttu-id="5f9a2-112">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="5f9a2-112">The following flag can be set:</span></span>
    
<span data-ttu-id="5f9a2-113">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="5f9a2-113">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="5f9a2-114">Nur Nachricht Klasse Zeichenfolgen, die eine genaue Übereinstimmung sollten aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="5f9a2-114">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="5f9a2-115">_ppfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="5f9a2-115">_ppfrminfoarray_</span></span>
  
> <span data-ttu-id="5f9a2-116">[out] Ein Zeiger auf einen Zeiger auf ein Array von Formular Informationen-Objekten.</span><span class="sxs-lookup"><span data-stu-id="5f9a2-116">[out] A pointer to a pointer to an array of form information objects.</span></span> <span data-ttu-id="5f9a2-117">Wenn eine Clientanwendung NULL im Parameter _pMsgClassArray_ übergibt, enthält der Parameter _Ppfrminfoarray_ Formular Informationen-Objekte für alle Formulare im Container.</span><span class="sxs-lookup"><span data-stu-id="5f9a2-117">If a client application passes NULL in the  _pMsgClassArray_ parameter, the  _ppfrminfoarray_ parameter contains form information objects for all forms in the container.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5f9a2-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5f9a2-118">Return value</span></span>

<span data-ttu-id="5f9a2-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="5f9a2-119">S_OK</span></span> 
  
> <span data-ttu-id="5f9a2-120">Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="5f9a2-120">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5f9a2-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5f9a2-121">Remarks</span></span>

<span data-ttu-id="5f9a2-122">Clientanwendungen rufen Sie die **IMAPIFormContainer::ResolveMultipleMessageClasses** -Methode, um eine Gruppe von Nachrichtenklassen für Formulare innerhalb eines Containers Formular zu beheben.</span><span class="sxs-lookup"><span data-stu-id="5f9a2-122">Client applications call the **IMAPIFormContainer::ResolveMultipleMessageClasses** method to resolve a group of message classes to forms within a form container.</span></span> <span data-ttu-id="5f9a2-123">Das Objektarray Formular Informationen zurückgegeben, die im Parameter _Ppfrminfoarray_ bietet weitere Zugriff auf jede der Forms-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5f9a2-123">The array of form information objects returned in the  _ppfrminfoarray_ parameter provides further access to each of the forms' properties.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5f9a2-124">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="5f9a2-124">Notes to callers</span></span>

<span data-ttu-id="5f9a2-125">Um eine Gruppe von Nachrichtenklassen für Formulare zu beheben, übergeben Sie ein Array von Nachrichtenklassennamen aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="5f9a2-125">To resolve a group of message classes to forms, pass in an array of message class names to be resolved.</span></span> <span data-ttu-id="5f9a2-126">So erzwingen Sie die Auflösung genau sein (d. h., um auf eine Basisklasse der Nachrichtenklasse Lösung zu verhindern), die Kennzeichen MAPIFORM_EXACTMATCH im _UlFlags_ -Parameter übergeben werden können.</span><span class="sxs-lookup"><span data-stu-id="5f9a2-126">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="5f9a2-127">Wenn eine Nachrichtenklasse in einem Formular aufgelöst werden kann, wird NULL für die Nachrichtenklasse in das Formular Informationen Array zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5f9a2-127">If a message class cannot be resolved to a form, NULL is returned for that message class in the form information array.</span></span> <span data-ttu-id="5f9a2-128">Aus diesem Grund, auch wenn die Methode S_OK zurückgegeben wird, gehen Sie nicht, dass alle Nachrichtenklassen erfolgreich behoben wurden.</span><span class="sxs-lookup"><span data-stu-id="5f9a2-128">Therefore, even if the method returns S_OK, do not assume that all message classes have been successfully resolved.</span></span> <span data-ttu-id="5f9a2-129">Überprüfen Sie stattdessen die Werte in das zurückgegebene Array.</span><span class="sxs-lookup"><span data-stu-id="5f9a2-129">Instead, check the values in the returned array.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5f9a2-130">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="5f9a2-130">MFCMAPI reference</span></span>

<span data-ttu-id="5f9a2-131">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="5f9a2-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5f9a2-132">**Datei**</span><span class="sxs-lookup"><span data-stu-id="5f9a2-132">**File**</span></span>|<span data-ttu-id="5f9a2-133">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="5f9a2-133">**Function**</span></span>|<span data-ttu-id="5f9a2-134">**Comment**</span><span class="sxs-lookup"><span data-stu-id="5f9a2-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5f9a2-135">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="5f9a2-135">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="5f9a2-136">CFormContainerDlg::OnResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="5f9a2-136">CFormContainerDlg::OnResolveMultipleMessageClasses</span></span>  <br/> |<span data-ttu-id="5f9a2-137">MFCMAPI (engl.) verwendet die **IMAPIFormContainer::ResolveMultipleMessageClasses** -Methode, um ein Formular zu suchen, die eine Reihe von Nachrichtenklassen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5f9a2-137">MFCMAPI uses the **IMAPIFormContainer::ResolveMultipleMessageClasses** method to locate a form that is associated with a set of message classes.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5f9a2-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f9a2-138">See also</span></span>



[<span data-ttu-id="5f9a2-139">IMAPIFormContainer::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="5f9a2-139">IMAPIFormContainer::ResolveMessageClass</span></span>](imapiformcontainer-resolvemessageclass.md)
  
[<span data-ttu-id="5f9a2-140">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5f9a2-140">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="5f9a2-141">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="5f9a2-141">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

