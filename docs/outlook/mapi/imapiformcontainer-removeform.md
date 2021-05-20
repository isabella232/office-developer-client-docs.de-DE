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
ms.openlocfilehash: e53c0cbd9946ff04516594a7ce99fdc2daf4ff4d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432198"
---
# <a name="imapiformcontainerremoveform"></a><span data-ttu-id="0d1b7-103">IMAPIFormContainer::RemoveForm</span><span class="sxs-lookup"><span data-stu-id="0d1b7-103">IMAPIFormContainer::RemoveForm</span></span>

  
  
<span data-ttu-id="0d1b7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d1b7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d1b7-105">Entfernt ein bestimmtes Formular aus einem Formularcontainer.</span><span class="sxs-lookup"><span data-stu-id="0d1b7-105">Removes a particular form from a form container.</span></span>
  
```cpp
HRESULT RemoveForm(
  LPCSTR szMessageClass
);
```

## <a name="parameters"></a><span data-ttu-id="0d1b7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d1b7-106">Parameters</span></span>

 <span data-ttu-id="0d1b7-107">_szMessageClass_</span><span class="sxs-lookup"><span data-stu-id="0d1b7-107">_szMessageClass_</span></span>
  
> <span data-ttu-id="0d1b7-108">[in] Eine Zeichenfolge, die die Nachrichtenklasse des Formulars benennt, das aus dem Formularcontainer entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0d1b7-108">[in] A string that names the message class of the form to be removed from the form container.</span></span> <span data-ttu-id="0d1b7-109">Nachrichtenklassennamen sind immer ANSI-Zeichenfolgen, nie Unicode.</span><span class="sxs-lookup"><span data-stu-id="0d1b7-109">Message class names are always ANSI strings, never Unicode.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0d1b7-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0d1b7-110">Return value</span></span>

<span data-ttu-id="0d1b7-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="0d1b7-111">S_OK</span></span> 
  
> <span data-ttu-id="0d1b7-112">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="0d1b7-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="0d1b7-113">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="0d1b7-113">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="0d1b7-114">Die im  _szMessageClass-Parameter_ übergebene Nachrichtenklasse ist nicht mit der Nachrichtenklasse eines Formulars im Formularcontainer übereinstimmend.</span><span class="sxs-lookup"><span data-stu-id="0d1b7-114">The message class passed in the  _szMessageClass_ parameter does not match the message class of any form in the form container.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="0d1b7-115">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="0d1b7-115">MFCMAPI reference</span></span>

<span data-ttu-id="0d1b7-116">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="0d1b7-116">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0d1b7-117">**Datei**</span><span class="sxs-lookup"><span data-stu-id="0d1b7-117">**File**</span></span>|<span data-ttu-id="0d1b7-118">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="0d1b7-118">**Function**</span></span>|<span data-ttu-id="0d1b7-119">**Comment**</span><span class="sxs-lookup"><span data-stu-id="0d1b7-119">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0d1b7-120">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="0d1b7-120">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="0d1b7-121">CFormContainerDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="0d1b7-121">CFormContainerDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="0d1b7-122">MFCMAPI verwendet die **IMAPIFormContainer::RemoveForm-Methode,** um ein Formular aus einem Formularcontainer zu löschen.</span><span class="sxs-lookup"><span data-stu-id="0d1b7-122">MFCMAPI uses the **IMAPIFormContainer::RemoveForm** method to delete a form from a form container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0d1b7-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d1b7-123">See also</span></span>



[<span data-ttu-id="0d1b7-124">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0d1b7-124">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="0d1b7-125">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="0d1b7-125">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

