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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 68a358c91e35c5a075e220794c78f4e5c96e43ee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321637"
---
# <a name="imapiformmgropenformcontainer"></a><span data-ttu-id="fb120-103">IMAPIFormMgr::OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="fb120-103">IMAPIFormMgr::OpenFormContainer</span></span>

  
  
<span data-ttu-id="fb120-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fb120-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fb120-105">Öffnet eine [IMAPIFormContainer](imapiformcontaineriunknown.md) -Schnittstelle für einen bestimmten Formular Container.</span><span class="sxs-lookup"><span data-stu-id="fb120-105">Opens an [IMAPIFormContainer](imapiformcontaineriunknown.md) interface for a specific form container.</span></span> 
  
```cpp
HRESULT OpenFormContainer(
  HFRMREG hfrmreg,
  LPUNKNOWN lpunk,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="fb120-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb120-106">Parameters</span></span>

 <span data-ttu-id="fb120-107">_hfrmreg_</span><span class="sxs-lookup"><span data-stu-id="fb120-107">_hfrmreg_</span></span>
  
> <span data-ttu-id="fb120-108">in Eine HFRMREG-Aufzählung, die die zu öffnende Formularbibliothek angibt (also den zu öffnenden Formular Container).</span><span class="sxs-lookup"><span data-stu-id="fb120-108">[in] An HFRMREG enumeration that indicates the form library to open (that is, the form container to open).</span></span> <span data-ttu-id="fb120-109">Eine HFRMREG-Aufzählung ist eine für einen Formular Bibliotheks anbieterspezifische Enumeration.</span><span class="sxs-lookup"><span data-stu-id="fb120-109">An HFRMREG enumeration is an enumeration that is specific to a form library provider.</span></span> <span data-ttu-id="fb120-110">Zu den möglichen HFRMREG-Werten gehört Folgendes:</span><span class="sxs-lookup"><span data-stu-id="fb120-110">Possible HFRMREG values include the following:</span></span>
    
<span data-ttu-id="fb120-111">HFRMREG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="fb120-111">HFRMREG_DEFAULT</span></span> 
  
> <span data-ttu-id="fb120-112">Ein bequemer Formular Container.</span><span class="sxs-lookup"><span data-stu-id="fb120-112">A convenient form container.</span></span>
    
<span data-ttu-id="fb120-113">HFRMREG_FOLDER</span><span class="sxs-lookup"><span data-stu-id="fb120-113">HFRMREG_FOLDER</span></span> 
  
> <span data-ttu-id="fb120-114">Ein Ordner Container.</span><span class="sxs-lookup"><span data-stu-id="fb120-114">A folder container.</span></span> 
    
<span data-ttu-id="fb120-115">HFRMREG_PERSONAL</span><span class="sxs-lookup"><span data-stu-id="fb120-115">HFRMREG_PERSONAL</span></span> 
  
> <span data-ttu-id="fb120-116">Der Container für den Standardnachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="fb120-116">The container for the default message store.</span></span> 
    
<span data-ttu-id="fb120-117">HFRMREG_LOCAL</span><span class="sxs-lookup"><span data-stu-id="fb120-117">HFRMREG_LOCAL</span></span> 
  
> <span data-ttu-id="fb120-118">Ein lokaler Formular Container.</span><span class="sxs-lookup"><span data-stu-id="fb120-118">A local form container.</span></span> 
    
 <span data-ttu-id="fb120-119">_lpUnk_</span><span class="sxs-lookup"><span data-stu-id="fb120-119">_lpunk_</span></span>
  
> <span data-ttu-id="fb120-120">in Ein Zeiger auf das Objekt, für das die Schnittstelle geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="fb120-120">[in] A pointer to the object for which the interface is opened.</span></span> <span data-ttu-id="fb120-121">Der _lpUnk_ -Parameter muss **null** sein, es sei denn, der Wert für den _hfrmreg_ -Parameter erfordert einen Objektzeiger.</span><span class="sxs-lookup"><span data-stu-id="fb120-121">The  _lpunk_ parameter must be **null** unless the value for the  _hfrmreg_ parameter requires an object pointer.</span></span> 
    
 <span data-ttu-id="fb120-122">_lppfcnt_</span><span class="sxs-lookup"><span data-stu-id="fb120-122">_lppfcnt_</span></span>
  
> <span data-ttu-id="fb120-123">Out Ein Zeiger auf einen Zeiger auf das zurückgegebene Formular Container-Objekt.</span><span class="sxs-lookup"><span data-stu-id="fb120-123">[out] A pointer to a pointer to the returned form container object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fb120-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fb120-124">Return value</span></span>

<span data-ttu-id="fb120-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="fb120-125">S_OK</span></span> 
  
> <span data-ttu-id="fb120-126">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="fb120-126">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="fb120-127">MAPI_E_NO_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="fb120-127">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="fb120-128">Das Objekt, auf das durch _lpUnk_ verwiesen wird, unterstützt die erforderliche Schnittstelle nicht.</span><span class="sxs-lookup"><span data-stu-id="fb120-128">The object pointed to by  _lpunk_ does not support the required interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="fb120-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb120-129">Remarks</span></span>

<span data-ttu-id="fb120-130">Formular Betrachter rufen die **IMAPIFormMgr:: OpenFormContainer** -Methode auf, um eine **IMAPIFormContainer** -Schnittstelle für einen bestimmten Formular Container zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="fb120-130">Form viewers call the **IMAPIFormMgr::OpenFormContainer** method to open an **IMAPIFormContainer** interface for a specific form container.</span></span> <span data-ttu-id="fb120-131">Diese Schnittstelle kann dann verwendet werden, um Formulare zu installieren und Formulare aus einem Formular Container zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="fb120-131">This interface can then be used for installing forms into and removing forms from a form container.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="fb120-132">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="fb120-132">Notes to callers</span></span>

<span data-ttu-id="fb120-133">Wenn der Wert in _HFRMREG_ HFRMREG_FOLDER ist, muss der in _lpUnk_ verwendete Schnittstellenbezeichner ungleich **null** sein und [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) -Methodenaufrufe an eine [IMAPIFolder](imapifolderimapicontainer.md) -Schnittstelle zulassen.</span><span class="sxs-lookup"><span data-stu-id="fb120-133">If the value in  _hfrmreg_ is HFRMREG_FOLDER, the interface identifier used in  _lpunk_ must be non- **null** and must allow [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) method calls to an [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> 
  
<span data-ttu-id="fb120-134">Zum Öffnen des lokalen Formular Containers müssen Sie einen Aufruf der **OpenFormContainer** -Methode oder der [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) -Funktion verwenden. Sie können die [IMAPIFormMgr:: SelectFormContainer](imapiformmgr-selectformcontainer.md) -Methode nicht verwenden, um dem Benutzer das Auswählen des lokalen Formular Containers zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="fb120-134">To open the local form container, you must use a call to **OpenFormContainer** method or the [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) function; you cannot use the [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) method to enable the user to select the local form container.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="fb120-135">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="fb120-135">MFCMAPI reference</span></span>

<span data-ttu-id="fb120-136">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="fb120-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="fb120-137">**Datei**</span><span class="sxs-lookup"><span data-stu-id="fb120-137">**File**</span></span>|<span data-ttu-id="fb120-138">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="fb120-138">**Function**</span></span>|<span data-ttu-id="fb120-139">**Comment**</span><span class="sxs-lookup"><span data-stu-id="fb120-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fb120-140">MainDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="fb120-140">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="fb120-141">CMainDlg:: OnOpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="fb120-141">CMainDlg::OnOpenFormContainer</span></span>  <br/> |<span data-ttu-id="fb120-142">MFCMAPI verwendet die **IMAPIFormMgr:: OpenFormContainer** -Methode, um einen Formular Container abzurufen, damit der Inhalt des Containers gerendert werden kann.</span><span class="sxs-lookup"><span data-stu-id="fb120-142">MFCMAPI uses the **IMAPIFormMgr::OpenFormContainer** method to retrieve a form container so the container's contents can be rendered.</span></span>  <br/> |
|<span data-ttu-id="fb120-143">MsgStoreDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="fb120-143">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="fb120-144">CMsgStoreDlg:: OnOpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="fb120-144">CMsgStoreDlg::OnOpenFormContainer</span></span>  <br/> |<span data-ttu-id="fb120-145">MFCMAPI verwendet die **IMAPIFormMgr:: OpenFormContainer** -Methode, um einen Formular Container für einen Ordner abzurufen, damit der Inhalt des Containers gerendert werden kann.</span><span class="sxs-lookup"><span data-stu-id="fb120-145">MFCMAPI uses the **IMAPIFormMgr::OpenFormContainer** method to retrieve a form container for a folder so the container's contents can be rendered.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fb120-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb120-146">See also</span></span>



[<span data-ttu-id="fb120-147">IMAPIFormContainer::InstallForm</span><span class="sxs-lookup"><span data-stu-id="fb120-147">IMAPIFormContainer::InstallForm</span></span>](imapiformcontainer-installform.md)
  
[<span data-ttu-id="fb120-148">IMAPIFormMgr::SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="fb120-148">IMAPIFormMgr::SelectFormContainer</span></span>](imapiformmgr-selectformcontainer.md)
  
[<span data-ttu-id="fb120-149">MAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="fb120-149">MAPIOpenLocalFormContainer</span></span>](mapiopenlocalformcontainer.md)
  
[<span data-ttu-id="fb120-150">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fb120-150">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="fb120-151">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="fb120-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

