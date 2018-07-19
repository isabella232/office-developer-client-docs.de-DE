---
title: PpropFindProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PpropFindProp
api_type:
- HeaderDef
ms.assetid: f23dd6f4-915b-4fe8-ab3f-6d625c7d6061
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b7755f2ec067003e47d358a9736c6d7d96ede267
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795319"
---
# <a name="ppropfindprop"></a><span data-ttu-id="c00fe-103">PpropFindProp</span><span class="sxs-lookup"><span data-stu-id="c00fe-103">PpropFindProp</span></span>

  
  
<span data-ttu-id="c00fe-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c00fe-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c00fe-105">Sucht nach einer angegebenen Eigenschaft in einer Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="c00fe-105">Searches for a specified property in a property set.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c00fe-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="c00fe-106">Header file:</span></span>  <br/> |<span data-ttu-id="c00fe-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="c00fe-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="c00fe-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="c00fe-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c00fe-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c00fe-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c00fe-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="c00fe-110">Called by:</span></span>  <br/> |<span data-ttu-id="c00fe-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="c00fe-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSPropValue PpropFindProp(
  LPSPropValue rgprop,
  ULONG cprop,
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="c00fe-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c00fe-112">Parameters</span></span>

 <span data-ttu-id="c00fe-113">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="c00fe-113">_rgprop_</span></span>
  
> <span data-ttu-id="c00fe-114">[in] Array von [SPropValue](spropvalue.md) -Strukturen, die definieren die Eigenschaften, die durchsucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="c00fe-114">[in] Array of [SPropValue](spropvalue.md) structures that define the properties to be searched.</span></span> 
    
 <span data-ttu-id="c00fe-115">_cprop_</span><span class="sxs-lookup"><span data-stu-id="c00fe-115">_cprop_</span></span>
  
> <span data-ttu-id="c00fe-116">[in] Anzahl der Eigenschaften in den Eigenschaftensatz, der durch den Parameter _Rgprop_ angegeben.</span><span class="sxs-lookup"><span data-stu-id="c00fe-116">[in] Count of properties in the property set indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="c00fe-117">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="c00fe-117">_ulPropTag_</span></span>
  
> <span data-ttu-id="c00fe-118">[in] Eigenschaftentag für die Eigenschaft in dem durch den _Rgprop_ -Parameter angegebenen Eigenschaftensatz suchen.</span><span class="sxs-lookup"><span data-stu-id="c00fe-118">[in] Property tag for the property to search for in the property set indicated by the  _rgprop_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c00fe-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c00fe-119">Return value</span></span>

 <span data-ttu-id="c00fe-120">**PpropFindProp** gibt eine [SPropValue](spropvalue.md) -Struktur definieren die Eigenschaft, die dem input-Eigenschaftentag übereinstimmt, oder NULL, wenn keine Übereinstimmung vorliegt.</span><span class="sxs-lookup"><span data-stu-id="c00fe-120">**PpropFindProp** returns an [SPropValue](spropvalue.md) structure defining the property that matches the input property tag, or NULL if there is no match.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c00fe-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c00fe-121">Remarks</span></span>

<span data-ttu-id="c00fe-122">Wenn der angegebene Eigenschaftstag eine Eigenschaft vom Typ PT_UNSPECIFIED gibt an, sucht die **PpropFindProp** -Funktion nur eine Übereinstimmung mit der Bezeichner für die in das Tag an.</span><span class="sxs-lookup"><span data-stu-id="c00fe-122">If the given property tag indicates a property of type PT_UNSPECIFIED, the **PpropFindProp** function finds a match only for the property identifier in the tag.</span></span> <span data-ttu-id="c00fe-123">Andernfalls findet eine Übereinstimmung für das gesamte Eigenschafts-Tag, einschließlich den Eigenschaftentyp und gibt die angegebene Eigenschaft zurück.</span><span class="sxs-lookup"><span data-stu-id="c00fe-123">Otherwise, it finds a match for the entire property tag, including the property type, and returns the property identified.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c00fe-124">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="c00fe-124">MFCMAPI reference</span></span>

<span data-ttu-id="c00fe-125">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c00fe-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c00fe-126">**Datei**</span><span class="sxs-lookup"><span data-stu-id="c00fe-126">**File**</span></span>|<span data-ttu-id="c00fe-127">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="c00fe-127">**Function**</span></span>|<span data-ttu-id="c00fe-128">**Comment**</span><span class="sxs-lookup"><span data-stu-id="c00fe-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c00fe-129">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="c00fe-129">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="c00fe-130">CContentsTableListCtrl::BuildDataItem</span><span class="sxs-lookup"><span data-stu-id="c00fe-130">CContentsTableListCtrl::BuildDataItem</span></span>  <br/> |<span data-ttu-id="c00fe-131">MFCMAPI (engl.) verwendet die **PpropFindProp** -Methode, um zu finden, dass Eigenschaften in einer Eigenschaft festgelegt, die der Liste hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="c00fe-131">MFCMAPI uses the **PpropFindProp** method to find properties in a property set being added to the list.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c00fe-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c00fe-132">See also</span></span>



[<span data-ttu-id="c00fe-133">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="c00fe-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

