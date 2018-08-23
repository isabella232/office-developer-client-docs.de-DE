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
ms.openlocfilehash: fb0bfaba1ca0a0d7d34096b3b0b1db9863207097
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576267"
---
# <a name="rowentry"></a><span data-ttu-id="03c65-103">ROWENTRY</span><span class="sxs-lookup"><span data-stu-id="03c65-103">ROWENTRY</span></span>

<span data-ttu-id="03c65-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03c65-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03c65-105">Enthält eine Zeile und den Vorgang, der für diese Zeile in einer Tabelle über die Schnittstelle [IExchangeModifyTable](iexchangemodifytableiunknown.md) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="03c65-105">Contains a row and the operation that is performed on that row in a table through the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface.</span></span> 
  
```cpp
typedef struct
{
  ULONG         ulRowFlags;
  ULONG         cValues;
  LPSPropValue  rgPropVals;
}  ROWENTRY, FAR * LPROWENTRY;
```

## <a name="members"></a><span data-ttu-id="03c65-106">Elemente</span><span class="sxs-lookup"><span data-stu-id="03c65-106">Members</span></span>

<span data-ttu-id="03c65-107">**ulRowFlags**</span><span class="sxs-lookup"><span data-stu-id="03c65-107">**ulRowFlags**</span></span>
  
> <span data-ttu-id="03c65-108">Einer der folgenden Vorgänge in die Daten ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="03c65-108">One of the following operations to be performed on the data:</span></span> 
    
  - <span data-ttu-id="03c65-109">ROW_ADD: Fügen Sie die Daten als eine neue Zeile der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="03c65-109">ROW_ADD: Add the data to the table as a new row.</span></span>
      
  - <span data-ttu-id="03c65-110">ROW_MODIFY: Ändern Sie diese Zeile in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="03c65-110">ROW_MODIFY: Modify this row in the table.</span></span>
      
  - <span data-ttu-id="03c65-111">ROW_REMOVE: Entfernen Sie diese Zeile aus der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="03c65-111">ROW_REMOVE: Remove this row from the table.</span></span>
      
  - <span data-ttu-id="03c65-112">ROW_EMPTY: Fügen Sie die Zeilendaten nicht auf die Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="03c65-112">ROW_EMPTY: Do not add the row data to the table.</span></span> <span data-ttu-id="03c65-113">(Die Zeile ist leer).</span><span class="sxs-lookup"><span data-stu-id="03c65-113">(The row is empty.)</span></span>
    
<span data-ttu-id="03c65-114">**cValues**</span><span class="sxs-lookup"><span data-stu-id="03c65-114">**cValues**</span></span>
  
> <span data-ttu-id="03c65-115">Die Anzahl der Eigenschaftswerte in **RgPropvals**.</span><span class="sxs-lookup"><span data-stu-id="03c65-115">The number of property values in **rgPropvals**.</span></span>
    
<span data-ttu-id="03c65-116">**rgPropVals**</span><span class="sxs-lookup"><span data-stu-id="03c65-116">**rgPropVals**</span></span>
  
> <span data-ttu-id="03c65-117">Ein Array von [SPropValue](spropvalue.md) -Strukturen, die Darstellung der Werte der Spalten in der Tabelle eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="03c65-117">An array of [SPropValue](spropvalue.md) structures representing the columns values to be inserted into the table.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="03c65-118">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="03c65-118">MFCMAPI reference</span></span>

<span data-ttu-id="03c65-119">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="03c65-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="03c65-120">**Datei**</span><span class="sxs-lookup"><span data-stu-id="03c65-120">**File**</span></span>|<span data-ttu-id="03c65-121">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="03c65-121">**Function**</span></span>|<span data-ttu-id="03c65-122">**Comment**</span><span class="sxs-lookup"><span data-stu-id="03c65-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="03c65-123">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="03c65-123">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="03c65-124">CRulesDlg::GetSelectedItems</span><span class="sxs-lookup"><span data-stu-id="03c65-124">CRulesDlg::GetSelectedItems</span></span>  <br/> |<span data-ttu-id="03c65-125">Verwendet, um eine Liste der ausgewählten Regeln für nachfolgende **ModifyTable** Aktionen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="03c65-125">Used to build a list of selected rules for subsequent **ModifyTable** actions.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="03c65-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03c65-126">See also</span></span>
  
- [<span data-ttu-id="03c65-127">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="03c65-127">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
- [<span data-ttu-id="03c65-128">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="03c65-128">MAPI Structures</span></span>](mapi-structures.md)

