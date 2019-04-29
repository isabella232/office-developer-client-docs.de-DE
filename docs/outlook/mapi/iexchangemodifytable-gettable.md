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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 87c60f424e08eea011bb643041196ca9445a3aa1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436244"
---
# <a name="iexchangemodifytablegettable"></a><span data-ttu-id="27a6e-103">IExchangeModifyTable::GetTable</span><span class="sxs-lookup"><span data-stu-id="27a6e-103">IExchangeModifyTable::GetTable</span></span>

  
  
<span data-ttu-id="27a6e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27a6e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27a6e-105">Gibt einen Zeiger auf eine Schnittstelle für ein MAPI-Tabellenobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="27a6e-105">Returns a pointer to an interface for a MAPI table object.</span></span>
  
```cpp
HRESULT GetTable( 
  ULONG ulFlags, 
  LPMAPITABLE FAR * lppTable 
); 

```

## <a name="parameters"></a><span data-ttu-id="27a6e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="27a6e-106">Parameters</span></span>

 <span data-ttu-id="27a6e-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="27a6e-107">_ulFlags_</span></span>
  
> <span data-ttu-id="27a6e-108">in Reserviert muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="27a6e-108">[in] Reserved; must be 0 (zero).</span></span>
    
<span data-ttu-id="27a6e-109">ACLTABLE_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="27a6e-109">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="27a6e-110">Legt neue Rechte fest.</span><span class="sxs-lookup"><span data-stu-id="27a6e-110">Sets new rights.</span></span>
    
<span data-ttu-id="27a6e-111">frightsFreeBusyDetailed</span><span class="sxs-lookup"><span data-stu-id="27a6e-111">frightsFreeBusyDetailed</span></span>
  
> <span data-ttu-id="27a6e-112">Wenn ACLTABLE_FREEBUSY übergeben wird, werden neue frei/gebucht-Rechte ausführlich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="27a6e-112">When ACLTABLE_FREEBUSY is passed, provides a detailed display of new free/busy rights.</span></span>
    
<span data-ttu-id="27a6e-113">frightsFreeBusySimple</span><span class="sxs-lookup"><span data-stu-id="27a6e-113">frightsFreeBusySimple</span></span>
  
> <span data-ttu-id="27a6e-114">Wenn ACLTABLE_FREEBUSY übergeben wird, bietet eine einfache Anzeige der neuen frei/gebucht-Rechte.</span><span class="sxs-lookup"><span data-stu-id="27a6e-114">When ACLTABLE_FREEBUSY is passed, provides a simple display of new free/busy rights.</span></span>
    
 <span data-ttu-id="27a6e-115">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="27a6e-115">_lppTable_</span></span>
  
> <span data-ttu-id="27a6e-116">Out Verweist auf eine [IMAPITable: IUnknown](imapitableiunknown.md) -Schnittstelle, die das Table-Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="27a6e-116">[out] Points to a [IMAPITable : IUnknown](imapitableiunknown.md) interface containing the table object.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="27a6e-117">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="27a6e-117">MFCMAPI reference</span></span>

<span data-ttu-id="27a6e-118">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="27a6e-118">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="27a6e-119">**Datei**</span><span class="sxs-lookup"><span data-stu-id="27a6e-119">**File**</span></span>|<span data-ttu-id="27a6e-120">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="27a6e-120">**Function**</span></span>|<span data-ttu-id="27a6e-121">**Comment**</span><span class="sxs-lookup"><span data-stu-id="27a6e-121">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="27a6e-122">RulesDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="27a6e-122">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="27a6e-123">CRulesDlg:: OnRefreshView</span><span class="sxs-lookup"><span data-stu-id="27a6e-123">CRulesDlg::OnRefreshView</span></span>  <br/> |<span data-ttu-id="27a6e-124">MFCMAPI verwendet die **IExchangeModifyTable:: GetTable** -Methode, um eine Tabelle mit Regeln abzurufen.</span><span class="sxs-lookup"><span data-stu-id="27a6e-124">MFCMAPI uses the **IExchangeModifyTable::GetTable** method to get a table of rules.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="27a6e-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27a6e-125">See also</span></span>



[<span data-ttu-id="27a6e-126">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="27a6e-126">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="27a6e-127">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="27a6e-127">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

