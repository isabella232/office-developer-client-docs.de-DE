---
title: IMAPIFormMgrOpenFormContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.OpenFormContainer
api_type:
- COM
ms.assetid: df02bdc5-903a-4ce2-9f43-5f4513ea19b3
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 68a358c91e35c5a075e220794c78f4e5c96e43ee
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393117"
---
# <a name="imapiformmgropenformcontainer"></a><span data-ttu-id="a1cda-103">IMAPIFormMgr::OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="a1cda-103">IMAPIFormMgr::OpenFormContainer</span></span>

  
  
<span data-ttu-id="a1cda-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1cda-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1cda-105">Öffnet eine [IMAPIFormContainer](imapiformcontaineriunknown.md) -Schnittstelle für ein bestimmtes Formular Container.</span><span class="sxs-lookup"><span data-stu-id="a1cda-105">Opens an [IMAPIFormContainer](imapiformcontaineriunknown.md) interface for a specific form container.</span></span> 
  
```cpp
HRESULT OpenFormContainer(
  HFRMREG hfrmreg,
  LPUNKNOWN lpunk,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="a1cda-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1cda-106">Parameters</span></span>

 <span data-ttu-id="a1cda-107">_hfrmreg_</span><span class="sxs-lookup"><span data-stu-id="a1cda-107">_hfrmreg_</span></span>
  
> <span data-ttu-id="a1cda-108">[in] Eine HFRMREG-Enumeration, die zum Öffnen die Formularbibliothek angibt (d. h., die Container Formular öffnen).</span><span class="sxs-lookup"><span data-stu-id="a1cda-108">[in] An HFRMREG enumeration that indicates the form library to open (that is, the form container to open).</span></span> <span data-ttu-id="a1cda-109">Eine Enumeration HFRMREG ist eine Enumeration, die zu einem Formular Bibliotheksanbieter spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="a1cda-109">An HFRMREG enumeration is an enumeration that is specific to a form library provider.</span></span> <span data-ttu-id="a1cda-110">Die folgenden: möglichen Werte für HFRMREG</span><span class="sxs-lookup"><span data-stu-id="a1cda-110">Possible HFRMREG values include the following:</span></span>
    
<span data-ttu-id="a1cda-111">HFRMREG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="a1cda-111">HFRMREG_DEFAULT</span></span> 
  
> <span data-ttu-id="a1cda-112">Ein Container komfortable Formular.</span><span class="sxs-lookup"><span data-stu-id="a1cda-112">A convenient form container.</span></span>
    
<span data-ttu-id="a1cda-113">HFRMREG_FOLDER</span><span class="sxs-lookup"><span data-stu-id="a1cda-113">HFRMREG_FOLDER</span></span> 
  
> <span data-ttu-id="a1cda-114">Ein Ordnercontainer.</span><span class="sxs-lookup"><span data-stu-id="a1cda-114">A folder container.</span></span> 
    
<span data-ttu-id="a1cda-115">HFRMREG_PERSONAL</span><span class="sxs-lookup"><span data-stu-id="a1cda-115">HFRMREG_PERSONAL</span></span> 
  
> <span data-ttu-id="a1cda-116">Der Container für Standard-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="a1cda-116">The container for the default message store.</span></span> 
    
<span data-ttu-id="a1cda-117">HFRMREG_LOCAL</span><span class="sxs-lookup"><span data-stu-id="a1cda-117">HFRMREG_LOCAL</span></span> 
  
> <span data-ttu-id="a1cda-118">Ein Container für lokale Formular.</span><span class="sxs-lookup"><span data-stu-id="a1cda-118">A local form container.</span></span> 
    
 <span data-ttu-id="a1cda-119">_lpUnk_</span><span class="sxs-lookup"><span data-stu-id="a1cda-119">_lpunk_</span></span>
  
> <span data-ttu-id="a1cda-120">[in] Ein Zeiger auf das Objekt, für das die Schnittstelle geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="a1cda-120">[in] A pointer to the object for which the interface is opened.</span></span> <span data-ttu-id="a1cda-121">Der Parameter _Lpunk_ muss **null** sein, es sei denn, der Wert für den Parameter _Hfrmreg_ einen Zeiger erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a1cda-121">The  _lpunk_ parameter must be **null** unless the value for the  _hfrmreg_ parameter requires an object pointer.</span></span> 
    
 <span data-ttu-id="a1cda-122">_lppfcnt_</span><span class="sxs-lookup"><span data-stu-id="a1cda-122">_lppfcnt_</span></span>
  
> <span data-ttu-id="a1cda-123">[out] Ein Zeiger auf einen Zeiger auf das zurückgegebene Form Container-Objekt.</span><span class="sxs-lookup"><span data-stu-id="a1cda-123">[out] A pointer to a pointer to the returned form container object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a1cda-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a1cda-124">Return value</span></span>

<span data-ttu-id="a1cda-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="a1cda-125">S_OK</span></span> 
  
> <span data-ttu-id="a1cda-126">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="a1cda-126">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="a1cda-127">MAPI_E_NO_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="a1cda-127">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="a1cda-128">Das Objekt, das auf _Lpunk_ unterstützt nicht die erforderliche Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="a1cda-128">The object pointed to by  _lpunk_ does not support the required interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a1cda-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a1cda-129">Remarks</span></span>

<span data-ttu-id="a1cda-130">Formular Viewer rufen Sie die **IMAPIFormMgr::OpenFormContainer** -Methode, um eine **IMAPIFormContainer** -Schnittstelle für ein bestimmtes Formular Container zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a1cda-130">Form viewers call the **IMAPIFormMgr::OpenFormContainer** method to open an **IMAPIFormContainer** interface for a specific form container.</span></span> <span data-ttu-id="a1cda-131">Diese Schnittstelle kann dann für die Installation in und Entfernen von Formularen aus einem Formular Container verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a1cda-131">This interface can then be used for installing forms into and removing forms from a form container.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a1cda-132">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="a1cda-132">Notes to callers</span></span>

<span data-ttu-id="a1cda-133">Wenn der Wert in _Hfrmreg_ HFRMREG_FOLDER ist, der Schnittstellenbezeichner in _Lpunk_ verwendet muss ungleich **null** sein und muss [QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) -Methode Anrufe an eine Schnittstelle [IMAPIFolder](imapifolderimapicontainer.md) zulassen.</span><span class="sxs-lookup"><span data-stu-id="a1cda-133">If the value in  _hfrmreg_ is HFRMREG_FOLDER, the interface identifier used in  _lpunk_ must be non- **null** and must allow [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) method calls to an [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> 
  
<span data-ttu-id="a1cda-134">Um den Container lokale Formular zu öffnen, müssen Sie einen Anruf an **OpenFormContainer** -Methode oder die [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) -Funktion verwenden. Sie können nicht die [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) -Methode verwenden, um die Benutzer auswählen den Container lokale Formular aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a1cda-134">To open the local form container, you must use a call to **OpenFormContainer** method or the [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) function; you cannot use the [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) method to enable the user to select the local form container.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a1cda-135">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="a1cda-135">MFCMAPI reference</span></span>

<span data-ttu-id="a1cda-136">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a1cda-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a1cda-137">**Datei**</span><span class="sxs-lookup"><span data-stu-id="a1cda-137">**File**</span></span>|<span data-ttu-id="a1cda-138">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="a1cda-138">**Function**</span></span>|<span data-ttu-id="a1cda-139">**Kommentar**</span><span class="sxs-lookup"><span data-stu-id="a1cda-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a1cda-140">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="a1cda-140">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="a1cda-141">CMainDlg::OnOpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="a1cda-141">CMainDlg::OnOpenFormContainer</span></span>  <br/> |<span data-ttu-id="a1cda-142">MFCMAPI (engl.) verwendet die **IMAPIFormMgr::OpenFormContainer** -Methode, um ein Formular Container abrufen, damit der Inhalt des Containers gerendert werden können.</span><span class="sxs-lookup"><span data-stu-id="a1cda-142">MFCMAPI uses the **IMAPIFormMgr::OpenFormContainer** method to retrieve a form container so the container's contents can be rendered.</span></span>  <br/> |
|<span data-ttu-id="a1cda-143">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="a1cda-143">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="a1cda-144">CMsgStoreDlg::OnOpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="a1cda-144">CMsgStoreDlg::OnOpenFormContainer</span></span>  <br/> |<span data-ttu-id="a1cda-145">MFCMAPI (engl.) wird die **IMAPIFormMgr::OpenFormContainer** -Methode verwendet, um ein Formular Container für einen Ordner abzurufen, damit der Inhalt des Containers gerendert werden können.</span><span class="sxs-lookup"><span data-stu-id="a1cda-145">MFCMAPI uses the **IMAPIFormMgr::OpenFormContainer** method to retrieve a form container for a folder so the container's contents can be rendered.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a1cda-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1cda-146">See also</span></span>



[<span data-ttu-id="a1cda-147">IMAPIFormContainer::InstallForm</span><span class="sxs-lookup"><span data-stu-id="a1cda-147">IMAPIFormContainer::InstallForm</span></span>](imapiformcontainer-installform.md)
  
[<span data-ttu-id="a1cda-148">IMAPIFormMgr::SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="a1cda-148">IMAPIFormMgr::SelectFormContainer</span></span>](imapiformmgr-selectformcontainer.md)
  
[<span data-ttu-id="a1cda-149">MAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="a1cda-149">MAPIOpenLocalFormContainer</span></span>](mapiopenlocalformcontainer.md)
  
[<span data-ttu-id="a1cda-150">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a1cda-150">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="a1cda-151">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="a1cda-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

