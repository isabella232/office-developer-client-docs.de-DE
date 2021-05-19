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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416650"
---
# <a name="imapiformmgrprepareform"></a><span data-ttu-id="4fa7f-103">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="4fa7f-103">IMAPIFormMgr::PrepareForm</span></span>

  
  
<span data-ttu-id="4fa7f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4fa7f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4fa7f-105">Lädt ein Formular zum Öffnen herunter.</span><span class="sxs-lookup"><span data-stu-id="4fa7f-105">Downloads a form for opening.</span></span>
  
```cpp
HRESULT PrepareForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMINFO pfrmiInfo
);
```

## <a name="parameters"></a><span data-ttu-id="4fa7f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4fa7f-106">Parameters</span></span>

 <span data-ttu-id="4fa7f-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="4fa7f-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="4fa7f-108">[in] Ein Handle zum übergeordneten Fenster der Statusanzeige, das beim Herunterladen des Formulars angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4fa7f-108">[in] A handle to the parent window of the progress indicator that is displayed while the form is downloaded.</span></span> <span data-ttu-id="4fa7f-109">Der  _ulUIParam-Parameter_ wird ignoriert, es sei denn, das MAPI_DIALOG wird im  _ulFlags-Parameter_ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4fa7f-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="4fa7f-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4fa7f-110">_ulFlags_</span></span>
  
> <span data-ttu-id="4fa7f-111">[in] Eine Bitmaske mit Flags, die steuert, wie das Formular heruntergeladen wird.</span><span class="sxs-lookup"><span data-stu-id="4fa7f-111">[in] A bitmask of flags that controls how the form is downloaded.</span></span> <span data-ttu-id="4fa7f-112">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="4fa7f-112">The following flag can be set:</span></span>
    
<span data-ttu-id="4fa7f-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="4fa7f-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="4fa7f-114">Zeigt eine Benutzeroberfläche an, um den Status zur Verfügung zu stellen, oder fordert den Benutzer auf, weitere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4fa7f-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="4fa7f-115">Wenn dieses Kennzeichen nicht festgelegt ist, wird keine Benutzeroberfläche angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4fa7f-115">If this flag is not set, no user interface is displayed.</span></span>
    
 <span data-ttu-id="4fa7f-116">_pfrmiInfo_</span><span class="sxs-lookup"><span data-stu-id="4fa7f-116">_pfrmiInfo_</span></span>
  
> <span data-ttu-id="4fa7f-117">[in] Ein Zeiger auf ein Formularinformationsobjekt für das zu herunterladende Formular.</span><span class="sxs-lookup"><span data-stu-id="4fa7f-117">[in] A pointer to a form information object for the form to be downloaded.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4fa7f-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4fa7f-118">Return value</span></span>

<span data-ttu-id="4fa7f-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="4fa7f-119">S_OK</span></span> 
  
> <span data-ttu-id="4fa7f-120">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="4fa7f-120">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4fa7f-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4fa7f-121">Remarks</span></span>

<span data-ttu-id="4fa7f-122">Formularbetrachter rufen die **IMAPIFormMgr::P repareForm-Methode** auf, um ein Formular aus einem Formularcontainer zum Öffnen herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="4fa7f-122">Form viewers call the **IMAPIFormMgr::PrepareForm** method to download a form from a form container for opening.</span></span> <span data-ttu-id="4fa7f-123">Die meisten Formularbetrachter müssen **PrepareForm** nicht aufrufen, da die [Methoden IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) und [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) bei Bedarf **PrepareForm** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4fa7f-123">Most form viewers do not need to call **PrepareForm**, because both the [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) and [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) methods call **PrepareForm**, if necessary.</span></span> 
  
<span data-ttu-id="4fa7f-124">Sie können **PrepareForm verwenden,** um die Dynamic Link Libraries (DLLs) und andere Dateien zu erhalten, die einem Formular zugeordnet sind, um sie zu ändern.</span><span class="sxs-lookup"><span data-stu-id="4fa7f-124">You can use **PrepareForm** to obtain the dynamic-link libraries (DLLs) and other files associated with a form to modify them.</span></span> <span data-ttu-id="4fa7f-125">Wenn das geänderte Formular wieder in den Formularcontainer geladen wird, muss es erneut installiert werden.</span><span class="sxs-lookup"><span data-stu-id="4fa7f-125">If the modified form is loaded back into its form container, it must be reinstalled.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4fa7f-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4fa7f-126">See also</span></span>



[<span data-ttu-id="4fa7f-127">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="4fa7f-127">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="4fa7f-128">IMAPIFormMgr::LoadForm</span><span class="sxs-lookup"><span data-stu-id="4fa7f-128">IMAPIFormMgr::LoadForm</span></span>](imapiformmgr-loadform.md)
  
[<span data-ttu-id="4fa7f-129">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4fa7f-129">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

