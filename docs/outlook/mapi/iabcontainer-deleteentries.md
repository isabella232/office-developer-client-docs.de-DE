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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e3b238129e55e03da33ef3af75ecce7e73fbad03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339382"
---
# <a name="iabcontainerdeleteentries"></a><span data-ttu-id="a57d0-103">IABContainer::DeleteEntries</span><span class="sxs-lookup"><span data-stu-id="a57d0-103">IABContainer::DeleteEntries</span></span>

  
  
<span data-ttu-id="a57d0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a57d0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a57d0-105">Entfernt einen oder mehrere Einträge, in der Regel Messagingbenutzer, Verteilerlisten oder andere Container.</span><span class="sxs-lookup"><span data-stu-id="a57d0-105">Removes one or more entries, typically messaging users, distribution lists, or other containers.</span></span>
  
```cpp
HRESULT DeleteEntries(
  LPENTRYLIST lpEntries,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a57d0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a57d0-106">Parameters</span></span>

 <span data-ttu-id="a57d0-107">_lpEntries_</span><span class="sxs-lookup"><span data-stu-id="a57d0-107">_lpEntries_</span></span>
  
> <span data-ttu-id="a57d0-108">in Ein Zeiger auf ein Array von [entrylist](entrylist.md) -Strukturen, die Eintrags-IDs enthalten, die die zu löschenden Einträge darstellen.</span><span class="sxs-lookup"><span data-stu-id="a57d0-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that contain entry identifiers that represent the entries being deleted.</span></span> 
    
 <span data-ttu-id="a57d0-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a57d0-109">_ulFlags_</span></span>
  
> <span data-ttu-id="a57d0-110">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="a57d0-110">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a57d0-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a57d0-111">Return value</span></span>

<span data-ttu-id="a57d0-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="a57d0-112">S_OK</span></span> 
  
> <span data-ttu-id="a57d0-113">Die angegebenen Einträge wurden erfolgreich gelöscht.</span><span class="sxs-lookup"><span data-stu-id="a57d0-113">The specified entries have been successfully deleted.</span></span> 
    
<span data-ttu-id="a57d0-114">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="a57d0-114">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="a57d0-115">Der Aufruf war erfolgreich, aber mindestens einer der Einträge konnte nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="a57d0-115">The call succeeded, but one or more of the entries could not be deleted.</span></span> <span data-ttu-id="a57d0-116">Wenn dieser Wert zurückgegeben wird, sollte der Aufruf als erfolgreich behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="a57d0-116">When this value is returned, the call should be handled as successful.</span></span> <span data-ttu-id="a57d0-117">Verwenden Sie das **HR_FAILED** -Makro, um diesen Wert zu testen.</span><span class="sxs-lookup"><span data-stu-id="a57d0-117">To test for this value, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="a57d0-118">Weitere Informationen finden Sie unter [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="a57d0-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="a57d0-119">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="a57d0-119">MFCMAPI reference</span></span>

<span data-ttu-id="a57d0-120">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a57d0-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a57d0-121">**Datei**</span><span class="sxs-lookup"><span data-stu-id="a57d0-121">**File**</span></span>|<span data-ttu-id="a57d0-122">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="a57d0-122">**Function**</span></span>|<span data-ttu-id="a57d0-123">**Comment**</span><span class="sxs-lookup"><span data-stu-id="a57d0-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a57d0-124">Abdlg. cpp</span><span class="sxs-lookup"><span data-stu-id="a57d0-124">Abdlg.cpp</span></span>  <br/> |<span data-ttu-id="a57d0-125">CabDlg:: OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="a57d0-125">CabDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="a57d0-126">MFCMAPI verwendet die **DeleteEntries** -Methode, um einen bestimmten Eintrag aus einem Adressbuchcontainer zu löschen.</span><span class="sxs-lookup"><span data-stu-id="a57d0-126">MFCMAPI uses the **DeleteEntries** method to delete a specific entry from an address book container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a57d0-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a57d0-127">See also</span></span>



[<span data-ttu-id="a57d0-128">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="a57d0-128">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)


[<span data-ttu-id="a57d0-129">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="a57d0-129">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

