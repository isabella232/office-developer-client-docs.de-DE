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
ms.openlocfilehash: 6e8ea7230ae86dee99cc4413715055fc53afa900
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579725"
---
# <a name="imapiformmgrprepareform"></a><span data-ttu-id="df698-103">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="df698-103">IMAPIFormMgr::PrepareForm</span></span>

  
  
<span data-ttu-id="df698-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df698-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df698-105">Downloads für ein Formular zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="df698-105">Downloads a form for opening.</span></span>
  
```cpp
HRESULT PrepareForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMINFO pfrmiInfo
);
```

## <a name="parameters"></a><span data-ttu-id="df698-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="df698-106">Parameters</span></span>

 <span data-ttu-id="df698-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="df698-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="df698-108">[in] Ein Handle für das übergeordnete Fenster der Statusanzeige, die angezeigt wird, während das Formular heruntergeladen wird.</span><span class="sxs-lookup"><span data-stu-id="df698-108">[in] A handle to the parent window of the progress indicator that is displayed while the form is downloaded.</span></span> <span data-ttu-id="df698-109">Der Parameter _UlUIParam_ wird ignoriert, es sei denn, das Flag MAPI_DIALOG im _UlFlags_ -Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="df698-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="df698-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="df698-110">_ulFlags_</span></span>
  
> <span data-ttu-id="df698-111">[in] Eine Bitmaske aus Flags, die steuert, wie das Formular heruntergeladen wird.</span><span class="sxs-lookup"><span data-stu-id="df698-111">[in] A bitmask of flags that controls how the form is downloaded.</span></span> <span data-ttu-id="df698-112">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="df698-112">The following flag can be set:</span></span>
    
<span data-ttu-id="df698-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="df698-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="df698-114">Zeigt eine Benutzeroberfläche zum Bereitstellen von Status oder auffordern, Weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="df698-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="df698-115">Wenn dieses Flag nicht festgelegt ist, wird keine Benutzeroberfläche angezeigt.</span><span class="sxs-lookup"><span data-stu-id="df698-115">If this flag is not set, no user interface is displayed.</span></span>
    
 <span data-ttu-id="df698-116">_pfrmiInfo_</span><span class="sxs-lookup"><span data-stu-id="df698-116">_pfrmiInfo_</span></span>
  
> <span data-ttu-id="df698-117">[in] Ein Zeiger auf ein Formular Informationen-Objekt für das Formular heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="df698-117">[in] A pointer to a form information object for the form to be downloaded.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="df698-118">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="df698-118">Return value</span></span>

<span data-ttu-id="df698-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="df698-119">S_OK</span></span> 
  
> <span data-ttu-id="df698-120">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="df698-120">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="df698-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="df698-121">Remarks</span></span>

<span data-ttu-id="df698-122">Formular Viewer rufen Sie die **IMAPIFormMgr::PrepareForm** -Methode, um ein Formular Container für das Öffnen ein Formulars heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="df698-122">Form viewers call the **IMAPIFormMgr::PrepareForm** method to download a form from a form container for opening.</span></span> <span data-ttu-id="df698-123">Die meisten Formular Viewer müssen nicht **PrepareForm**, aufrufen, da die [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) und die [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) Methoden **PrepareForm**, rufen Sie bei Bedarf.</span><span class="sxs-lookup"><span data-stu-id="df698-123">Most form viewers do not need to call **PrepareForm**, because both the [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) and [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) methods call **PrepareForm**, if necessary.</span></span> 
  
<span data-ttu-id="df698-124">Sie können **PrepareForm** verwenden, um die Dynamic Link Libraries (DLLs) und andere Dateien, die sie zum Ändern eines Formulars zugeordnet abzurufen.</span><span class="sxs-lookup"><span data-stu-id="df698-124">You can use **PrepareForm** to obtain the dynamic-link libraries (DLLs) and other files associated with a form to modify them.</span></span> <span data-ttu-id="df698-125">Wenn das geänderte Formular wieder in dessen Container Formular geladen wird, muss es neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="df698-125">If the modified form is loaded back into its form container, it must be reinstalled.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="df698-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df698-126">See also</span></span>



[<span data-ttu-id="df698-127">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="df698-127">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="df698-128">IMAPIFormMgr::LoadForm</span><span class="sxs-lookup"><span data-stu-id="df698-128">IMAPIFormMgr::LoadForm</span></span>](imapiformmgr-loadform.md)
  
[<span data-ttu-id="df698-129">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="df698-129">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

