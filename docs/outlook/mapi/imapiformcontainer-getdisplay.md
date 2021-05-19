---
title: IMAPIFormContainerGetDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.GetDisplay
api_type:
- COM
ms.assetid: 6829e273-4a75-4278-b58a-ae7543e075ac
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 994041d050df56fd3fa3c0e599542e05a202ad65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416132"
---
# <a name="imapiformcontainergetdisplay"></a><span data-ttu-id="84cae-103">IMAPIFormContainer::GetDisplay</span><span class="sxs-lookup"><span data-stu-id="84cae-103">IMAPIFormContainer::GetDisplay</span></span>

  
  
<span data-ttu-id="84cae-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84cae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84cae-105">Gibt den Anzeigenamen eines Formularcontainers zurück.</span><span class="sxs-lookup"><span data-stu-id="84cae-105">Returns the display name of a form container.</span></span>
  
```cpp
HRESULT GetDisplay(
  ULONG ulFlags,
  LPSTR FAR * pszDisplayName
);
```

## <a name="parameters"></a><span data-ttu-id="84cae-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="84cae-106">Parameters</span></span>

 <span data-ttu-id="84cae-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="84cae-107">_ulFlags_</span></span>
  
> <span data-ttu-id="84cae-108">[in] Eine Bitmaske mit Flags, die den Typ der zurückgegebenen Zeichenfolge steuert.</span><span class="sxs-lookup"><span data-stu-id="84cae-108">[in] A bitmask of flags that controls the type of the returned string.</span></span> <span data-ttu-id="84cae-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="84cae-109">The following flag can be set:</span></span>
    
<span data-ttu-id="84cae-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="84cae-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="84cae-111">Die zurückgegebene Zeichenfolge befindet sich im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="84cae-111">The returned string is in Unicode format.</span></span> <span data-ttu-id="84cae-112">Wenn das MAPI_UNICODE nicht festgelegt ist, hat die Zeichenfolge das ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="84cae-112">If the MAPI_UNICODE flag is not set, the string is in ANSI format.</span></span>
    
 <span data-ttu-id="84cae-113">_pszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="84cae-113">_pszDisplayName_</span></span>
  
> <span data-ttu-id="84cae-114">[out] Ein Zeiger auf eine Zeichenfolge, die den Anzeigenamen des Formularcontainers enthält.</span><span class="sxs-lookup"><span data-stu-id="84cae-114">[out] A pointer to a string that contains the display name of the form container.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="84cae-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="84cae-115">Return value</span></span>

<span data-ttu-id="84cae-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="84cae-116">S_OK</span></span> 
  
> <span data-ttu-id="84cae-117">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="84cae-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="84cae-118">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="84cae-118">MFCMAPI reference</span></span>

<span data-ttu-id="84cae-119">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="84cae-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="84cae-120">**Datei**</span><span class="sxs-lookup"><span data-stu-id="84cae-120">**File**</span></span>|<span data-ttu-id="84cae-121">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="84cae-121">**Function**</span></span>|<span data-ttu-id="84cae-122">**Comment**</span><span class="sxs-lookup"><span data-stu-id="84cae-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="84cae-123">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="84cae-123">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="84cae-124">CFormContainerDlg::CFormContainerDlg</span><span class="sxs-lookup"><span data-stu-id="84cae-124">CFormContainerDlg::CFormContainerDlg</span></span>  <br/> |<span data-ttu-id="84cae-125">MFCMAPI verwendet die **IMAPIFormContainer::GetDisplay-Methode,** um den Namen des Formularcontainers zu erhalten, wenn CFormContainerDlg gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="84cae-125">MFCMAPI uses the **IMAPIFormContainer::GetDisplay** method to get the name of the form container when it renders CFormContainerDlg.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="84cae-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84cae-126">See also</span></span>



[<span data-ttu-id="84cae-127">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="84cae-127">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="84cae-128">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="84cae-128">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

