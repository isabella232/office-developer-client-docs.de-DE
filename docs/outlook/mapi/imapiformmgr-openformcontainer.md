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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321637"
---
# <a name="imapiformmgropenformcontainer"></a><span data-ttu-id="f2194-103">IMAPIFormMgr::OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="f2194-103">IMAPIFormMgr::OpenFormContainer</span></span>

  
  
<span data-ttu-id="f2194-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f2194-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f2194-105">Öffnet eine [IMAPIFormContainer-Schnittstelle](imapiformcontaineriunknown.md) für einen bestimmten Formularcontainer.</span><span class="sxs-lookup"><span data-stu-id="f2194-105">Opens an [IMAPIFormContainer](imapiformcontaineriunknown.md) interface for a specific form container.</span></span> 
  
```cpp
HRESULT OpenFormContainer(
  HFRMREG hfrmreg,
  LPUNKNOWN lpunk,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="f2194-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2194-106">Parameters</span></span>

 <span data-ttu-id="f2194-107">_hfrmreg_</span><span class="sxs-lookup"><span data-stu-id="f2194-107">_hfrmreg_</span></span>
  
> <span data-ttu-id="f2194-108">[in] Eine HFRMREG-Aufzählung, die die zu öffnende Formularbibliothek angibt (d. h. den zu öffnenden Formularcontainer).</span><span class="sxs-lookup"><span data-stu-id="f2194-108">[in] An HFRMREG enumeration that indicates the form library to open (that is, the form container to open).</span></span> <span data-ttu-id="f2194-109">Eine HFRMREG-Enumeration ist eine Enumeration, die für einen Formularbibliotheksanbieter spezifisch ist.</span><span class="sxs-lookup"><span data-stu-id="f2194-109">An HFRMREG enumeration is an enumeration that is specific to a form library provider.</span></span> <span data-ttu-id="f2194-110">Mögliche HFRMREG-Werte sind:</span><span class="sxs-lookup"><span data-stu-id="f2194-110">Possible HFRMREG values include the following:</span></span>
    
<span data-ttu-id="f2194-111">HFRMREG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="f2194-111">HFRMREG_DEFAULT</span></span> 
  
> <span data-ttu-id="f2194-112">Ein praktischer Formularcontainer.</span><span class="sxs-lookup"><span data-stu-id="f2194-112">A convenient form container.</span></span>
    
<span data-ttu-id="f2194-113">HFRMREG_FOLDER</span><span class="sxs-lookup"><span data-stu-id="f2194-113">HFRMREG_FOLDER</span></span> 
  
> <span data-ttu-id="f2194-114">Ein Ordnercontainer.</span><span class="sxs-lookup"><span data-stu-id="f2194-114">A folder container.</span></span> 
    
<span data-ttu-id="f2194-115">HFRMREG_PERSONAL</span><span class="sxs-lookup"><span data-stu-id="f2194-115">HFRMREG_PERSONAL</span></span> 
  
> <span data-ttu-id="f2194-116">Der Container für den Standardnachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="f2194-116">The container for the default message store.</span></span> 
    
<span data-ttu-id="f2194-117">HFRMREG_LOCAL</span><span class="sxs-lookup"><span data-stu-id="f2194-117">HFRMREG_LOCAL</span></span> 
  
> <span data-ttu-id="f2194-118">Ein lokaler Formularcontainer.</span><span class="sxs-lookup"><span data-stu-id="f2194-118">A local form container.</span></span> 
    
 <span data-ttu-id="f2194-119">_lpunk_</span><span class="sxs-lookup"><span data-stu-id="f2194-119">_lpunk_</span></span>
  
> <span data-ttu-id="f2194-120">[in] Ein Zeiger auf das Objekt, für das die Schnittstelle geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="f2194-120">[in] A pointer to the object for which the interface is opened.</span></span> <span data-ttu-id="f2194-121">Der  _lpunk-Parameter_ muss **null sein,** es sei denn, der Wert für den  _parameter hfrmreg_ erfordert einen Objektzeiger.</span><span class="sxs-lookup"><span data-stu-id="f2194-121">The  _lpunk_ parameter must be **null** unless the value for the  _hfrmreg_ parameter requires an object pointer.</span></span> 
    
 <span data-ttu-id="f2194-122">_lppfcnt_</span><span class="sxs-lookup"><span data-stu-id="f2194-122">_lppfcnt_</span></span>
  
> <span data-ttu-id="f2194-123">[out] Ein Zeiger auf einen Zeiger auf das zurückgegebene Formularcontainerobjekt.</span><span class="sxs-lookup"><span data-stu-id="f2194-123">[out] A pointer to a pointer to the returned form container object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f2194-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f2194-124">Return value</span></span>

<span data-ttu-id="f2194-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="f2194-125">S_OK</span></span> 
  
> <span data-ttu-id="f2194-126">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="f2194-126">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="f2194-127">MAPI_E_NO_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="f2194-127">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="f2194-128">Das von  _lpunk_ angezeigte Objekt unterstützt die erforderliche Schnittstelle nicht.</span><span class="sxs-lookup"><span data-stu-id="f2194-128">The object pointed to by  _lpunk_ does not support the required interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f2194-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f2194-129">Remarks</span></span>

<span data-ttu-id="f2194-130">Formularbetrachter rufen die **IMAPIFormMgr::OpenFormContainer-Methode** auf, um eine **IMAPIFormContainer-Schnittstelle** für einen bestimmten Formularcontainer zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f2194-130">Form viewers call the **IMAPIFormMgr::OpenFormContainer** method to open an **IMAPIFormContainer** interface for a specific form container.</span></span> <span data-ttu-id="f2194-131">Diese Schnittstelle kann dann zum Installieren von Formularen in einem Formularcontainer und zum Entfernen von Formularen aus einem Formularcontainer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f2194-131">This interface can then be used for installing forms into and removing forms from a form container.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f2194-132">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="f2194-132">Notes to callers</span></span>

<span data-ttu-id="f2194-133">Wenn der Wert in _hfrmreg_ HFRMREG_FOLDER ist, muss der in _lpunk_ verwendete Schnittstellenbezeichner nicht null sein und [IUnknown::QueryInterface-Methodenaufrufe](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) an eine  [IMAPIFolder-Schnittstelle](imapifolderimapicontainer.md) zulassen.</span><span class="sxs-lookup"><span data-stu-id="f2194-133">If the value in  _hfrmreg_ is HFRMREG_FOLDER, the interface identifier used in  _lpunk_ must be non- **null** and must allow [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) method calls to an [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> 
  
<span data-ttu-id="f2194-134">Zum Öffnen des lokalen Formularcontainers müssen Sie einen Aufruf der **OpenFormContainer-Methode** oder der [MAPIOpenLocalFormContainer-Funktion](mapiopenlocalformcontainer.md) verwenden. Sie können die [IMAPIFormMgr::SelectFormContainer-Methode](imapiformmgr-selectformcontainer.md) nicht verwenden, um dem Benutzer die Auswahl des lokalen Formularcontainers zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="f2194-134">To open the local form container, you must use a call to **OpenFormContainer** method or the [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) function; you cannot use the [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) method to enable the user to select the local form container.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f2194-135">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="f2194-135">MFCMAPI reference</span></span>

<span data-ttu-id="f2194-136">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="f2194-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f2194-137">**Datei**</span><span class="sxs-lookup"><span data-stu-id="f2194-137">**File**</span></span>|<span data-ttu-id="f2194-138">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="f2194-138">**Function**</span></span>|<span data-ttu-id="f2194-139">**Comment**</span><span class="sxs-lookup"><span data-stu-id="f2194-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f2194-140">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="f2194-140">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="f2194-141">CMainDlg::OnOpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="f2194-141">CMainDlg::OnOpenFormContainer</span></span>  <br/> |<span data-ttu-id="f2194-142">MFCMAPI verwendet die **IMAPIFormMgr::OpenFormContainer-Methode,** um einen Formularcontainer abzurufen, damit der Inhalt des Containers gerendert werden kann.</span><span class="sxs-lookup"><span data-stu-id="f2194-142">MFCMAPI uses the **IMAPIFormMgr::OpenFormContainer** method to retrieve a form container so the container's contents can be rendered.</span></span>  <br/> |
|<span data-ttu-id="f2194-143">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="f2194-143">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="f2194-144">CMsgStoreDlg::OnOpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="f2194-144">CMsgStoreDlg::OnOpenFormContainer</span></span>  <br/> |<span data-ttu-id="f2194-145">MFCMAPI verwendet die **IMAPIFormMgr::OpenFormContainer-Methode,** um einen Formularcontainer für einen Ordner abzurufen, damit der Inhalt des Containers gerendert werden kann.</span><span class="sxs-lookup"><span data-stu-id="f2194-145">MFCMAPI uses the **IMAPIFormMgr::OpenFormContainer** method to retrieve a form container for a folder so the container's contents can be rendered.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f2194-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2194-146">See also</span></span>



[<span data-ttu-id="f2194-147">IMAPIFormContainer::InstallForm</span><span class="sxs-lookup"><span data-stu-id="f2194-147">IMAPIFormContainer::InstallForm</span></span>](imapiformcontainer-installform.md)
  
[<span data-ttu-id="f2194-148">IMAPIFormMgr::SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="f2194-148">IMAPIFormMgr::SelectFormContainer</span></span>](imapiformmgr-selectformcontainer.md)
  
[<span data-ttu-id="f2194-149">MAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="f2194-149">MAPIOpenLocalFormContainer</span></span>](mapiopenlocalformcontainer.md)
  
[<span data-ttu-id="f2194-150">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f2194-150">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="f2194-151">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="f2194-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

