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
ms.openlocfilehash: 66e23d73af53b05295bf2cbcd8c604ab3545bbca
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573138"
---
# <a name="imapiformcontainergetdisplay"></a><span data-ttu-id="0e8da-103">IMAPIFormContainer::GetDisplay</span><span class="sxs-lookup"><span data-stu-id="0e8da-103">IMAPIFormContainer::GetDisplay</span></span>

  
  
<span data-ttu-id="0e8da-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0e8da-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0e8da-105">Gibt den Anzeigenamen eines Containers Formular zurück.</span><span class="sxs-lookup"><span data-stu-id="0e8da-105">Returns the display name of a form container.</span></span>
  
```cpp
HRESULT GetDisplay(
  ULONG ulFlags,
  LPSTR FAR * pszDisplayName
);
```

## <a name="parameters"></a><span data-ttu-id="0e8da-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e8da-106">Parameters</span></span>

 <span data-ttu-id="0e8da-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0e8da-107">_ulFlags_</span></span>
  
> <span data-ttu-id="0e8da-108">[in] Eine Bitmaske aus Flags, die den Typ der zurückgegebenen Zeichenfolge steuert.</span><span class="sxs-lookup"><span data-stu-id="0e8da-108">[in] A bitmask of flags that controls the type of the returned string.</span></span> <span data-ttu-id="0e8da-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="0e8da-109">The following flag can be set:</span></span>
    
<span data-ttu-id="0e8da-110">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0e8da-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="0e8da-111">Die zurückgegebene Zeichenfolge wird im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="0e8da-111">The returned string is in Unicode format.</span></span> <span data-ttu-id="0e8da-112">Wenn die Option MAPI_UNICODE nicht festgelegt ist, wird die Zeichenfolge im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="0e8da-112">If the MAPI_UNICODE flag is not set, the string is in ANSI format.</span></span>
    
 <span data-ttu-id="0e8da-113">_pszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="0e8da-113">_pszDisplayName_</span></span>
  
> <span data-ttu-id="0e8da-114">[out] Ein Zeiger auf eine Zeichenfolge, die den Anzeigenamen des Containers Formular enthält.</span><span class="sxs-lookup"><span data-stu-id="0e8da-114">[out] A pointer to a string that contains the display name of the form container.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0e8da-115">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="0e8da-115">Return value</span></span>

<span data-ttu-id="0e8da-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="0e8da-116">S_OK</span></span> 
  
> <span data-ttu-id="0e8da-117">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="0e8da-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="0e8da-118">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="0e8da-118">MFCMAPI reference</span></span>

<span data-ttu-id="0e8da-119">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="0e8da-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0e8da-120">**Datei**</span><span class="sxs-lookup"><span data-stu-id="0e8da-120">**File**</span></span>|<span data-ttu-id="0e8da-121">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="0e8da-121">**Function**</span></span>|<span data-ttu-id="0e8da-122">**Comment**</span><span class="sxs-lookup"><span data-stu-id="0e8da-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0e8da-123">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="0e8da-123">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="0e8da-124">CFormContainerDlg::CFormContainerDlg</span><span class="sxs-lookup"><span data-stu-id="0e8da-124">CFormContainerDlg::CFormContainerDlg</span></span>  <br/> |<span data-ttu-id="0e8da-125">MFCMAPI (engl.) verwendet die **IMAPIFormContainer::GetDisplay** -Methode, um den Namen des Containers Formular abrufen, wenn CFormContainerDlg gerendert.</span><span class="sxs-lookup"><span data-stu-id="0e8da-125">MFCMAPI uses the **IMAPIFormContainer::GetDisplay** method to get the name of the form container when it renders CFormContainerDlg.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0e8da-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e8da-126">See also</span></span>



[<span data-ttu-id="0e8da-127">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0e8da-127">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="0e8da-128">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="0e8da-128">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

