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
ms.openlocfilehash: e3b238129e55e03da33ef3af75ecce7e73fbad03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425596"
---
# <a name="iabcontainerdeleteentries"></a><span data-ttu-id="30483-103">IABContainer::DeleteEntries</span><span class="sxs-lookup"><span data-stu-id="30483-103">IABContainer::DeleteEntries</span></span>

  
  
<span data-ttu-id="30483-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="30483-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="30483-105">Entfernt einen oder mehrere Einträge, in der Regel Messagingbenutzer, Verteilerlisten oder andere Container.</span><span class="sxs-lookup"><span data-stu-id="30483-105">Removes one or more entries, typically messaging users, distribution lists, or other containers.</span></span>
  
```cpp
HRESULT DeleteEntries(
  LPENTRYLIST lpEntries,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="30483-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="30483-106">Parameters</span></span>

 <span data-ttu-id="30483-107">_lpEntries_</span><span class="sxs-lookup"><span data-stu-id="30483-107">_lpEntries_</span></span>
  
> <span data-ttu-id="30483-108">[in] Ein Zeiger auf ein Array von [ENTRYLIST-Strukturen,](entrylist.md) die Eintragsbezeichner enthalten, die die zu löschenden Einträge darstellen.</span><span class="sxs-lookup"><span data-stu-id="30483-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that contain entry identifiers that represent the entries being deleted.</span></span> 
    
 <span data-ttu-id="30483-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="30483-109">_ulFlags_</span></span>
  
> <span data-ttu-id="30483-110">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="30483-110">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="30483-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="30483-111">Return value</span></span>

<span data-ttu-id="30483-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="30483-112">S_OK</span></span> 
  
> <span data-ttu-id="30483-113">Die angegebenen Einträge wurden erfolgreich gelöscht.</span><span class="sxs-lookup"><span data-stu-id="30483-113">The specified entries have been successfully deleted.</span></span> 
    
<span data-ttu-id="30483-114">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="30483-114">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="30483-115">Der Aufruf ist erfolgreich, aber mindestens einer der Einträge konnte nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="30483-115">The call succeeded, but one or more of the entries could not be deleted.</span></span> <span data-ttu-id="30483-116">Wenn dieser Wert zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="30483-116">When this value is returned, the call should be handled as successful.</span></span> <span data-ttu-id="30483-117">Verwenden Sie zum Testen dieses Werts **das HR_FAILED** Makro.</span><span class="sxs-lookup"><span data-stu-id="30483-117">To test for this value, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="30483-118">Weitere Informationen finden Sie unter [Using Macros for Error Handling](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="30483-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="30483-119">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="30483-119">MFCMAPI reference</span></span>

<span data-ttu-id="30483-120">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="30483-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="30483-121">**Datei**</span><span class="sxs-lookup"><span data-stu-id="30483-121">**File**</span></span>|<span data-ttu-id="30483-122">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="30483-122">**Function**</span></span>|<span data-ttu-id="30483-123">**Comment**</span><span class="sxs-lookup"><span data-stu-id="30483-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="30483-124">Abdlg.cpp</span><span class="sxs-lookup"><span data-stu-id="30483-124">Abdlg.cpp</span></span>  <br/> |<span data-ttu-id="30483-125">CabDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="30483-125">CabDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="30483-126">MFCMAPI verwendet die **DeleteEntries-Methode,** um einen bestimmten Eintrag aus einem Adressbuchcontainer zu löschen.</span><span class="sxs-lookup"><span data-stu-id="30483-126">MFCMAPI uses the **DeleteEntries** method to delete a specific entry from an address book container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="30483-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30483-127">See also</span></span>



[<span data-ttu-id="30483-128">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="30483-128">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)


[<span data-ttu-id="30483-129">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="30483-129">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

