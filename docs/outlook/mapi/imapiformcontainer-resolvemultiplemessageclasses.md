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
ms.openlocfilehash: 0730da9c3877985853e2cd0a55420e64fbd98e0c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412541"
---
# <a name="imapiformcontainerresolvemultiplemessageclasses"></a><span data-ttu-id="3e9a6-103">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="3e9a6-103">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>

  
  
<span data-ttu-id="3e9a6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3e9a6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3e9a6-105">Löst eine Gruppe von Nachrichtenklassen in Ihre Formulare in einem Formular Container auf und gibt ein Array von Formular Informationsobjekten für diese Formulare zurück.</span><span class="sxs-lookup"><span data-stu-id="3e9a6-105">Resolves a group of message classes to their forms in a form container and returns an array of form information objects for those forms.</span></span>
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClassArray,
  ULONG ulFlags,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a><span data-ttu-id="3e9a6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e9a6-106">Parameters</span></span>

 <span data-ttu-id="3e9a6-107">_pMsgClassArray_</span><span class="sxs-lookup"><span data-stu-id="3e9a6-107">_pMsgClassArray_</span></span>
  
> <span data-ttu-id="3e9a6-108">in Ein Zeiger auf ein Array, das die Namen der aufzulösenden Nachrichtenklassen enthält.</span><span class="sxs-lookup"><span data-stu-id="3e9a6-108">[in] A pointer to an array that contains the names of the message classes to resolve.</span></span> <span data-ttu-id="3e9a6-109">Nachrichtenklassennamen sind immer ANSI-Zeichenfolgen, nie Unicode.</span><span class="sxs-lookup"><span data-stu-id="3e9a6-109">Message class names are always ANSI strings, never Unicode.</span></span>
    
 <span data-ttu-id="3e9a6-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3e9a6-110">_ulFlags_</span></span>
  
> <span data-ttu-id="3e9a6-111">in Eine Bitmaske von Flags, die die Auflösung der Nachrichtenklassen steuert.</span><span class="sxs-lookup"><span data-stu-id="3e9a6-111">[in] A bitmask of flags that controls how the message classes are resolved.</span></span> <span data-ttu-id="3e9a6-112">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="3e9a6-112">The following flag can be set:</span></span>
    
<span data-ttu-id="3e9a6-113">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="3e9a6-113">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="3e9a6-114">Nur Nachrichtenklassen Zeichenfolgen, die exakt übereinstimmen, sollten aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="3e9a6-114">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="3e9a6-115">_ppfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="3e9a6-115">_ppfrminfoarray_</span></span>
  
> <span data-ttu-id="3e9a6-116">Out Ein Zeiger auf einen Zeiger auf ein Array von Formular Informationsobjekten.</span><span class="sxs-lookup"><span data-stu-id="3e9a6-116">[out] A pointer to a pointer to an array of form information objects.</span></span> <span data-ttu-id="3e9a6-117">Wenn eine Clientanwendung im _pMsgClassArray_ -Parameter den Wert NULL übergibt, enthält der _ppfrminfoarray_ -parameterformular Informationsobjekte für alle Formulare im Container.</span><span class="sxs-lookup"><span data-stu-id="3e9a6-117">If a client application passes NULL in the  _pMsgClassArray_ parameter, the  _ppfrminfoarray_ parameter contains form information objects for all forms in the container.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3e9a6-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3e9a6-118">Return value</span></span>

<span data-ttu-id="3e9a6-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="3e9a6-119">S_OK</span></span> 
  
> <span data-ttu-id="3e9a6-120">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="3e9a6-120">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3e9a6-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3e9a6-121">Remarks</span></span>

<span data-ttu-id="3e9a6-122">Client Anwendungen rufen die **IMAPIFormContainer:: ResolveMultipleMessageClasses** -Methode auf, um eine Gruppe von Nachrichtenklassen in Formulare in einem Formular Container aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="3e9a6-122">Client applications call the **IMAPIFormContainer::ResolveMultipleMessageClasses** method to resolve a group of message classes to forms within a form container.</span></span> <span data-ttu-id="3e9a6-123">Das im _ppfrminfoarray_ -Parameter zurückgegebene Array von Formular Informationsobjekten bietet weiteren Zugriff auf die einzelnen Eigenschaften der Formulare.</span><span class="sxs-lookup"><span data-stu-id="3e9a6-123">The array of form information objects returned in the  _ppfrminfoarray_ parameter provides further access to each of the forms' properties.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3e9a6-124">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="3e9a6-124">Notes to callers</span></span>

<span data-ttu-id="3e9a6-125">Um eine Gruppe von Nachrichtenklassen in Formulare aufzulösen, führen Sie ein Array von Nachrichtenklassennamen aus, die aufgelöst werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3e9a6-125">To resolve a group of message classes to forms, pass in an array of message class names to be resolved.</span></span> <span data-ttu-id="3e9a6-126">Um die Genauigkeit der Auflösung zu erzwingen (das heißt, um eine Lösung für eine Basisklasse der Nachrichtenklasse zu verhindern), kann das MAPIFORM_EXACTMATCH-Flag im _ulFlags_ -Parameter übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="3e9a6-126">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="3e9a6-127">Wenn eine Nachrichtenklasse nicht in ein Formular aufgelöst werden kann, wird für diese Nachrichtenklasse im Formular Informations Array NULL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3e9a6-127">If a message class cannot be resolved to a form, NULL is returned for that message class in the form information array.</span></span> <span data-ttu-id="3e9a6-128">Daher sollten Sie nicht davon ausgehen, dass alle Nachrichtenklassen erfolgreich aufgelöst wurden, selbst wenn die Methode S_OK zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="3e9a6-128">Therefore, even if the method returns S_OK, do not assume that all message classes have been successfully resolved.</span></span> <span data-ttu-id="3e9a6-129">Überprüfen Sie stattdessen die Werte im zurückgegebenen Array.</span><span class="sxs-lookup"><span data-stu-id="3e9a6-129">Instead, check the values in the returned array.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3e9a6-130">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="3e9a6-130">MFCMAPI reference</span></span>

<span data-ttu-id="3e9a6-131">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="3e9a6-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3e9a6-132">**Datei**</span><span class="sxs-lookup"><span data-stu-id="3e9a6-132">**File**</span></span>|<span data-ttu-id="3e9a6-133">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="3e9a6-133">**Function**</span></span>|<span data-ttu-id="3e9a6-134">**Comment**</span><span class="sxs-lookup"><span data-stu-id="3e9a6-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3e9a6-135">FormContainerDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="3e9a6-135">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="3e9a6-136">CFormContainerDlg:: OnResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="3e9a6-136">CFormContainerDlg::OnResolveMultipleMessageClasses</span></span>  <br/> |<span data-ttu-id="3e9a6-137">MFCMAPI verwendet die **IMAPIFormContainer:: ResolveMultipleMessageClasses** -Methode, um ein Formular zu suchen, das einer Gruppe von Nachrichtenklassen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3e9a6-137">MFCMAPI uses the **IMAPIFormContainer::ResolveMultipleMessageClasses** method to locate a form that is associated with a set of message classes.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3e9a6-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e9a6-138">See also</span></span>



[<span data-ttu-id="3e9a6-139">IMAPIFormContainer::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="3e9a6-139">IMAPIFormContainer::ResolveMessageClass</span></span>](imapiformcontainer-resolvemessageclass.md)
  
[<span data-ttu-id="3e9a6-140">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3e9a6-140">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="3e9a6-141">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="3e9a6-141">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

