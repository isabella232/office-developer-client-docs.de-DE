---
title: IMAPIFormMgrSelectMultipleForms
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.SelectMultipleForms
api_type:
- COM
ms.assetid: 172f8f53-b837-4286-9236-3f72806d7f1f
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 096437f10c5b992a1db55f6a856c38021a81b99a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792206"
---
# <a name="imapiformmgrselectmultipleforms"></a><span data-ttu-id="a88ea-103">IMAPIFormMgr::SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="a88ea-103">IMAPIFormMgr::SelectMultipleForms</span></span>

  
  
<span data-ttu-id="a88ea-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a88ea-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a88ea-105">Zeigt ein Dialogfeld, mit dem den Benutzer mehrere Formulare auswählen kann, und gibt ein Array von Formular Informationsobjekten, die diesen Formularen zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="a88ea-105">Presents a dialog box that enables the user to select multiple forms, and returns an array of form information objects that describe those forms.</span></span>
  
```cpp
HRESULT SelectMultipleForms(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR pszTitle,
  LPMAPIFOLDER pfld,
  LPMAPIFORMINFOARRAY pfrminfoarray,
  LPMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a><span data-ttu-id="a88ea-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a88ea-106">Parameters</span></span>

 <span data-ttu-id="a88ea-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="a88ea-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="a88ea-108">[in] Ein Handle für das übergeordnete Fenster im angezeigten Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="a88ea-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="a88ea-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a88ea-109">_ulFlags_</span></span>
  
> <span data-ttu-id="a88ea-110">[in] Eine Bitmaske aus Flags, die den Typ der übergebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="a88ea-110">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="a88ea-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="a88ea-111">The following flag can be set:</span></span>
    
<span data-ttu-id="a88ea-112">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a88ea-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a88ea-113">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="a88ea-113">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="a88ea-114">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="a88ea-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="a88ea-115">_pszTitle_</span><span class="sxs-lookup"><span data-stu-id="a88ea-115">_pszTitle_</span></span>
  
> <span data-ttu-id="a88ea-116">[in] Ein Zeiger auf eine Zeichenfolge, die Beschriftung des Dialogfelds enthält.</span><span class="sxs-lookup"><span data-stu-id="a88ea-116">[in] A pointer to a string that contains the caption of the dialog box.</span></span> <span data-ttu-id="a88ea-117">Wenn der Parameter _PszTitle_ NULL ist, stellt der Formular-Bibliotheksanbieter, der die Formulare enthält einen Standardtitel.</span><span class="sxs-lookup"><span data-stu-id="a88ea-117">If the  _pszTitle_ parameter is NULL, the form library provider that provides the forms supplies a default caption.</span></span> 
    
 <span data-ttu-id="a88ea-118">_pfld_</span><span class="sxs-lookup"><span data-stu-id="a88ea-118">_pfld_</span></span>
  
> <span data-ttu-id="a88ea-119">[in] Ein Zeiger auf den Ordner aus, wählen Sie die Formulare.</span><span class="sxs-lookup"><span data-stu-id="a88ea-119">[in] A pointer to the folder from which to select the forms.</span></span> <span data-ttu-id="a88ea-120">Wenn der Parameter _Pfld_ NULL ist, werden die Formulare aus dem lokalen persönlich oder Organisation Formular Container ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="a88ea-120">If the  _pfld_ parameter is NULL, the forms are selected from the local, personal, or organization form container.</span></span> 
    
 <span data-ttu-id="a88ea-121">_pfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="a88ea-121">_pfrminfoarray_</span></span>
  
> <span data-ttu-id="a88ea-122">[in] Ein Zeiger auf ein Array von Formular Informationen-Objekten, die für den Benutzer bereits ausgewählt sind.</span><span class="sxs-lookup"><span data-stu-id="a88ea-122">[in] A pointer to an array of form information objects that are preselected for the user.</span></span>
    
 <span data-ttu-id="a88ea-123">_ppfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="a88ea-123">_ppfrminfoarray_</span></span>
  
> <span data-ttu-id="a88ea-124">[out] Ein Zeiger auf einen Zeiger auf das zurückgegebene Array von Formular Informationen-Objekte.</span><span class="sxs-lookup"><span data-stu-id="a88ea-124">[out] A pointer to a pointer to the returned array of form information objects.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a88ea-125">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="a88ea-125">Return value</span></span>

<span data-ttu-id="a88ea-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="a88ea-126">S_OK</span></span> 
  
> <span data-ttu-id="a88ea-127">Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a88ea-127">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="a88ea-128">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="a88ea-128">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="a88ea-129">Entweder die Option MAPI_UNICODE festgelegt wurde und die Implementierung unterstützt keine Unicode oder Parameter MAPI_UNICODE nicht festgelegt wurde und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="a88ea-129">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="a88ea-130">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="a88ea-130">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="a88ea-131">Der Benutzer hat den Vorgang in der Regel durch Klicken auf die Schaltfläche **Abbrechen** im Dialogfeld abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="a88ea-131">The user canceled the operation, typically by clicking the **Cancel** button in the dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a88ea-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a88ea-132">Remarks</span></span>

<span data-ttu-id="a88ea-133">Formular Viewer rufen Sie die **IMAPIFormMgr::SelectMultipleForms** -Methode zum ersten vorhanden ein Dialogfeld, mit dem den Benutzer mehrere Formulare auswählen kann, und klicken Sie dann Informationen zum Abrufen eines Arrays des Formulars Objekte, die die ausgewählten Formulare beschreiben.</span><span class="sxs-lookup"><span data-stu-id="a88ea-133">Form viewers call the **IMAPIFormMgr::SelectMultipleForms** method to first present a dialog box that enables the user to select multiple forms and then to retrieve an array of form information objects that describe the selected forms.</span></span> <span data-ttu-id="a88ea-134">Das Dialogfeld **SelectMultipleForms** zeigt alle Formulare, unabhängig davon, ob sie ausgeblendet werden (d. h., ob ihre ausgeblendeten Eigenschaften deaktiviert sind).</span><span class="sxs-lookup"><span data-stu-id="a88ea-134">The **SelectMultipleForms** dialog box displays all forms, whether or not they are hidden (that is, whether or not their hidden properties are clear).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a88ea-135">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="a88ea-135">Notes to implementers</span></span>

<span data-ttu-id="a88ea-136">Wenn ein Formular Viewer die Option MAPI_UNICODE im Parameter _UlFlags_ übergibt, werden alle Zeichenfolgen Unicode.</span><span class="sxs-lookup"><span data-stu-id="a88ea-136">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings are Unicode.</span></span> <span data-ttu-id="a88ea-137">Formular Bibliothek Anbieter, die keine für Unicode-Zeichenfolgen Unterstützung sollte MAPI_E_BAD_CHARWIDTH zurückgegeben, wenn der Parameter MAPI_UNICODE übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a88ea-137">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a88ea-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a88ea-138">See also</span></span>



[<span data-ttu-id="a88ea-139">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a88ea-139">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

