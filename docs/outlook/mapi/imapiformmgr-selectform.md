---
title: IMAPIFormMgrSelectForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.SelectForm
api_type:
- COM
ms.assetid: c1cfe71b-01f3-429a-8b4c-73191a2ffea0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3c6242c9a926341908cb86645a8ea8586a9ca598
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586354"
---
# <a name="imapiformmgrselectform"></a><span data-ttu-id="31f19-103">IMAPIFormMgr::SelectForm</span><span class="sxs-lookup"><span data-stu-id="31f19-103">IMAPIFormMgr::SelectForm</span></span>

  
  
<span data-ttu-id="31f19-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31f19-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="31f19-105">Zeigt ein Dialogfeld, mit dem den Benutzer ein Formular auswählen an und gibt ein Form-Informationen-Objekt, das dieses Formular beschreibt.</span><span class="sxs-lookup"><span data-stu-id="31f19-105">Presents a dialog box that enables the user to select a form, and returns a form information object that describes that form.</span></span>
  
```cpp
HRESULT SelectForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR pszTitle,
  LPMAPIFOLDER pfld,
  LPMAPIFORMINFO FAR * ppfrminfoReturned
);
```

## <a name="parameters"></a><span data-ttu-id="31f19-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="31f19-106">Parameters</span></span>

 <span data-ttu-id="31f19-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="31f19-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="31f19-108">[in] Ein Handle für das übergeordnete Fenster im angezeigten Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="31f19-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="31f19-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="31f19-109">_ulFlags_</span></span>
  
> <span data-ttu-id="31f19-110">[in] Eine Bitmaske aus Flags, die den Typ der übergebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="31f19-110">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="31f19-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="31f19-111">The following flag can be set:</span></span>
    
<span data-ttu-id="31f19-112">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="31f19-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="31f19-113">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="31f19-113">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="31f19-114">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="31f19-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="31f19-115">_pszTitle_</span><span class="sxs-lookup"><span data-stu-id="31f19-115">_pszTitle_</span></span>
  
> <span data-ttu-id="31f19-116">[in] Ein Zeiger auf eine Zeichenfolge, die Beschriftung des Dialogfelds enthält.</span><span class="sxs-lookup"><span data-stu-id="31f19-116">[in] A pointer to a string that contains the caption of the dialog box.</span></span> <span data-ttu-id="31f19-117">Wenn der Parameter _PszTitle_ NULL ist, stellt der Form Library Anbieter einen Standardtitel.</span><span class="sxs-lookup"><span data-stu-id="31f19-117">If the  _pszTitle_ parameter is NULL, the form library provider supplies a default caption.</span></span> 
    
 <span data-ttu-id="31f19-118">_pfld_</span><span class="sxs-lookup"><span data-stu-id="31f19-118">_pfld_</span></span>
  
> <span data-ttu-id="31f19-119">[in] Ein Zeiger auf den Ordner aus der das Formular auswählen.</span><span class="sxs-lookup"><span data-stu-id="31f19-119">[in] A pointer to the folder from which to select the form.</span></span> <span data-ttu-id="31f19-120">Wenn der Parameter _Pfld_ NULL ist, kann das Formular aus dem lokalen persönlich oder Organisation Formular Container ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="31f19-120">If the  _pfld_ parameter is NULL, the form can be selected from the local, personal, or organization form container.</span></span> 
    
 <span data-ttu-id="31f19-121">_ppfrminfoReturned_</span><span class="sxs-lookup"><span data-stu-id="31f19-121">_ppfrminfoReturned_</span></span>
  
> <span data-ttu-id="31f19-122">[out] Ein Zeiger auf einen Zeiger auf das zurückgegebene Informationen Formularobjekt.</span><span class="sxs-lookup"><span data-stu-id="31f19-122">[out] A pointer to a pointer to the returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="31f19-123">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="31f19-123">Return value</span></span>

<span data-ttu-id="31f19-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="31f19-124">S_OK</span></span> 
  
