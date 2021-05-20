---
title: IMAPIFormMgrSelectFormContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CopyMessages
api_type:
- COM
ms.assetid: c33daad6-52c4-4968-ac56-415178c9bf12
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: bfddc24e6a9c7cf8bdeae1e5ea730ecdb116f564
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428592"
---
# <a name="imapiformmgrselectformcontainer"></a><span data-ttu-id="0c264-103">IMAPIFormMgr::SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="0c264-103">IMAPIFormMgr::SelectFormContainer</span></span>

  
  
<span data-ttu-id="0c264-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c264-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c264-105">Zeigt ein Dialogfeld an, in dem der Benutzer einen Formularcontainer auswählen kann, und gibt eine Schnittstelle für das vom Benutzer ausgewählte Containerobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="0c264-105">Presents a dialog box that enables the user to select a form container, and returns an interface for the container object the user selected.</span></span>
  
```cpp
HRESULT SelectFormContainer(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="0c264-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c264-106">Parameters</span></span>

 <span data-ttu-id="0c264-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="0c264-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="0c264-108">[in] Ein Handle zum übergeordneten Fenster des angezeigten Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="0c264-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="0c264-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0c264-109">_ulFlags_</span></span>
  
> <span data-ttu-id="0c264-110">[in] Eine Bitmaske mit Flags, die steuert, wie die Formularbibliothek ausgewählt wird (d. h. wie der Formularcontainer ausgewählt wird).</span><span class="sxs-lookup"><span data-stu-id="0c264-110">[in] A bitmask of flags that controls how the form library is selected (that is, how the form container is selected).</span></span> <span data-ttu-id="0c264-111">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="0c264-111">The following flags can be set:</span></span>
    
<span data-ttu-id="0c264-112">MAPIFORM_SELECT_ALL_REGISTRIES</span><span class="sxs-lookup"><span data-stu-id="0c264-112">MAPIFORM_SELECT_ALL_REGISTRIES</span></span> 
  
> <span data-ttu-id="0c264-113">Die Auswahl kann aus allen Containern vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="0c264-113">Selection can be made from all containers.</span></span> <span data-ttu-id="0c264-114">Dies ist der Standardauswahltyp.</span><span class="sxs-lookup"><span data-stu-id="0c264-114">This is the default selection type.</span></span> 
    
<span data-ttu-id="0c264-115">MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY</span><span class="sxs-lookup"><span data-stu-id="0c264-115">MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY</span></span> 
  
> <span data-ttu-id="0c264-116">Die Auswahl kann nur in Ordnercontainern vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="0c264-116">Selection can be made only from folder containers.</span></span>
    
<span data-ttu-id="0c264-117">MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY</span><span class="sxs-lookup"><span data-stu-id="0c264-117">MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY</span></span> 
  
> <span data-ttu-id="0c264-118">Die Auswahl kann nur aus Containern vorgenommen werden, die ordnern nicht zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0c264-118">Selection can be made only from containers that are not associated with folders.</span></span>
    
 <span data-ttu-id="0c264-119">_lppfcnt_</span><span class="sxs-lookup"><span data-stu-id="0c264-119">_lppfcnt_</span></span>
  
> <span data-ttu-id="0c264-120">[out] Ein Zeiger auf einen Zeiger auf die zurückgegebene Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0c264-120">[out] A pointer to a pointer to the returned interface.</span></span> <span data-ttu-id="0c264-121">Diese Schnittstelle ist für das Containerobjekt, das vom Benutzer ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="0c264-121">This interface is for the container object that is selected by the user.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0c264-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0c264-122">Return value</span></span>

<span data-ttu-id="0c264-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="0c264-123">S_OK</span></span> 
  
> <span data-ttu-id="0c264-124">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="0c264-124">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0c264-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0c264-125">Remarks</span></span>

<span data-ttu-id="0c264-126">Formularanzeigen rufen in der Regel die **IMAPIFormMgr::SelectFormContainer-Methode** auf, um einen Formularcontainer auszuwählen, in dem ein Formular installiert ist.</span><span class="sxs-lookup"><span data-stu-id="0c264-126">Form viewers typically call the **IMAPIFormMgr::SelectFormContainer** method to select a form container into which a form is installed.</span></span> <span data-ttu-id="0c264-127">**SelectFormContainer** kann nicht zum Auswählen des lokalen Formularcontainers verwendet werden, der den Wert HFRMREG_LOCAL.</span><span class="sxs-lookup"><span data-stu-id="0c264-127">**SelectFormContainer** cannot be used to select the local form container, which has the value HFRMREG_LOCAL.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0c264-128">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="0c264-128">MFCMAPI reference</span></span>

<span data-ttu-id="0c264-129">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="0c264-129">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0c264-130">**Datei**</span><span class="sxs-lookup"><span data-stu-id="0c264-130">**File**</span></span>|<span data-ttu-id="0c264-131">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="0c264-131">**Function**</span></span>|<span data-ttu-id="0c264-132">**Comment**</span><span class="sxs-lookup"><span data-stu-id="0c264-132">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0c264-133">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="0c264-133">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="0c264-134">CMainDlg::OnSelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="0c264-134">CMainDlg::OnSelectFormContainer</span></span>  <br/> |<span data-ttu-id="0c264-135">MFCMAPI verwendet die **IMAPIFormMgr::SelectFormContainer-Methode,** um einen Formularcontainer auszuwählen, bevor der Inhalt gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="0c264-135">MFCMAPI uses the **IMAPIFormMgr::SelectFormContainer** method to select a form container before rendering its contents.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0c264-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c264-136">See also</span></span>



[<span data-ttu-id="0c264-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0c264-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="0c264-138">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="0c264-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

