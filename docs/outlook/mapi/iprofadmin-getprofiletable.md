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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c942bdbf27590dde04b84970e345f265bc645045
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792762"
---
# <a name="iprofadmingetprofiletable"></a><span data-ttu-id="1d932-103">IProfAdmin::GetProfileTable</span><span class="sxs-lookup"><span data-stu-id="1d932-103">IProfAdmin::GetProfileTable</span></span>

  
  
<span data-ttu-id="1d932-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1d932-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1d932-105">Bietet Zugriff auf die Benutzerprofildienst-Tabelle eine Tabelle mit Informationen zu allen verfügbaren Profilen.</span><span class="sxs-lookup"><span data-stu-id="1d932-105">Provides access to the profile table, a table that contains information about all of the available profiles.</span></span>
  
```cpp
HRESULT GetProfileTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="1d932-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d932-106">Parameters</span></span>

 <span data-ttu-id="1d932-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1d932-107">_ulFlags_</span></span>
  
> <span data-ttu-id="1d932-108">[in] Immer NULL.</span><span class="sxs-lookup"><span data-stu-id="1d932-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="1d932-109">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="1d932-109">_lppTable_</span></span>
  
> <span data-ttu-id="1d932-110">[out] Ein Zeiger auf einen Zeiger auf die Benutzerprofildienst-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1d932-110">[out] A pointer to a pointer to the profile table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1d932-111">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="1d932-111">Return value</span></span>

<span data-ttu-id="1d932-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="1d932-112">S_OK</span></span> 
  
> <span data-ttu-id="1d932-113">Die Profiltabelle wurde erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="1d932-113">The profile table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1d932-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1d932-114">Remarks</span></span>

<span data-ttu-id="1d932-115">Die **IProfAdmin::GetProfileTable** -Methode ermöglicht den Zugriff auf die Benutzerprofildienst-Tabelle, die enthält eine Zeile für jedes verfügbaren Profil.</span><span class="sxs-lookup"><span data-stu-id="1d932-115">The **IProfAdmin::GetProfileTable** method provides access to the profile table, which contains one row for every available profile.</span></span> <span data-ttu-id="1d932-116">Es gibt nur zwei Spalten in jeder Zeile: Anzeigename den Namen des Profils und ein Flag, das angibt, ob das Profil der Standardwert ist.</span><span class="sxs-lookup"><span data-stu-id="1d932-116">There are only two columns in each row: the profile's display name, and a flag that indicates whether the profile is the default.</span></span> 
  
<span data-ttu-id="1d932-117">Profile, die gelöscht oder, die verwendet werden, aber zum Löschen markiert wurden, sind nicht in der Profiltabelle enthalten.</span><span class="sxs-lookup"><span data-stu-id="1d932-117">Profiles that have been deleted, or that are in use but have been marked for deletion, are not included in the profile table.</span></span> <span data-ttu-id="1d932-118">Die Benutzerprofildienst-Tabelle ist statisch. nachfolgende hinzufügen und Löschen von Profilen werden in der Tabelle nicht wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="1d932-118">The profile table is static; subsequent additions and deletions of profiles are not reflected in the table.</span></span> 
  
<span data-ttu-id="1d932-119">Wenn keine Profile vorhanden ist, gibt **"GetProfileTable"** eine Tabelle mit 0 (null) Zeilen zurück.</span><span class="sxs-lookup"><span data-stu-id="1d932-119">If no profiles exist, **GetProfileTable** returns a table with zero rows.</span></span> 
  
<span data-ttu-id="1d932-120">Weitere Informationen zu der Tabelle "Profil" finden Sie unter [Profil Tabellen](profile-tables.md).</span><span class="sxs-lookup"><span data-stu-id="1d932-120">For more information about the profile table, see [Profile Tables](profile-tables.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1d932-121">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="1d932-121">MFCMAPI reference</span></span>

<span data-ttu-id="1d932-122">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1d932-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1d932-123">**Datei**</span><span class="sxs-lookup"><span data-stu-id="1d932-123">**File**</span></span>|<span data-ttu-id="1d932-124">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="1d932-124">**Function**</span></span>|<span data-ttu-id="1d932-125">**Comment**</span><span class="sxs-lookup"><span data-stu-id="1d932-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1d932-126">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="1d932-126">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="1d932-127">CMainDlg::OnShowProfiles</span><span class="sxs-lookup"><span data-stu-id="1d932-127">CMainDlg::OnShowProfiles</span></span>  <br/> |<span data-ttu-id="1d932-128">MFCMAPI (engl.) verwendet die **IProfAdmin::GetProfileTable** -Methode zum Abrufen der Benutzerprofildienst-Tabelle in ein neues Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1d932-128">MFCMAPI uses the **IProfAdmin::GetProfileTable** method to get the profile table to display in a new dialog box.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1d932-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d932-129">See also</span></span>



[<span data-ttu-id="1d932-130">IMAPITable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="1d932-130">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="1d932-131">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="1d932-131">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="1d932-132">IProfAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="1d932-132">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


[<span data-ttu-id="1d932-133">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="1d932-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

