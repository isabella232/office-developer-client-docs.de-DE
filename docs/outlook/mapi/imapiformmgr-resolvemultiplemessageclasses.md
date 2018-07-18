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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ad2014d1d003a4d80646ed1b679f0d3827341c1b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792181"
---
# <a name="imapiformmgrresolvemultiplemessageclasses"></a><span data-ttu-id="9ffb0-103">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="9ffb0-103">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>

  
  
<span data-ttu-id="9ffb0-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9ffb0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9ffb0-105">Eine Gruppe von Nachrichtenklassen in ihre Formulare in einem Formular Container aufgelöst wird, und gibt ein Array von Formular Informationen Objekte für diese Formulare.</span><span class="sxs-lookup"><span data-stu-id="9ffb0-105">Resolves a group of message classes to their forms within a form container, and returns an array of form information objects for those forms.</span></span>
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClasses,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a><span data-ttu-id="9ffb0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ffb0-106">Parameters</span></span>

 <span data-ttu-id="9ffb0-107">_pMsgClasses_</span><span class="sxs-lookup"><span data-stu-id="9ffb0-107">_pMsgClasses_</span></span>
  
> <span data-ttu-id="9ffb0-108">[in] Ein Zeiger auf ein Array, das die Namen der Nachrichtenklassen aufzulösende enthält.</span><span class="sxs-lookup"><span data-stu-id="9ffb0-108">[in] A pointer to an array that contains the names of the message classes to resolve.</span></span>
    
 <span data-ttu-id="9ffb0-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9ffb0-109">_ulFlags_</span></span>
  
> <span data-ttu-id="9ffb0-110">[in] Eine Bitmaske aus Flags, die steuert, wie die Nachrichtenklassen aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="9ffb0-110">[in] A bitmask of flags that controls how the message classes are resolved.</span></span> <span data-ttu-id="9ffb0-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="9ffb0-111">The following flag can be set:</span></span>
    
<span data-ttu-id="9ffb0-112">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="9ffb0-112">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="9ffb0-113">Nur Nachricht Klasse Zeichenfolgen, die eine genaue Übereinstimmung sollten aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="9ffb0-113">Only message class strings that are an exact match should be resolved.</span></span>
    
<span data-ttu-id="9ffb0-114">MAPIFORM_LOCALONLY</span><span class="sxs-lookup"><span data-stu-id="9ffb0-114">MAPIFORM_LOCALONLY</span></span>
  
> <span data-ttu-id="9ffb0-115">Schließen Sie nicht zwischengespeicherte Formulare.</span><span class="sxs-lookup"><span data-stu-id="9ffb0-115">Do not include cached forms.</span></span>
    
 <span data-ttu-id="9ffb0-116">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="9ffb0-116">_pFolderFocus_</span></span>
  
> <span data-ttu-id="9ffb0-117">[in] Ein Zeiger auf den Ordner, der das Formular enthält, deren Nachrichtenklasse aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="9ffb0-117">[in] A pointer to the folder that contains the form whose message class is being resolved.</span></span> <span data-ttu-id="9ffb0-118">Der Parameter _pFolderFocus_ kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="9ffb0-118">The  _pFolderFocus_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="9ffb0-119">_ppfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="9ffb0-119">_ppfrminfoarray_</span></span>
  
> <span data-ttu-id="9ffb0-120">[out] Ein Zeiger auf einen Zeiger auf ein Array von Formular Informationen-Objekten.</span><span class="sxs-lookup"><span data-stu-id="9ffb0-120">[out] A pointer to a pointer to an array of form information objects.</span></span> <span data-ttu-id="9ffb0-121">Wenn ein Formular Viewer NULL im Parameter _pMsgClasses_ übergibt, enthält der Parameter _Ppfrminfoarray_ Formular Informationen-Objekte für alle Formulare im Container.</span><span class="sxs-lookup"><span data-stu-id="9ffb0-121">If a form viewer passes NULL in the  _pMsgClasses_ parameter, the  _ppfrminfoarray_ parameter contains form information objects for all forms in the container.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9ffb0-122">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="9ffb0-122">Return value</span></span>

<span data-ttu-id="9ffb0-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="9ffb0-123">S_OK</span></span> 
  
> <span data-ttu-id="9ffb0-124">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="9ffb0-124">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9ffb0-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9ffb0-125">Remarks</span></span>

<span data-ttu-id="9ffb0-126">Formular Viewer rufen Sie die **IMAPIFormMgr::ResolveMultipleMessageClasses** -Methode, um eine Gruppe von Nachrichtenklassen für Formulare innerhalb eines Containers Formular zu beheben.</span><span class="sxs-lookup"><span data-stu-id="9ffb0-126">Form viewers call the **IMAPIFormMgr::ResolveMultipleMessageClasses** method to resolve a group of message classes to forms within a form container.</span></span> <span data-ttu-id="9ffb0-127">Das Array von Formular Informationen-Objekten, die in _Ppfrminfoarray_ zurückgegeben ermöglicht den Zugriff auf die Formulare Eigenschaften weiter.</span><span class="sxs-lookup"><span data-stu-id="9ffb0-127">The array of form information objects returned in  _ppfrminfoarray_ provides further access to each of the forms' properties.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9ffb0-128">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="9ffb0-128">Notes to callers</span></span>

<span data-ttu-id="9ffb0-129">Um eine Gruppe von Nachrichtenklassen in Formularen aufzulösen, übergibt ein Formular Viewer in einem Array von Nachrichtenklassennamen aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="9ffb0-129">To resolve a group of message classes to forms, a form viewer passes in an array of message class names to be resolved.</span></span> <span data-ttu-id="9ffb0-130">So erzwingen Sie die Auflösung genau sein (d. h., um auf eine Basisklasse der Nachrichtenklasse, wenn ein Formular genau übereinstimmenden Lösung zu verhindern Server ist nicht verfügbar) das Flag MAPIFORM_EXACTMATCH im _UlFlags_ -Parameter übergeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="9ffb0-130">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class when an exactly matching form server is not available) the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="9ffb0-131">Nachrichtenklassennamen sind immer noch nie Unicode-ANSI-Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="9ffb0-131">Message class names are always ANSI strings, never Unicode.</span></span>
  
<span data-ttu-id="9ffb0-132">Wenn eine Nachrichtenklasse in einem Formular aufgelöst werden kann, wird NULL für die Nachrichtenklasse in das Formular Informationen Array zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9ffb0-132">If a message class cannot be resolved to a form, NULL is returned for that message class in the form information array.</span></span> <span data-ttu-id="9ffb0-133">Aus diesem Grund, auch wenn die Methode gibt S_OK zurück, sollte Formular Viewer funktioniert nicht auf der Annahme, dass alle Nachrichtenklassen erfolgreich behoben wurden.</span><span class="sxs-lookup"><span data-stu-id="9ffb0-133">Therefore, even if the method returns S_OK, form viewers should not work on the assumption that all message classes have been successfully resolved.</span></span> <span data-ttu-id="9ffb0-134">Formular Viewer sollten Sie stattdessen die Werte im zurückgegebenen Array überprüfen.</span><span class="sxs-lookup"><span data-stu-id="9ffb0-134">Instead, form viewers should check the values in the returned array.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9ffb0-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ffb0-135">See also</span></span>



[<span data-ttu-id="9ffb0-136">IMAPIFormMgr::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="9ffb0-136">IMAPIFormMgr::ResolveMessageClass</span></span>](imapiformmgr-resolvemessageclass.md)
  
[<span data-ttu-id="9ffb0-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9ffb0-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

