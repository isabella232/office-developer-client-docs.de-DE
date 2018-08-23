---
title: IABContainerDeleteEntries
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.DeleteEntries
api_type:
- COM
ms.assetid: 70a24811-0c41-4b44-8c63-7ef807bc9051
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4140dc39b7f866b0372e5940aef5efc0524ad593
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573110"
---
# <a name="iabcontainerdeleteentries"></a><span data-ttu-id="7e85a-103">IABContainer::DeleteEntries</span><span class="sxs-lookup"><span data-stu-id="7e85a-103">IABContainer::DeleteEntries</span></span>

  
  
<span data-ttu-id="7e85a-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7e85a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7e85a-105">Entfernt einen oder mehrere Einträge in der Regel messaging Benutzern, Verteilerlisten oder andere Container.</span><span class="sxs-lookup"><span data-stu-id="7e85a-105">Removes one or more entries, typically messaging users, distribution lists, or other containers.</span></span>
  
```cpp
HRESULT DeleteEntries(
  LPENTRYLIST lpEntries,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="7e85a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e85a-106">Parameters</span></span>

 <span data-ttu-id="7e85a-107">_lpEntries_</span><span class="sxs-lookup"><span data-stu-id="7e85a-107">_lpEntries_</span></span>
  
> <span data-ttu-id="7e85a-108">[in] Ein Zeiger auf ein Array von [ENTRYLIST](entrylist.md) -Strukturen, die Eintragsbezeichner enthalten, die die zu löschenden Einträge darstellen.</span><span class="sxs-lookup"><span data-stu-id="7e85a-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that contain entry identifiers that represent the entries being deleted.</span></span> 
    
 <span data-ttu-id="7e85a-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7e85a-109">_ulFlags_</span></span>
  
> <span data-ttu-id="7e85a-110">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="7e85a-110">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7e85a-111">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="7e85a-111">Return value</span></span>

<span data-ttu-id="7e85a-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="7e85a-112">S_OK</span></span> 
  
> <span data-ttu-id="7e85a-113">Die angegebenen Einträge wurden gelöscht.</span><span class="sxs-lookup"><span data-stu-id="7e85a-113">The specified entries have been successfully deleted.</span></span> 
    
<span data-ttu-id="7e85a-114">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="7e85a-114">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="7e85a-115">Der Aufruf war erfolgreich, aber eine oder mehrere Einträge konnte nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="7e85a-115">The call succeeded, but one or more of the entries could not be deleted.</span></span> <span data-ttu-id="7e85a-116">Wenn dieser Wert zurückgegeben wird, sollte der Anruf als erfolgreich verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="7e85a-116">When this value is returned, the call should be handled as successful.</span></span> <span data-ttu-id="7e85a-117">Verwenden Sie das Makro **HR_FAILED** , um für diesen Wert zu testen.</span><span class="sxs-lookup"><span data-stu-id="7e85a-117">To test for this value, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="7e85a-118">Weitere Informationen finden Sie unter [Verwendung von Makros Fehlerbehandlung](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="7e85a-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="7e85a-119">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="7e85a-119">MFCMAPI reference</span></span>

<span data-ttu-id="7e85a-120">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7e85a-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7e85a-121">**Datei**</span><span class="sxs-lookup"><span data-stu-id="7e85a-121">**File**</span></span>|<span data-ttu-id="7e85a-122">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="7e85a-122">**Function**</span></span>|<span data-ttu-id="7e85a-123">**Comment**</span><span class="sxs-lookup"><span data-stu-id="7e85a-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7e85a-124">Abdlg.cpp</span><span class="sxs-lookup"><span data-stu-id="7e85a-124">Abdlg.cpp</span></span>  <br/> |<span data-ttu-id="7e85a-125">CabDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="7e85a-125">CabDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="7e85a-126">MFCMAPI (engl.) wird die **DeleteEntries** -Methode verwendet, um einen bestimmten Eintrag aus einer Adressbuchcontainer zu löschen.</span><span class="sxs-lookup"><span data-stu-id="7e85a-126">MFCMAPI uses the **DeleteEntries** method to delete a specific entry from an address book container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7e85a-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e85a-127">See also</span></span>



[<span data-ttu-id="7e85a-128">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="7e85a-128">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)


[<span data-ttu-id="7e85a-129">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="7e85a-129">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

