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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 46bb9b2cc1a4d54807d6929b4e1439b58fb3a531
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418176"
---
# <a name="iexchangemodifytablemodifytable"></a><span data-ttu-id="e1362-103">IExchangeModifyTable::ModifyTable</span><span class="sxs-lookup"><span data-stu-id="e1362-103">IExchangeModifyTable::ModifyTable</span></span>

  
  
<span data-ttu-id="e1362-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1362-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1362-105">Aktualisiert ein MAPI-Tabellenobjekt.</span><span class="sxs-lookup"><span data-stu-id="e1362-105">Updates a MAPI table object.</span></span>
  
```cpp
HRESULT ModifyTable( 
  ULONG ulFlags, 
  LPROWLIST lpMods 
); 

```

## <a name="parameters"></a><span data-ttu-id="e1362-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1362-106">Parameters</span></span>

 <span data-ttu-id="e1362-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e1362-107">_ulFlags_</span></span>
  
> <span data-ttu-id="e1362-108">in Verwenden Sie einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="e1362-108">[in] Use one of the following values:</span></span> 
    
<span data-ttu-id="e1362-109">0 (Null)</span><span class="sxs-lookup"><span data-stu-id="e1362-109">0 (zero)</span></span>
  
> <span data-ttu-id="e1362-110">Verwenden Sie den Wert des **ulRowFlags** -Elements der [ROWENTRY](rowentry.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="e1362-110">Use the value of the **ulRowFlags** member of the [ROWENTRY](rowentry.md) structure.</span></span> 
    
<span data-ttu-id="e1362-111">ACLTABLE_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="e1362-111">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="e1362-112">Legt neue Rechte fest.</span><span class="sxs-lookup"><span data-stu-id="e1362-112">Sets new rights.</span></span>
    
<span data-ttu-id="e1362-113">frightsFreeBusyDetailed</span><span class="sxs-lookup"><span data-stu-id="e1362-113">frightsFreeBusyDetailed</span></span>
  
> <span data-ttu-id="e1362-114">Wenn ACLTABLE_FREEBUSY übergeben wird, werden neue frei/gebucht-Rechte ausführlich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e1362-114">When ACLTABLE_FREEBUSY is passed, provides a detailed display of new free/busy rights.</span></span>
    
<span data-ttu-id="e1362-115">frightsFreeBusySimple</span><span class="sxs-lookup"><span data-stu-id="e1362-115">frightsFreeBusySimple</span></span>
  
> <span data-ttu-id="e1362-116">Wenn ACLTABLE_FREEBUSY übergeben wird, bietet eine einfache Anzeige der neuen frei/gebucht-Rechte.</span><span class="sxs-lookup"><span data-stu-id="e1362-116">When ACLTABLE_FREEBUSY is passed, provides a simple display of new free/busy rights.</span></span>
    
<span data-ttu-id="e1362-117">ROWLIST_REPLACE</span><span class="sxs-lookup"><span data-stu-id="e1362-117">ROWLIST_REPLACE</span></span>
  
> <span data-ttu-id="e1362-118">Ersetzen Sie alle Zeilen in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e1362-118">Replace all the rows in the table.</span></span>
    
 <span data-ttu-id="e1362-119">_lpMods_</span><span class="sxs-lookup"><span data-stu-id="e1362-119">_lpMods_</span></span>
  
> <span data-ttu-id="e1362-120">in Verweist auf eine [ROWLIST](rowlist.md) -Struktur, die die Eigenschaften für das Table-Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="e1362-120">[in] Points to a [ROWLIST](rowlist.md) structure containing the properties for the table object.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="e1362-121">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="e1362-121">MFCMAPI reference</span></span>

<span data-ttu-id="e1362-122">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e1362-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e1362-123">**Datei**</span><span class="sxs-lookup"><span data-stu-id="e1362-123">**File**</span></span>|<span data-ttu-id="e1362-124">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="e1362-124">**Function**</span></span>|<span data-ttu-id="e1362-125">**Comment**</span><span class="sxs-lookup"><span data-stu-id="e1362-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e1362-126">RulesDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="e1362-126">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="e1362-127">CRulesDlg:: OnModifySelectedItem</span><span class="sxs-lookup"><span data-stu-id="e1362-127">CRulesDlg::OnModifySelectedItem</span></span>  <br/> |<span data-ttu-id="e1362-128">MFCMAPI verwendet die **IExchangeModifyTable:: Modify** Table-Methode, um eine geänderte Regel zurück in die Tabelle der Regeln zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="e1362-128">MFCMAPI uses the **IExchangeModifyTable::ModifyTable** method to write a modified rule back to the table of rules.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e1362-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e1362-129">See also</span></span>



[<span data-ttu-id="e1362-130">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e1362-130">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="e1362-131">ROWENTRY</span><span class="sxs-lookup"><span data-stu-id="e1362-131">ROWENTRY</span></span>](rowentry.md)
  
[<span data-ttu-id="e1362-132">ROWLIST</span><span class="sxs-lookup"><span data-stu-id="e1362-132">ROWLIST</span></span>](rowlist.md)


[<span data-ttu-id="e1362-133">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="e1362-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

