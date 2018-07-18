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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ef9b99f06b62fd361bb780debb527ec2d7457589
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792214"
---
# <a name="imapiformmgrselectformcontainer"></a><span data-ttu-id="30f03-103">IMAPIFormMgr::SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="30f03-103">IMAPIFormMgr::SelectFormContainer</span></span>

  
  
<span data-ttu-id="30f03-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="30f03-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="30f03-105">Zeigt ein Dialogfeld an, die ermöglicht dem Benutzer das Formular Container auswählen, und gibt eine Schnittstelle für das Containerobjekt der ausgewählten Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="30f03-105">Presents a dialog box that enables the user to select a form container, and returns an interface for the container object the user selected.</span></span>
  
```cpp
HRESULT SelectFormContainer(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="30f03-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="30f03-106">Parameters</span></span>

 <span data-ttu-id="30f03-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="30f03-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="30f03-108">[in] Ein Handle für das übergeordnete Fenster im angezeigten Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="30f03-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="30f03-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="30f03-109">_ulFlags_</span></span>
  
> <span data-ttu-id="30f03-110">[in] Eine Bitmaske aus Flags, die steuert, wie die Formularbibliothek aktiviert ist (d. h., wie der Formular Container ausgewählt ist).</span><span class="sxs-lookup"><span data-stu-id="30f03-110">[in] A bitmask of flags that controls how the form library is selected (that is, how the form container is selected).</span></span> <span data-ttu-id="30f03-111">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="30f03-111">The following flags can be set:</span></span>
    
<span data-ttu-id="30f03-112">MAPIFORM_SELECT_ALL_REGISTRIES</span><span class="sxs-lookup"><span data-stu-id="30f03-112">MAPIFORM_SELECT_ALL_REGISTRIES</span></span> 
  
> <span data-ttu-id="30f03-113">Auswahl kann von allen Containern vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="30f03-113">Selection can be made from all containers.</span></span> <span data-ttu-id="30f03-114">Dies ist der Standard-Auswahltyp.</span><span class="sxs-lookup"><span data-stu-id="30f03-114">This is the default selection type.</span></span> 
    
<span data-ttu-id="30f03-115">MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY</span><span class="sxs-lookup"><span data-stu-id="30f03-115">MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY</span></span> 
  
> <span data-ttu-id="30f03-116">Auswahl kann nur von Ordner Containern vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="30f03-116">Selection can be made only from folder containers.</span></span>
    
<span data-ttu-id="30f03-117">MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY</span><span class="sxs-lookup"><span data-stu-id="30f03-117">MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY</span></span> 
  
> <span data-ttu-id="30f03-118">Auswahl kann nur aus den Containern vorgenommen werden, die keine Ordner zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="30f03-118">Selection can be made only from containers that are not associated with folders.</span></span>
    
 <span data-ttu-id="30f03-119">_lppfcnt_</span><span class="sxs-lookup"><span data-stu-id="30f03-119">_lppfcnt_</span></span>
  
> <span data-ttu-id="30f03-120">[out] Ein Zeiger auf einen Zeiger auf die zurückgegebene Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="30f03-120">[out] A pointer to a pointer to the returned interface.</span></span> <span data-ttu-id="30f03-121">Diese Schnittstelle ist für das Containerobjekt, das vom Benutzer ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="30f03-121">This interface is for the container object that is selected by the user.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="30f03-122">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="30f03-122">Return value</span></span>

<span data-ttu-id="30f03-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="30f03-123">S_OK</span></span> 
  
> <span data-ttu-id="30f03-124">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="30f03-124">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="30f03-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="30f03-125">Remarks</span></span>

<span data-ttu-id="30f03-126">Formular Viewer aufrufen in der Regel die **IMAPIFormMgr::SelectFormContainer** -Methode, um ein Formular Container auszuwählen, in dem einem Formular installiert ist.</span><span class="sxs-lookup"><span data-stu-id="30f03-126">Form viewers typically call the **IMAPIFormMgr::SelectFormContainer** method to select a form container into which a form is installed.</span></span> <span data-ttu-id="30f03-127">**SelectFormContainer** kann nicht aus dem Container lokale Formular mit dem Wert HFRMREG_LOCAL verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="30f03-127">**SelectFormContainer** cannot be used to select the local form container, which has the value HFRMREG_LOCAL.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="30f03-128">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="30f03-128">MFCMAPI reference</span></span>

<span data-ttu-id="30f03-129">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="30f03-129">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="30f03-130">**Datei**</span><span class="sxs-lookup"><span data-stu-id="30f03-130">**File**</span></span>|<span data-ttu-id="30f03-131">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="30f03-131">**Function**</span></span>|<span data-ttu-id="30f03-132">**Comment**</span><span class="sxs-lookup"><span data-stu-id="30f03-132">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="30f03-133">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="30f03-133">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="30f03-134">CMainDlg::OnSelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="30f03-134">CMainDlg::OnSelectFormContainer</span></span>  <br/> |<span data-ttu-id="30f03-135">MFCMAPI (engl.) verwendet die **IMAPIFormMgr::SelectFormContainer** -Methode, um ein Formular Container wählen Sie vor dem Rendern seinen Inhalt.</span><span class="sxs-lookup"><span data-stu-id="30f03-135">MFCMAPI uses the **IMAPIFormMgr::SelectFormContainer** method to select a form container before rendering its contents.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="30f03-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30f03-136">See also</span></span>



[<span data-ttu-id="30f03-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="30f03-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="30f03-138">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="30f03-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

