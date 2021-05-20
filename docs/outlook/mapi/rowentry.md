---
title: ROWENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ROWENTRY
api_type:
- COM
ms.assetid: bd6c0d8e-68cc-4d60-9029-13ed81c816cd
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 243ab1e926171ee66b95cfd8e969cd77e2b31faf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436034"
---
# <a name="rowentry"></a><span data-ttu-id="259a0-103">ROWENTRY</span><span class="sxs-lookup"><span data-stu-id="259a0-103">ROWENTRY</span></span>

<span data-ttu-id="259a0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="259a0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="259a0-105">Enthält eine Zeile und den Vorgang, der für diese Zeile in einer Tabelle über die [IExchangeModifyTable-Schnittstelle ausgeführt](iexchangemodifytableiunknown.md) wird.</span><span class="sxs-lookup"><span data-stu-id="259a0-105">Contains a row and the operation that is performed on that row in a table through the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface.</span></span> 
  
```cpp
typedef struct
{
  ULONG         ulRowFlags;
  ULONG         cValues;
  LPSPropValue  rgPropVals;
}  ROWENTRY, FAR * LPROWENTRY;
```

## <a name="members"></a><span data-ttu-id="259a0-106">Elemente</span><span class="sxs-lookup"><span data-stu-id="259a0-106">Members</span></span>

<span data-ttu-id="259a0-107">**ulRowFlags**</span><span class="sxs-lookup"><span data-stu-id="259a0-107">**ulRowFlags**</span></span>
  
> <span data-ttu-id="259a0-108">Einer der folgenden Vorgänge, die für die Daten ausgeführt werden sollen:</span><span class="sxs-lookup"><span data-stu-id="259a0-108">One of the following operations to be performed on the data:</span></span> 
    
  - <span data-ttu-id="259a0-109">ROW_ADD: Fügen Sie der Tabelle die Daten als neue Zeile hinzu.</span><span class="sxs-lookup"><span data-stu-id="259a0-109">ROW_ADD: Add the data to the table as a new row.</span></span>
      
  - <span data-ttu-id="259a0-110">ROW_MODIFY: Ändern Sie diese Zeile in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="259a0-110">ROW_MODIFY: Modify this row in the table.</span></span>
      
  - <span data-ttu-id="259a0-111">ROW_REMOVE: Entfernen Sie diese Zeile aus der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="259a0-111">ROW_REMOVE: Remove this row from the table.</span></span>
      
  - <span data-ttu-id="259a0-112">ROW_EMPTY: Fügen Sie der Tabelle keine Zeilendaten hinzu.</span><span class="sxs-lookup"><span data-stu-id="259a0-112">ROW_EMPTY: Do not add the row data to the table.</span></span> <span data-ttu-id="259a0-113">(Die Zeile ist leer.)</span><span class="sxs-lookup"><span data-stu-id="259a0-113">(The row is empty.)</span></span>
    
<span data-ttu-id="259a0-114">**cValues**</span><span class="sxs-lookup"><span data-stu-id="259a0-114">**cValues**</span></span>
  
> <span data-ttu-id="259a0-115">Die Anzahl der Eigenschaftswerte in **rgPropvals**.</span><span class="sxs-lookup"><span data-stu-id="259a0-115">The number of property values in **rgPropvals**.</span></span>
    
<span data-ttu-id="259a0-116">**rgPropVals**</span><span class="sxs-lookup"><span data-stu-id="259a0-116">**rgPropVals**</span></span>
  
> <span data-ttu-id="259a0-117">Ein Array von [SPropValue-Strukturen,](spropvalue.md) die die Spaltenwerte darstellen, die in die Tabelle eingefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="259a0-117">An array of [SPropValue](spropvalue.md) structures representing the columns values to be inserted into the table.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="259a0-118">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="259a0-118">MFCMAPI reference</span></span>

<span data-ttu-id="259a0-119">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="259a0-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="259a0-120">**Datei**</span><span class="sxs-lookup"><span data-stu-id="259a0-120">**File**</span></span>|<span data-ttu-id="259a0-121">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="259a0-121">**Function**</span></span>|<span data-ttu-id="259a0-122">**Comment**</span><span class="sxs-lookup"><span data-stu-id="259a0-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="259a0-123">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="259a0-123">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="259a0-124">CRulesDlg::GetSelectedItems</span><span class="sxs-lookup"><span data-stu-id="259a0-124">CRulesDlg::GetSelectedItems</span></span>  <br/> |<span data-ttu-id="259a0-125">Wird verwendet, um eine Liste ausgewählter Regeln für nachfolgende **ModifyTable-Aktionen zu** erstellen.</span><span class="sxs-lookup"><span data-stu-id="259a0-125">Used to build a list of selected rules for subsequent **ModifyTable** actions.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="259a0-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="259a0-126">See also</span></span>
  
- [<span data-ttu-id="259a0-127">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="259a0-127">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
- [<span data-ttu-id="259a0-128">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="259a0-128">MAPI Structures</span></span>](mapi-structures.md)

