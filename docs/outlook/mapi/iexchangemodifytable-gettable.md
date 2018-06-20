---
title: IExchangeModifyTableGetTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable.GetTable
api_type:
- COM
ms.assetid: 97df32c4-07c6-41f1-84e7-c6e87d396e34
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0cf9373c68d533908b857a4d8f1c0e71aa11846f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792065"
---
# <a name="iexchangemodifytablegettable"></a><span data-ttu-id="f15e8-103">IExchangeModifyTable::GetTable</span><span class="sxs-lookup"><span data-stu-id="f15e8-103">IExchangeModifyTable::GetTable</span></span>

  
  
<span data-ttu-id="f15e8-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f15e8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f15e8-105">Gibt einen Zeiger auf eine Schnittstelle für ein MAPI-Table-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="f15e8-105">Returns a pointer to an interface for a MAPI table object.</span></span>
  
```cpp
HRESULT GetTable( 
  ULONG ulFlags, 
  LPMAPITABLE FAR * lppTable 
); 

```

## <a name="parameters"></a><span data-ttu-id="f15e8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f15e8-106">Parameters</span></span>

 <span data-ttu-id="f15e8-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f15e8-107">_ulFlags_</span></span>
  
> <span data-ttu-id="f15e8-108">[in] Reserviert. 0 (null) muss sein.</span><span class="sxs-lookup"><span data-stu-id="f15e8-108">[in] Reserved; must be 0 (zero).</span></span>
    
<span data-ttu-id="f15e8-109">ACLTABLE_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="f15e8-109">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="f15e8-110">Neue Rechte festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f15e8-110">Sets new rights.</span></span>
    
<span data-ttu-id="f15e8-111">frightsFreeBusyDetailed</span><span class="sxs-lookup"><span data-stu-id="f15e8-111">frightsFreeBusyDetailed</span></span>
  
> <span data-ttu-id="f15e8-112">Wenn ACLTABLE_FREEBUSY übergeben wird, bietet eine detaillierte Ansicht der Rechte für neue Frei/Gebucht-Informationen.</span><span class="sxs-lookup"><span data-stu-id="f15e8-112">When ACLTABLE_FREEBUSY is passed, provides a detailed display of new free/busy rights.</span></span>
    
<span data-ttu-id="f15e8-113">frightsFreeBusySimple</span><span class="sxs-lookup"><span data-stu-id="f15e8-113">frightsFreeBusySimple</span></span>
  
> <span data-ttu-id="f15e8-114">Wenn ACLTABLE_FREEBUSY übergeben wird, bietet eine einfache Anzeige von Frei/Gebucht-Informationen Rechte für neue.</span><span class="sxs-lookup"><span data-stu-id="f15e8-114">When ACLTABLE_FREEBUSY is passed, provides a simple display of new free/busy rights.</span></span>
    
 <span data-ttu-id="f15e8-115">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="f15e8-115">_lppTable_</span></span>
  
> <span data-ttu-id="f15e8-116">[out] Verweist auf eine [IMAPITable: IUnknown](imapitableiunknown.md) Schnittstelle, die das Table-Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="f15e8-116">[out] Points to a [IMAPITable : IUnknown](imapitableiunknown.md) interface containing the table object.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="f15e8-117">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="f15e8-117">MFCMAPI reference</span></span>

<span data-ttu-id="f15e8-118">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="f15e8-118">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f15e8-119">**Datei**</span><span class="sxs-lookup"><span data-stu-id="f15e8-119">**File**</span></span>|<span data-ttu-id="f15e8-120">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="f15e8-120">**Function**</span></span>|<span data-ttu-id="f15e8-121">**Comment**</span><span class="sxs-lookup"><span data-stu-id="f15e8-121">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f15e8-122">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="f15e8-122">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="f15e8-123">CRulesDlg::OnRefreshView</span><span class="sxs-lookup"><span data-stu-id="f15e8-123">CRulesDlg::OnRefreshView</span></span>  <br/> |<span data-ttu-id="f15e8-124">MFCMAPI (engl.) wird die **IExchangeModifyTable::GetTable** -Methode zum Abrufen einer Tabelle der Regeln verwendet.</span><span class="sxs-lookup"><span data-stu-id="f15e8-124">MFCMAPI uses the **IExchangeModifyTable::GetTable** method to get a table of rules.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f15e8-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f15e8-125">See also</span></span>



[<span data-ttu-id="f15e8-126">IExchangeModifyTable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="f15e8-126">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="f15e8-127">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="f15e8-127">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

