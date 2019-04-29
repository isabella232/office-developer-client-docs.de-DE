---
title: IProfAdminGetProfileTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.GetProfileTable
api_type:
- COM
ms.assetid: cebccd2d-8215-486e-9964-7fc42412cec6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2db7dba67e7b71df6921ecd97189255a0ef7823a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414645"
---
# <a name="iprofadmingetprofiletable"></a><span data-ttu-id="cbb6e-103">IProfAdmin::GetProfileTable</span><span class="sxs-lookup"><span data-stu-id="cbb6e-103">IProfAdmin::GetProfileTable</span></span>

  
  
<span data-ttu-id="cbb6e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cbb6e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cbb6e-105">Ermöglicht den Zugriff auf die Profiltabelle, eine Tabelle, die Informationen zu allen verfügbaren Profilen enthält.</span><span class="sxs-lookup"><span data-stu-id="cbb6e-105">Provides access to the profile table, a table that contains information about all of the available profiles.</span></span>
  
```cpp
HRESULT GetProfileTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="cbb6e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cbb6e-106">Parameters</span></span>

 <span data-ttu-id="cbb6e-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cbb6e-107">_ulFlags_</span></span>
  
> <span data-ttu-id="cbb6e-108">in Immer NULL.</span><span class="sxs-lookup"><span data-stu-id="cbb6e-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="cbb6e-109">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="cbb6e-109">_lppTable_</span></span>
  
> <span data-ttu-id="cbb6e-110">Out Ein Zeiger auf einen Zeiger auf die Profiltabelle.</span><span class="sxs-lookup"><span data-stu-id="cbb6e-110">[out] A pointer to a pointer to the profile table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cbb6e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cbb6e-111">Return value</span></span>

<span data-ttu-id="cbb6e-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="cbb6e-112">S_OK</span></span> 
  
> <span data-ttu-id="cbb6e-113">Die Profiltabelle wurde erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="cbb6e-113">The profile table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cbb6e-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cbb6e-114">Remarks</span></span>

<span data-ttu-id="cbb6e-115">Die **IProfAdmin::** getprofilable-Methode ermöglicht den Zugriff auf die Profiltabelle, die eine Zeile für jedes verfügbare Profil enthält.</span><span class="sxs-lookup"><span data-stu-id="cbb6e-115">The **IProfAdmin::GetProfileTable** method provides access to the profile table, which contains one row for every available profile.</span></span> <span data-ttu-id="cbb6e-116">Es gibt nur zwei Spalten in jeder Zeile: der Anzeigename des Profils und ein Flag, das angibt, ob das Profil der Standardwert ist.</span><span class="sxs-lookup"><span data-stu-id="cbb6e-116">There are only two columns in each row: the profile's display name, and a flag that indicates whether the profile is the default.</span></span> 
  
<span data-ttu-id="cbb6e-117">Profile, die gelöscht wurden oder verwendet werden, aber zum Löschen markiert wurden, sind nicht in der Profiltabelle enthalten.</span><span class="sxs-lookup"><span data-stu-id="cbb6e-117">Profiles that have been deleted, or that are in use but have been marked for deletion, are not included in the profile table.</span></span> <span data-ttu-id="cbb6e-118">Die Profiltabelle ist statisch; nachfolgende Ergänzungen und Löschungen von Profilen werden in der Tabelle nicht wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="cbb6e-118">The profile table is static; subsequent additions and deletions of profiles are not reflected in the table.</span></span> 
  
<span data-ttu-id="cbb6e-119">Wenn keine Profile vorhanden sind \*\*\*\* , gibt getprofilable eine Tabelle mit null Zeilen zurück.</span><span class="sxs-lookup"><span data-stu-id="cbb6e-119">If no profiles exist, **GetProfileTable** returns a table with zero rows.</span></span> 
  
<span data-ttu-id="cbb6e-120">Weitere Informationen zur Profiltabelle finden Sie unter [profile](profile-tables.md)Tables.</span><span class="sxs-lookup"><span data-stu-id="cbb6e-120">For more information about the profile table, see [Profile Tables](profile-tables.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="cbb6e-121">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="cbb6e-121">MFCMAPI reference</span></span>

<span data-ttu-id="cbb6e-122">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="cbb6e-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="cbb6e-123">**Datei**</span><span class="sxs-lookup"><span data-stu-id="cbb6e-123">**File**</span></span>|<span data-ttu-id="cbb6e-124">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="cbb6e-124">**Function**</span></span>|<span data-ttu-id="cbb6e-125">**Comment**</span><span class="sxs-lookup"><span data-stu-id="cbb6e-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cbb6e-126">MainDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="cbb6e-126">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="cbb6e-127">CMainDlg:: OnShowProfiles</span><span class="sxs-lookup"><span data-stu-id="cbb6e-127">CMainDlg::OnShowProfiles</span></span>  <br/> |<span data-ttu-id="cbb6e-128">MFCMAPI verwendet die **IProfAdmin::** getprofilable-Methode, um die Profiltabelle abzurufen, die in einem neuen Dialogfeld angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cbb6e-128">MFCMAPI uses the **IProfAdmin::GetProfileTable** method to get the profile table to display in a new dialog box.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cbb6e-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cbb6e-129">See also</span></span>



[<span data-ttu-id="cbb6e-130">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cbb6e-130">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="cbb6e-131">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="cbb6e-131">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="cbb6e-132">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cbb6e-132">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


[<span data-ttu-id="cbb6e-133">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="cbb6e-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

