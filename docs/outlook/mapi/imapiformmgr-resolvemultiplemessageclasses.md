---
title: IMAPIFormMgrResolveMultipleMessageClasses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.ResolveMultipleMessageClasses
api_type:
- COM
ms.assetid: d3cc6658-e46d-42dd-b1ac-65c88cfef8ca
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 515061c6c208008c4752e5ff2f23933a4c259c00
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428018"
---
# <a name="imapiformmgrresolvemultiplemessageclasses"></a><span data-ttu-id="9ddfc-103">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="9ddfc-103">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>

  
  
<span data-ttu-id="9ddfc-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ddfc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ddfc-105">Löst eine Gruppe von Nachrichtenklassen in ihre Formulare in einem Formularcontainer auf und gibt ein Array von Formularinformationsobjekten für diese Formulare zurück.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-105">Resolves a group of message classes to their forms within a form container, and returns an array of form information objects for those forms.</span></span>
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClasses,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a><span data-ttu-id="9ddfc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ddfc-106">Parameters</span></span>

 <span data-ttu-id="9ddfc-107">_pMsgClasses_</span><span class="sxs-lookup"><span data-stu-id="9ddfc-107">_pMsgClasses_</span></span>
  
> <span data-ttu-id="9ddfc-108">[in] Ein Zeiger auf ein Array, das die Namen der zu auflösende Nachrichtenklassen enthält.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-108">[in] A pointer to an array that contains the names of the message classes to resolve.</span></span>
    
 <span data-ttu-id="9ddfc-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9ddfc-109">_ulFlags_</span></span>
  
> <span data-ttu-id="9ddfc-110">[in] Eine Bitmaske mit Flags, die steuert, wie die Nachrichtenklassen aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-110">[in] A bitmask of flags that controls how the message classes are resolved.</span></span> <span data-ttu-id="9ddfc-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="9ddfc-111">The following flag can be set:</span></span>
    
<span data-ttu-id="9ddfc-112">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="9ddfc-112">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="9ddfc-113">Es sollten nur Nachrichtenklassenzeichenfolgen aufgelöst werden, die eine genaue Übereinstimmung sind.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-113">Only message class strings that are an exact match should be resolved.</span></span>
    
<span data-ttu-id="9ddfc-114">MAPIFORM_LOCALONLY</span><span class="sxs-lookup"><span data-stu-id="9ddfc-114">MAPIFORM_LOCALONLY</span></span>
  
> <span data-ttu-id="9ddfc-115">Schließen Sie keine zwischengespeicherten Formulare ein.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-115">Do not include cached forms.</span></span>
    
 <span data-ttu-id="9ddfc-116">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="9ddfc-116">_pFolderFocus_</span></span>
  
> <span data-ttu-id="9ddfc-117">[in] Ein Zeiger auf den Ordner, der das Formular enthält, dessen Nachrichtenklasse aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-117">[in] A pointer to the folder that contains the form whose message class is being resolved.</span></span> <span data-ttu-id="9ddfc-118">Der  _pFolderFocus-Parameter_ kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-118">The  _pFolderFocus_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="9ddfc-119">_ppfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="9ddfc-119">_ppfrminfoarray_</span></span>
  
> <span data-ttu-id="9ddfc-120">[out] Ein Zeiger auf einen Zeiger auf ein Array von Formularinformationsobjekten.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-120">[out] A pointer to a pointer to an array of form information objects.</span></span> <span data-ttu-id="9ddfc-121">Wenn ein Formularanzeiger NULL im  _pMsgClasses-Parameter_ übergibt, enthält der  _ppfrminfoarray-Parameter_ Formularinformationsobjekte für alle Formulare im Container.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-121">If a form viewer passes NULL in the  _pMsgClasses_ parameter, the  _ppfrminfoarray_ parameter contains form information objects for all forms in the container.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9ddfc-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9ddfc-122">Return value</span></span>

<span data-ttu-id="9ddfc-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="9ddfc-123">S_OK</span></span> 
  
> <span data-ttu-id="9ddfc-124">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-124">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9ddfc-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9ddfc-125">Remarks</span></span>

<span data-ttu-id="9ddfc-126">Formularbetrachter rufen die **IMAPIFormMgr::ResolveMultipleMessageClasses-Methode** auf, um eine Gruppe von Nachrichtenklassen in Formulare innerhalb eines Formularcontainers zu auflösen.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-126">Form viewers call the **IMAPIFormMgr::ResolveMultipleMessageClasses** method to resolve a group of message classes to forms within a form container.</span></span> <span data-ttu-id="9ddfc-127">Das Array von Formularinformationsobjekten, die in  _ppfrminfoarray_ zurückgegeben werden, bietet weiteren Zugriff auf die Eigenschaften der einzelnen Formulare.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-127">The array of form information objects returned in  _ppfrminfoarray_ provides further access to each of the forms' properties.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9ddfc-128">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="9ddfc-128">Notes to callers</span></span>

<span data-ttu-id="9ddfc-129">Um eine Gruppe von Nachrichtenklassen in Formulare zu auflösen, übergibt eine Formularanzeige ein Array von Nachrichtenklassennamen, die aufgelöst werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-129">To resolve a group of message classes to forms, a form viewer passes in an array of message class names to be resolved.</span></span> <span data-ttu-id="9ddfc-130">Um zu erzwingen, dass die Auflösung exakt ist (d. h. um die Auflösung zu einer Basisklasse der Nachrichtenklasse zu verhindern, wenn kein exakt übereinstimmender Formularserver verfügbar ist), kann das MAPIFORM_EXACTMATCH-Flag im  _ulFlags-Parameter_ übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-130">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class when an exactly matching form server is not available) the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="9ddfc-131">Nachrichtenklassennamen sind immer ANSI-Zeichenfolgen, nie Unicode.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-131">Message class names are always ANSI strings, never Unicode.</span></span>
  
<span data-ttu-id="9ddfc-132">Wenn eine Nachrichtenklasse nicht in ein Formular aufgelöst werden kann, wird NULL für diese Nachrichtenklasse im Formularinformationsarray zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-132">If a message class cannot be resolved to a form, NULL is returned for that message class in the form information array.</span></span> <span data-ttu-id="9ddfc-133">Daher sollten Formularanzeigen nicht unter der Annahme funktionieren, dass alle Nachrichtenklassen erfolgreich aufgelöst wurden, auch wenn die Methode S_OK zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-133">Therefore, even if the method returns S_OK, form viewers should not work on the assumption that all message classes have been successfully resolved.</span></span> <span data-ttu-id="9ddfc-134">Stattdessen sollten Formularbetrachter die Werte im zurückgegebenen Array überprüfen.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-134">Instead, form viewers should check the values in the returned array.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9ddfc-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ddfc-135">See also</span></span>



[<span data-ttu-id="9ddfc-136">IMAPIFormMgr::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="9ddfc-136">IMAPIFormMgr::ResolveMessageClass</span></span>](imapiformmgr-resolvemessageclass.md)
  
[<span data-ttu-id="9ddfc-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9ddfc-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

