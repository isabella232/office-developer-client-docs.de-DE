---
title: IMAPIFormMgrPrepareForm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.PrepareForm
api_type:
- COM
ms.assetid: 8f8ee2cb-1c2a-4958-b01e-2f4aab689f89
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d0d5d8fe13a3c192dc0b0a8ddc0f5f945fa16f15
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321812"
---
# <a name="imapiformmgrprepareform"></a><span data-ttu-id="f4480-103">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="f4480-103">IMAPIFormMgr::PrepareForm</span></span>

  
  
<span data-ttu-id="f4480-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4480-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4480-105">Lädt ein Formular zum Öffnen herunter.</span><span class="sxs-lookup"><span data-stu-id="f4480-105">Downloads a form for opening.</span></span>
  
```cpp
HRESULT PrepareForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMINFO pfrmiInfo
);
```

## <a name="parameters"></a><span data-ttu-id="f4480-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4480-106">Parameters</span></span>

 <span data-ttu-id="f4480-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="f4480-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="f4480-108">in Ein Handle für das übergeordnete Fenster der Statusanzeige, das angezeigt wird, während das Formular heruntergeladen wird.</span><span class="sxs-lookup"><span data-stu-id="f4480-108">[in] A handle to the parent window of the progress indicator that is displayed while the form is downloaded.</span></span> <span data-ttu-id="f4480-109">Der _ulUIParam_ -Parameter wird ignoriert, es sei denn, das MAPI_DIALOG-Flag wird im _ulFlags_ -Parameter festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f4480-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="f4480-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f4480-110">_ulFlags_</span></span>
  
> <span data-ttu-id="f4480-111">in Eine Bitmaske von Flags, die das Herunterladen des Formulars steuert.</span><span class="sxs-lookup"><span data-stu-id="f4480-111">[in] A bitmask of flags that controls how the form is downloaded.</span></span> <span data-ttu-id="f4480-112">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="f4480-112">The following flag can be set:</span></span>
    
<span data-ttu-id="f4480-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="f4480-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="f4480-114">Zeigt eine Benutzeroberfläche an, um den Status anzugeben oder den Benutzer aufzufordern, weitere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f4480-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="f4480-115">Wenn dieses Flag nicht festgelegt ist, wird keine Benutzeroberfläche angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f4480-115">If this flag is not set, no user interface is displayed.</span></span>
    
 <span data-ttu-id="f4480-116">_pfrmiInfo_</span><span class="sxs-lookup"><span data-stu-id="f4480-116">_pfrmiInfo_</span></span>
  
> <span data-ttu-id="f4480-117">in Ein Zeiger auf ein Formular Informationsobjekt für das Formular heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="f4480-117">[in] A pointer to a form information object for the form to be downloaded.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f4480-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f4480-118">Return value</span></span>

<span data-ttu-id="f4480-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="f4480-119">S_OK</span></span> 
  
> <span data-ttu-id="f4480-120">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="f4480-120">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f4480-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4480-121">Remarks</span></span>

<span data-ttu-id="f4480-122">Formular Betrachter rufen die **IMAPIFormMgr::P repareform** -Methode auf, um ein Formular aus einem Formular Container zum Öffnen herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="f4480-122">Form viewers call the **IMAPIFormMgr::PrepareForm** method to download a form from a form container for opening.</span></span> <span data-ttu-id="f4480-123">Die meisten Formular Betrachter müssen **PrepareForm**nicht aufrufen, da die Methoden [IMAPIFormMgr:: CreateForm](imapiformmgr-createform.md) und [IMAPIFormMgr:: LoadForm](imapiformmgr-loadform.md) **PrepareForm**bei Bedarf aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f4480-123">Most form viewers do not need to call **PrepareForm**, because both the [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) and [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) methods call **PrepareForm**, if necessary.</span></span> 
  
<span data-ttu-id="f4480-124">Sie können **PrepareForm** verwenden, um die DLLs (Dynamic Link Libraries) und andere Dateien abzurufen, die einem Formular zugeordnet sind, um Sie zu ändern.</span><span class="sxs-lookup"><span data-stu-id="f4480-124">You can use **PrepareForm** to obtain the dynamic-link libraries (DLLs) and other files associated with a form to modify them.</span></span> <span data-ttu-id="f4480-125">Wenn das geänderte Formular wieder in seinen Formular Container geladen wird, muss es erneut installiert werden.</span><span class="sxs-lookup"><span data-stu-id="f4480-125">If the modified form is loaded back into its form container, it must be reinstalled.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f4480-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4480-126">See also</span></span>



[<span data-ttu-id="f4480-127">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="f4480-127">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="f4480-128">IMAPIFormMgr::LoadForm</span><span class="sxs-lookup"><span data-stu-id="f4480-128">IMAPIFormMgr::LoadForm</span></span>](imapiformmgr-loadform.md)
  
[<span data-ttu-id="f4480-129">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f4480-129">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

