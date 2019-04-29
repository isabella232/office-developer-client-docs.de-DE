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
# <a name="imapiformmgrresolvemultiplemessageclasses"></a><span data-ttu-id="d3334-103">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="d3334-103">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>

  
  
<span data-ttu-id="d3334-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d3334-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d3334-105">Löst eine Gruppe von Nachrichtenklassen in Ihre Formulare innerhalb eines Formular Containers auf und gibt ein Array von Formular Informationsobjekten für diese Formulare zurück.</span><span class="sxs-lookup"><span data-stu-id="d3334-105">Resolves a group of message classes to their forms within a form container, and returns an array of form information objects for those forms.</span></span>
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClasses,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a><span data-ttu-id="d3334-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3334-106">Parameters</span></span>

 <span data-ttu-id="d3334-107">_pMsgClasses_</span><span class="sxs-lookup"><span data-stu-id="d3334-107">_pMsgClasses_</span></span>
  
> <span data-ttu-id="d3334-108">in Ein Zeiger auf ein Array, das die Namen der aufzulösenden Nachrichtenklassen enthält.</span><span class="sxs-lookup"><span data-stu-id="d3334-108">[in] A pointer to an array that contains the names of the message classes to resolve.</span></span>
    
 <span data-ttu-id="d3334-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d3334-109">_ulFlags_</span></span>
  
> <span data-ttu-id="d3334-110">in Eine Bitmaske von Flags, die die Auflösung der Nachrichtenklassen steuert.</span><span class="sxs-lookup"><span data-stu-id="d3334-110">[in] A bitmask of flags that controls how the message classes are resolved.</span></span> <span data-ttu-id="d3334-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="d3334-111">The following flag can be set:</span></span>
    
<span data-ttu-id="d3334-112">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="d3334-112">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="d3334-113">Nur Nachrichtenklassen Zeichenfolgen, die exakt übereinstimmen, sollten aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="d3334-113">Only message class strings that are an exact match should be resolved.</span></span>
    
<span data-ttu-id="d3334-114">MAPIFORM_LOCALONLY</span><span class="sxs-lookup"><span data-stu-id="d3334-114">MAPIFORM_LOCALONLY</span></span>
  
> <span data-ttu-id="d3334-115">Verwenden Sie keine zwischengespeicherten Formulare.</span><span class="sxs-lookup"><span data-stu-id="d3334-115">Do not include cached forms.</span></span>
    
 <span data-ttu-id="d3334-116">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="d3334-116">_pFolderFocus_</span></span>
  
> <span data-ttu-id="d3334-117">in Ein Zeiger auf den Ordner, der das Formular enthält, dessen Nachrichtenklasse aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="d3334-117">[in] A pointer to the folder that contains the form whose message class is being resolved.</span></span> <span data-ttu-id="d3334-118">Der _pFolderFocus_ -Parameter kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="d3334-118">The  _pFolderFocus_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="d3334-119">_ppfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="d3334-119">_ppfrminfoarray_</span></span>
  
> <span data-ttu-id="d3334-120">Out Ein Zeiger auf einen Zeiger auf ein Array von Formular Informationsobjekten.</span><span class="sxs-lookup"><span data-stu-id="d3334-120">[out] A pointer to a pointer to an array of form information objects.</span></span> <span data-ttu-id="d3334-121">Wenn ein Formular-Viewer im _pMsgClasses_ -Parameter den Wert NULL übergibt, enthält der _ppfrminfoarray_ -parameterformular Informationsobjekte für alle Formulare im Container.</span><span class="sxs-lookup"><span data-stu-id="d3334-121">If a form viewer passes NULL in the  _pMsgClasses_ parameter, the  _ppfrminfoarray_ parameter contains form information objects for all forms in the container.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d3334-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d3334-122">Return value</span></span>

<span data-ttu-id="d3334-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="d3334-123">S_OK</span></span> 
  
> <span data-ttu-id="d3334-124">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="d3334-124">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d3334-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d3334-125">Remarks</span></span>

<span data-ttu-id="d3334-126">Formular Betrachter rufen die **IMAPIFormMgr:: ResolveMultipleMessageClasses** -Methode auf, um eine Gruppe von Nachrichtenklassen in Formulare in einem Formular Container aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="d3334-126">Form viewers call the **IMAPIFormMgr::ResolveMultipleMessageClasses** method to resolve a group of message classes to forms within a form container.</span></span> <span data-ttu-id="d3334-127">Das Array der in _ppfrminfoarray_ zurückgegebenen Formular Informationsobjekte bietet weiteren Zugriff auf die einzelnen Eigenschaften der Formulare.</span><span class="sxs-lookup"><span data-stu-id="d3334-127">The array of form information objects returned in  _ppfrminfoarray_ provides further access to each of the forms' properties.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d3334-128">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="d3334-128">Notes to callers</span></span>

<span data-ttu-id="d3334-129">Um eine Gruppe von Nachrichtenklassen in Formulare aufzulösen, übergibt ein Formular Betrachter ein Array von Nachrichtenklassennamen, die aufgelöst werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d3334-129">To resolve a group of message classes to forms, a form viewer passes in an array of message class names to be resolved.</span></span> <span data-ttu-id="d3334-130">Um die Auflösung genau zu erzwingen (das heißt, um die Auflösung einer Basisklasse der Nachrichtenklasse zu verhindern, wenn ein genau übereinstimmender Formularserver nicht verfügbar ist), kann das MAPIFORM_EXACTMATCH-Flag im _ulFlags_ -Parameter übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="d3334-130">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class when an exactly matching form server is not available) the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="d3334-131">Nachrichtenklassennamen sind immer ANSI-Zeichenfolgen, nie Unicode.</span><span class="sxs-lookup"><span data-stu-id="d3334-131">Message class names are always ANSI strings, never Unicode.</span></span>
  
<span data-ttu-id="d3334-132">Wenn eine Nachrichtenklasse nicht in ein Formular aufgelöst werden kann, wird für diese Nachrichtenklasse im Formular Informations Array NULL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d3334-132">If a message class cannot be resolved to a form, NULL is returned for that message class in the form information array.</span></span> <span data-ttu-id="d3334-133">Selbst wenn die Methode S_OK zurückgibt, sollten die Formular Betrachter daher nicht davon ausgehen, dass alle Nachrichtenklassen erfolgreich aufgelöst wurden.</span><span class="sxs-lookup"><span data-stu-id="d3334-133">Therefore, even if the method returns S_OK, form viewers should not work on the assumption that all message classes have been successfully resolved.</span></span> <span data-ttu-id="d3334-134">Stattdessen sollten Formular Betrachter die Werte im zurückgegebenen Array überprüfen.</span><span class="sxs-lookup"><span data-stu-id="d3334-134">Instead, form viewers should check the values in the returned array.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d3334-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3334-135">See also</span></span>



[<span data-ttu-id="d3334-136">IMAPIFormMgr::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="d3334-136">IMAPIFormMgr::ResolveMessageClass</span></span>](imapiformmgr-resolvemessageclass.md)
  
[<span data-ttu-id="d3334-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d3334-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

