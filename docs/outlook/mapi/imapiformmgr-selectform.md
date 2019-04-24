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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c25f352e7fa607a46741164574a4ba91d4026edf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321672"
---
# <a name="imapiformmgrselectform"></a><span data-ttu-id="146b5-103">IMAPIFormMgr::SelectForm</span><span class="sxs-lookup"><span data-stu-id="146b5-103">IMAPIFormMgr::SelectForm</span></span>

  
  
<span data-ttu-id="146b5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="146b5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="146b5-105">Zeigt ein Dialogfeld an, in dem der Benutzer ein Formular auswählen und ein Formular Informationsobjekt zurückgibt, das dieses Formular beschreibt.</span><span class="sxs-lookup"><span data-stu-id="146b5-105">Presents a dialog box that enables the user to select a form, and returns a form information object that describes that form.</span></span>
  
```cpp
HRESULT SelectForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR pszTitle,
  LPMAPIFOLDER pfld,
  LPMAPIFORMINFO FAR * ppfrminfoReturned
);
```

## <a name="parameters"></a><span data-ttu-id="146b5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="146b5-106">Parameters</span></span>

 <span data-ttu-id="146b5-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="146b5-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="146b5-108">in Ein Handle für das übergeordnete Fenster des angezeigten Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="146b5-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="146b5-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="146b5-109">_ulFlags_</span></span>
  
> <span data-ttu-id="146b5-110">in Eine Bitmaske von Flags, die den Typ der übergebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="146b5-110">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="146b5-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="146b5-111">The following flag can be set:</span></span>
    
<span data-ttu-id="146b5-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="146b5-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="146b5-113">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="146b5-113">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="146b5-114">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="146b5-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="146b5-115">_pszTitle_</span><span class="sxs-lookup"><span data-stu-id="146b5-115">_pszTitle_</span></span>
  
> <span data-ttu-id="146b5-116">in Ein Zeiger auf eine Zeichenfolge, die die Beschriftung des Dialogfelds enthält.</span><span class="sxs-lookup"><span data-stu-id="146b5-116">[in] A pointer to a string that contains the caption of the dialog box.</span></span> <span data-ttu-id="146b5-117">Wenn der _pszTitle_ -Parameter NULL ist, stellt der Formularbibliothek Anbieter eine Standardbeschriftung bereit.</span><span class="sxs-lookup"><span data-stu-id="146b5-117">If the  _pszTitle_ parameter is NULL, the form library provider supplies a default caption.</span></span> 
    
 <span data-ttu-id="146b5-118">_pfld_</span><span class="sxs-lookup"><span data-stu-id="146b5-118">_pfld_</span></span>
  
> <span data-ttu-id="146b5-119">in Ein Zeiger auf den Ordner, aus dem das Formular ausgewählt werden soll.</span><span class="sxs-lookup"><span data-stu-id="146b5-119">[in] A pointer to the folder from which to select the form.</span></span> <span data-ttu-id="146b5-120">Wenn der _pfld_ -Parameter NULL ist, kann das Formular aus dem Container für lokale, persönliche oder organisatorische Formulare ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="146b5-120">If the  _pfld_ parameter is NULL, the form can be selected from the local, personal, or organization form container.</span></span> 
    
 <span data-ttu-id="146b5-121">_ppfrminfoReturned_</span><span class="sxs-lookup"><span data-stu-id="146b5-121">_ppfrminfoReturned_</span></span>
  
> <span data-ttu-id="146b5-122">Out Ein Zeiger auf einen Zeiger auf das zurückgegebene Formular Informationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="146b5-122">[out] A pointer to a pointer to the returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="146b5-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="146b5-123">Return value</span></span>

<span data-ttu-id="146b5-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="146b5-124">S_OK</span></span> 
  
> <span data-ttu-id="146b5-125">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="146b5-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="146b5-126">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="146b5-126">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="146b5-127">Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="146b5-127">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="146b5-128">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="146b5-128">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="146b5-129">Der Benutzer hat den Vorgang abgebrochen, indem er in der Regel auf die Schaltfläche **Abbrechen** im Dialogfeld geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="146b5-129">The user canceled the operation, typically by clicking the **Cancel** button in the dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="146b5-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="146b5-130">Remarks</span></span>

<span data-ttu-id="146b5-131">Formular Betrachter rufen die **IMAPIFormMgr:: SelectForm** -Methode auf, um zuerst ein Dialogfeld darzustellen, das es dem Benutzer ermöglicht, ein Formular auszuwählen und dann ein Formular Informationsobjekt abzurufen, das das ausgewählte Formular beschreibt.</span><span class="sxs-lookup"><span data-stu-id="146b5-131">Form viewers call the **IMAPIFormMgr::SelectForm** method to first present a dialog box that enables the user to select a form and then to retrieve a form information object that describes the selected form.</span></span> <span data-ttu-id="146b5-132">Das Dialogfeld schränkt den Benutzer ein, um ein einzelnes Formular auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="146b5-132">The dialog box constrains the user to select a single form.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="146b5-133">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="146b5-133">Notes to callers</span></span>

<span data-ttu-id="146b5-134">Im Dialogfeld **SelectForm** werden nur Formulare angezeigt, die nicht ausgeblendet sind (also Formulare, deren ausgeblendete Eigenschaften deaktiviert sind).</span><span class="sxs-lookup"><span data-stu-id="146b5-134">The **SelectForm** dialog box displays only forms that are not hidden (that is, forms that have their hidden properties clear).</span></span> <span data-ttu-id="146b5-135">Wenn ein Formular Betrachter das MAPI_UNICODE-Flag im _ulFlags_ -Parameter übergibt, sind alle Zeichenfolgen Unicode.</span><span class="sxs-lookup"><span data-stu-id="146b5-135">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings are Unicode.</span></span> <span data-ttu-id="146b5-136">Formularbibliothek Anbieter, die Unicode-Zeichenfolgen nicht unterstützen, sollten MAPI_E_BAD_CHARWIDTH zurückgeben, wenn MAPI_UNICODE übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="146b5-136">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="146b5-137">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="146b5-137">MFCMAPI reference</span></span>

<span data-ttu-id="146b5-138">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="146b5-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="146b5-139">**Datei**</span><span class="sxs-lookup"><span data-stu-id="146b5-139">**File**</span></span>|<span data-ttu-id="146b5-140">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="146b5-140">**Function**</span></span>|<span data-ttu-id="146b5-141">**Comment**</span><span class="sxs-lookup"><span data-stu-id="146b5-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="146b5-142">FolderDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="146b5-142">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="146b5-143">CFolderDlg:: OnSelectForm</span><span class="sxs-lookup"><span data-stu-id="146b5-143">CFolderDlg::OnSelectForm</span></span>  <br/> |<span data-ttu-id="146b5-144">MFCMAPI verwendet die **IMAPIFormMgr:: SelectForm** -Methode, um ein Formular auszuwählen und Informationen zum Formular an ein oder mehrere Protokolle zu senden.</span><span class="sxs-lookup"><span data-stu-id="146b5-144">MFCMAPI uses the **IMAPIFormMgr::SelectForm** method to select a form and send information about the form to one or more logs.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="146b5-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="146b5-145">See also</span></span>



[<span data-ttu-id="146b5-146">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="146b5-146">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="146b5-147">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="146b5-147">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

