---
title: IExchangeModifyTableModifyTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable.ModifyTable
api_type:
- COM
ms.assetid: b9a745cc-260d-4a1c-896e-6a038ab3cfb9
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9e7f24fb4b444f63b6277d1844a7948f5ab0c590
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792053"
---
# <a name="iexchangemodifytablemodifytable"></a><span data-ttu-id="2c10d-103">IExchangeModifyTable::ModifyTable</span><span class="sxs-lookup"><span data-stu-id="2c10d-103">IExchangeModifyTable::ModifyTable</span></span>

  
  
<span data-ttu-id="2c10d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2c10d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2c10d-105">Aktualisiert ein MAPI-Table-Objekt.</span><span class="sxs-lookup"><span data-stu-id="2c10d-105">Updates a MAPI table object.</span></span>
  
```cpp
HRESULT ModifyTable( 
  ULONG ulFlags, 
  LPROWLIST lpMods 
); 

```

## <a name="parameters"></a><span data-ttu-id="2c10d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c10d-106">Parameters</span></span>

 <span data-ttu-id="2c10d-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2c10d-107">_ulFlags_</span></span>
  
> <span data-ttu-id="2c10d-108">[in] Verwenden Sie eine der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="2c10d-108">[in] Use one of the following values:</span></span> 
    
<span data-ttu-id="2c10d-109">0 (Null)</span><span class="sxs-lookup"><span data-stu-id="2c10d-109">0 (zero)</span></span>
  
> <span data-ttu-id="2c10d-110">Verwenden Sie den Wert des Elements **UlRowFlags** der [ROWENTRY](rowentry.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="2c10d-110">Use the value of the **ulRowFlags** member of the [ROWENTRY](rowentry.md) structure.</span></span> 
    
<span data-ttu-id="2c10d-111">ACLTABLE_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="2c10d-111">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="2c10d-112">Neue Rechte festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2c10d-112">Sets new rights.</span></span>
    
<span data-ttu-id="2c10d-113">frightsFreeBusyDetailed</span><span class="sxs-lookup"><span data-stu-id="2c10d-113">frightsFreeBusyDetailed</span></span>
  
> <span data-ttu-id="2c10d-114">Wenn ACLTABLE_FREEBUSY übergeben wird, bietet eine detaillierte Ansicht der Rechte für neue Frei/Gebucht-Informationen.</span><span class="sxs-lookup"><span data-stu-id="2c10d-114">When ACLTABLE_FREEBUSY is passed, provides a detailed display of new free/busy rights.</span></span>
    
<span data-ttu-id="2c10d-115">frightsFreeBusySimple</span><span class="sxs-lookup"><span data-stu-id="2c10d-115">frightsFreeBusySimple</span></span>
  
> <span data-ttu-id="2c10d-116">Wenn ACLTABLE_FREEBUSY übergeben wird, bietet eine einfache Anzeige von Frei/Gebucht-Informationen Rechte für neue.</span><span class="sxs-lookup"><span data-stu-id="2c10d-116">When ACLTABLE_FREEBUSY is passed, provides a simple display of new free/busy rights.</span></span>
    
<span data-ttu-id="2c10d-117">ROWLIST_REPLACE</span><span class="sxs-lookup"><span data-stu-id="2c10d-117">ROWLIST_REPLACE</span></span>
  
> <span data-ttu-id="2c10d-118">Ersetzen Sie alle Zeilen in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="2c10d-118">Replace all the rows in the table.</span></span>
    
 <span data-ttu-id="2c10d-119">_lpMods_</span><span class="sxs-lookup"><span data-stu-id="2c10d-119">_lpMods_</span></span>
  
> <span data-ttu-id="2c10d-120">[in] Verweist auf eine [ROWLIST](rowlist.md) -Struktur mit den Eigenschaften für das Table-Objekt.</span><span class="sxs-lookup"><span data-stu-id="2c10d-120">[in] Points to a [ROWLIST](rowlist.md) structure containing the properties for the table object.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="2c10d-121">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="2c10d-121">MFCMAPI reference</span></span>

<span data-ttu-id="2c10d-122">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="2c10d-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2c10d-123">**Datei**</span><span class="sxs-lookup"><span data-stu-id="2c10d-123">**File**</span></span>|<span data-ttu-id="2c10d-124">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="2c10d-124">**Function**</span></span>|<span data-ttu-id="2c10d-125">**Comment**</span><span class="sxs-lookup"><span data-stu-id="2c10d-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2c10d-126">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="2c10d-126">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="2c10d-127">CRulesDlg::OnModifySelectedItem</span><span class="sxs-lookup"><span data-stu-id="2c10d-127">CRulesDlg::OnModifySelectedItem</span></span>  <br/> |<span data-ttu-id="2c10d-128">MFCMAPI (engl.) wird die **IExchangeModifyTable::ModifyTable** -Methode verwendet, um eine geänderte Regel in der Tabelle der Regeln zurückzuschreiben.</span><span class="sxs-lookup"><span data-stu-id="2c10d-128">MFCMAPI uses the **IExchangeModifyTable::ModifyTable** method to write a modified rule back to the table of rules.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2c10d-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c10d-129">See also</span></span>



[<span data-ttu-id="2c10d-130">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2c10d-130">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="2c10d-131">ROWENTRY</span><span class="sxs-lookup"><span data-stu-id="2c10d-131">ROWENTRY</span></span>](rowentry.md)
  
[<span data-ttu-id="2c10d-132">ROWLIST</span><span class="sxs-lookup"><span data-stu-id="2c10d-132">ROWLIST</span></span>](rowlist.md)


[<span data-ttu-id="2c10d-133">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="2c10d-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

