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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c40d853c49645638c2ec4001d86e64a1b2d2e381
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420311"
---
# <a name="imapiformmgrselectmultipleforms"></a><span data-ttu-id="422d1-103">IMAPIFormMgr::SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="422d1-103">IMAPIFormMgr::SelectMultipleForms</span></span>

  
  
<span data-ttu-id="422d1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="422d1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="422d1-105">Stellt ein Dialogfeld vor, in dem der Benutzer mehrere Formulare auswählen kann, und gibt ein Array von Formularinformationsobjekten zurück, die diese Formulare beschreiben.</span><span class="sxs-lookup"><span data-stu-id="422d1-105">Presents a dialog box that enables the user to select multiple forms, and returns an array of form information objects that describe those forms.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="422d1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="422d1-106">Parameters</span></span>

 <span data-ttu-id="422d1-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="422d1-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="422d1-108">[in] Ein Handle zum übergeordneten Fenster des angezeigten Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="422d1-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="422d1-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="422d1-109">_ulFlags_</span></span>
  
> <span data-ttu-id="422d1-110">[in] Eine Bitmaske mit Flags, die den Typ der übergebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="422d1-110">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="422d1-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="422d1-111">The following flag can be set:</span></span>
    
<span data-ttu-id="422d1-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="422d1-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="422d1-113">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="422d1-113">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="422d1-114">Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="422d1-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="422d1-115">_pszTitle_</span><span class="sxs-lookup"><span data-stu-id="422d1-115">_pszTitle_</span></span>
  
> <span data-ttu-id="422d1-116">[in] Ein Zeiger auf eine Zeichenfolge, die die Beschriftung des Dialogfelds enthält.</span><span class="sxs-lookup"><span data-stu-id="422d1-116">[in] A pointer to a string that contains the caption of the dialog box.</span></span> <span data-ttu-id="422d1-117">Wenn der  _pszTitle-Parameter_ NULL ist, stellt der Formularbibliotheksanbieter, der die Formulare zur Verfügung stellt, eine Standardbeschriftung zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="422d1-117">If the  _pszTitle_ parameter is NULL, the form library provider that provides the forms supplies a default caption.</span></span> 
    
 <span data-ttu-id="422d1-118">_pfld_</span><span class="sxs-lookup"><span data-stu-id="422d1-118">_pfld_</span></span>
  
> <span data-ttu-id="422d1-119">[in] Ein Zeiger auf den Ordner, aus dem die Formulare ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="422d1-119">[in] A pointer to the folder from which to select the forms.</span></span> <span data-ttu-id="422d1-120">Wenn der  _pfld-Parameter_ NULL ist, werden die Formulare aus dem lokalen, persönlichen oder Organisationsformularcontainer ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="422d1-120">If the  _pfld_ parameter is NULL, the forms are selected from the local, personal, or organization form container.</span></span> 
    
 <span data-ttu-id="422d1-121">_pfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="422d1-121">_pfrminfoarray_</span></span>
  
> <span data-ttu-id="422d1-122">[in] Ein Zeiger auf ein Array von Formularinformationsobjekten, die für den Benutzer vorab ausgewählt sind.</span><span class="sxs-lookup"><span data-stu-id="422d1-122">[in] A pointer to an array of form information objects that are preselected for the user.</span></span>
    
 <span data-ttu-id="422d1-123">_ppfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="422d1-123">_ppfrminfoarray_</span></span>
  
> <span data-ttu-id="422d1-124">[out] Ein Zeiger auf einen Zeiger auf das zurückgegebene Array von Formularinformationsobjekten.</span><span class="sxs-lookup"><span data-stu-id="422d1-124">[out] A pointer to a pointer to the returned array of form information objects.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="422d1-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="422d1-125">Return value</span></span>

<span data-ttu-id="422d1-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="422d1-126">S_OK</span></span> 
  
> <span data-ttu-id="422d1-127">Der Aufruf war erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="422d1-127">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="422d1-128">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="422d1-128">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="422d1-129">Entweder wurde MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="422d1-129">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="422d1-130">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="422d1-130">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="422d1-131">Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die **Schaltfläche** Abbrechen im Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="422d1-131">The user canceled the operation, typically by clicking the **Cancel** button in the dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="422d1-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="422d1-132">Remarks</span></span>

<span data-ttu-id="422d1-133">Formularbetrachter rufen die **IMAPIFormMgr::SelectMultipleForms-Methode** auf, um zunächst ein Dialogfeld anzuzeigen, in dem der Benutzer mehrere Formulare auswählen und dann ein Array von Formularinformationsobjekten abrufen kann, die die ausgewählten Formulare beschreiben.</span><span class="sxs-lookup"><span data-stu-id="422d1-133">Form viewers call the **IMAPIFormMgr::SelectMultipleForms** method to first present a dialog box that enables the user to select multiple forms and then to retrieve an array of form information objects that describe the selected forms.</span></span> <span data-ttu-id="422d1-134">Im **Dialogfeld SelectMultipleForms** werden alle Formulare angezeigt, unabhängig davon, ob sie ausgeblendet sind (d. h., ob ihre ausgeblendeten Eigenschaften klar sind oder nicht).</span><span class="sxs-lookup"><span data-stu-id="422d1-134">The **SelectMultipleForms** dialog box displays all forms, whether or not they are hidden (that is, whether or not their hidden properties are clear).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="422d1-135">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="422d1-135">Notes to implementers</span></span>

<span data-ttu-id="422d1-136">Wenn ein Formularanzeiger das MAPI_UNICODE im  _ulFlags-Parameter_ übergibt, sind alle Zeichenfolgen Unicode.</span><span class="sxs-lookup"><span data-stu-id="422d1-136">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings are Unicode.</span></span> <span data-ttu-id="422d1-137">Formularbibliotheksanbieter, die keine Unicode-Zeichenfolgen unterstützen, sollten MAPI_E_BAD_CHARWIDTH zurückgeben, MAPI_UNICODE übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="422d1-137">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="422d1-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="422d1-138">See also</span></span>



[<span data-ttu-id="422d1-139">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="422d1-139">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

