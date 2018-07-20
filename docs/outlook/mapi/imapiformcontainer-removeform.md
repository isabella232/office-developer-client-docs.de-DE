---
title: IMAPIFormContainerRemoveForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.RemoveForm
api_type:
- COM
ms.assetid: 7f851ce8-bd01-4ea5-86e0-e44323cc0aab
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0d2c908f86ccd66ffd3a2eb2506d129ee2a14d48
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792142"
---
# <a name="imapiformcontainerremoveform"></a><span data-ttu-id="6dd0e-103">IMAPIFormContainer::RemoveForm</span><span class="sxs-lookup"><span data-stu-id="6dd0e-103">IMAPIFormContainer::RemoveForm</span></span>

  
  
<span data-ttu-id="6dd0e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6dd0e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6dd0e-105">Entfernt ein bestimmtes Formular aus einem Formular Container.</span><span class="sxs-lookup"><span data-stu-id="6dd0e-105">Removes a particular form from a form container.</span></span>
  
```cpp
HRESULT RemoveForm(
  LPCSTR szMessageClass
);
```

## <a name="parameters"></a><span data-ttu-id="6dd0e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6dd0e-106">Parameters</span></span>

 <span data-ttu-id="6dd0e-107">_szMessageClass_</span><span class="sxs-lookup"><span data-stu-id="6dd0e-107">_szMessageClass_</span></span>
  
> <span data-ttu-id="6dd0e-108">[in] Eine Zeichenfolge, die den Namen die Nachrichtenklasse des Formulars aus dem Container Formular entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6dd0e-108">[in] A string that names the message class of the form to be removed from the form container.</span></span> <span data-ttu-id="6dd0e-109">Nachrichtenklassennamen sind immer noch nie Unicode-ANSI-Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="6dd0e-109">Message class names are always ANSI strings, never Unicode.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6dd0e-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6dd0e-110">Return value</span></span>

<span data-ttu-id="6dd0e-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="6dd0e-111">S_OK</span></span> 
  
> <span data-ttu-id="6dd0e-112">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="6dd0e-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="6dd0e-113">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="6dd0e-113">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="6dd0e-114">Die Nachrichtenklasse in der _SzMessageClass_ -Parameter übergeben entspricht nicht die Nachrichtenklasse für jedes Formular in der Form Container.</span><span class="sxs-lookup"><span data-stu-id="6dd0e-114">The message class passed in the  _szMessageClass_ parameter does not match the message class of any form in the form container.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="6dd0e-115">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="6dd0e-115">MFCMAPI reference</span></span>

<span data-ttu-id="6dd0e-116">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="6dd0e-116">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6dd0e-117">**Datei**</span><span class="sxs-lookup"><span data-stu-id="6dd0e-117">**File**</span></span>|<span data-ttu-id="6dd0e-118">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="6dd0e-118">**Function**</span></span>|<span data-ttu-id="6dd0e-119">**Comment**</span><span class="sxs-lookup"><span data-stu-id="6dd0e-119">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6dd0e-120">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="6dd0e-120">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="6dd0e-121">CFormContainerDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="6dd0e-121">CFormContainerDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="6dd0e-122">MFCMAPI (engl.) verwendet die **IMAPIFormContainer::RemoveForm** -Methode, um ein Formular aus einem Formular Container zu löschen.</span><span class="sxs-lookup"><span data-stu-id="6dd0e-122">MFCMAPI uses the **IMAPIFormContainer::RemoveForm** method to delete a form from a form container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6dd0e-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6dd0e-123">See also</span></span>



[<span data-ttu-id="6dd0e-124">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6dd0e-124">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="6dd0e-125">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="6dd0e-125">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