> <span data-ttu-id="31f19-125">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="31f19-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="31f19-126">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="31f19-126">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="31f19-127">Entweder die Option MAPI_UNICODE festgelegt wurde und die Implementierung unterstützt keine Unicode oder Parameter MAPI_UNICODE nicht festgelegt wurde und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="31f19-127">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="31f19-128">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="31f19-128">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="31f19-129">Der Benutzer hat den Vorgang in der Regel durch Klicken auf die Schaltfläche **Abbrechen** im Dialogfeld abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="31f19-129">The user canceled the operation, typically by clicking the **Cancel** button in the dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="31f19-130">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="31f19-130">Remarks</span></span>

<span data-ttu-id="31f19-131">Formular Viewer rufen Sie die **IMAPIFormMgr::SelectForm** -Methode zum ersten Gegenwart ein Dialogfeld, mit dem den Benutzer ein Formular auswählen, und klicken Sie dann zum Abrufen eines Formulars Informationen-Objekts, die das ausgewählte Formular beschreibt.</span><span class="sxs-lookup"><span data-stu-id="31f19-131">Form viewers call the **IMAPIFormMgr::SelectForm** method to first present a dialog box that enables the user to select a form and then to retrieve a form information object that describes the selected form.</span></span> <span data-ttu-id="31f19-132">Das Dialogfeld schränkt des Benutzers ein einzelnes Formular auswählen.</span><span class="sxs-lookup"><span data-stu-id="31f19-132">The dialog box constrains the user to select a single form.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="31f19-133">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="31f19-133">Notes to callers</span></span>

<span data-ttu-id="31f19-134">Das Dialogfeld **SelectForm** zeigt nur für Formulare, die nicht ausgeblendet werden (d. h., deaktivieren Sie Formulare, die ihre ausgeblendeten Eigenschaften haben).</span><span class="sxs-lookup"><span data-stu-id="31f19-134">The **SelectForm** dialog box displays only forms that are not hidden (that is, forms that have their hidden properties clear).</span></span> <span data-ttu-id="31f19-135">Wenn ein Formular Viewer die Option MAPI_UNICODE im Parameter _UlFlags_ übergibt, werden alle Zeichenfolgen Unicode.</span><span class="sxs-lookup"><span data-stu-id="31f19-135">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings are Unicode.</span></span> <span data-ttu-id="31f19-136">Formular Bibliothek Anbieter, die keine für Unicode-Zeichenfolgen Unterstützung sollte MAPI_E_BAD_CHARWIDTH zurückgegeben, wenn der Parameter MAPI_UNICODE übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="31f19-136">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="31f19-137">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="31f19-137">MFCMAPI reference</span></span>

<span data-ttu-id="31f19-138">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="31f19-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="31f19-139">**Datei**</span><span class="sxs-lookup"><span data-stu-id="31f19-139">**File**</span></span>|<span data-ttu-id="31f19-140">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="31f19-140">**Function**</span></span>|<span data-ttu-id="31f19-141">**Comment**</span><span class="sxs-lookup"><span data-stu-id="31f19-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="31f19-142">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="31f19-142">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="31f19-143">CFolderDlg::OnSelectForm</span><span class="sxs-lookup"><span data-stu-id="31f19-143">CFolderDlg::OnSelectForm</span></span>  <br/> |<span data-ttu-id="31f19-144">MFCMAPI (engl.) wird die **IMAPIFormMgr::SelectForm** -Methode verwendet, um ein Formular auswählen und die Informationen zum Formular an einen oder mehrere Protokolle senden.</span><span class="sxs-lookup"><span data-stu-id="31f19-144">MFCMAPI uses the **IMAPIFormMgr::SelectForm** method to select a form and send information about the form to one or more logs.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="31f19-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31f19-145">See also</span></span>



[<span data-ttu-id="31f19-146">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="31f19-146">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="31f19-147">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="31f19-147">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

