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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 97021128f92af0486af1ba3125c7843eaa357648
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350731"
---
# <a name="ppropfindprop"></a><span data-ttu-id="5920c-103">PpropFindProp</span><span class="sxs-lookup"><span data-stu-id="5920c-103">PpropFindProp</span></span>

  
  
<span data-ttu-id="5920c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5920c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5920c-105">Sucht nach einer angegebenen Eigenschaft in einem Eigenschaftensatz.</span><span class="sxs-lookup"><span data-stu-id="5920c-105">Searches for a specified property in a property set.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5920c-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="5920c-106">Header file:</span></span>  <br/> |<span data-ttu-id="5920c-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="5920c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="5920c-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="5920c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5920c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5920c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5920c-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="5920c-110">Called by:</span></span>  <br/> |<span data-ttu-id="5920c-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="5920c-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSPropValue PpropFindProp(
  LPSPropValue rgprop,
  ULONG cprop,
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="5920c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5920c-112">Parameters</span></span>

 <span data-ttu-id="5920c-113">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="5920c-113">_rgprop_</span></span>
  
> <span data-ttu-id="5920c-114">in Array von [SPropValue](spropvalue.md) -Strukturen, die die zu durchsuchenden Eigenschaften definieren.</span><span class="sxs-lookup"><span data-stu-id="5920c-114">[in] Array of [SPropValue](spropvalue.md) structures that define the properties to be searched.</span></span> 
    
 <span data-ttu-id="5920c-115">_cprop_</span><span class="sxs-lookup"><span data-stu-id="5920c-115">_cprop_</span></span>
  
> <span data-ttu-id="5920c-116">in Die Anzahl der Eigenschaften in dem vom _rgprop_ -Parameter angegebenen Eigenschaftssatz.</span><span class="sxs-lookup"><span data-stu-id="5920c-116">[in] Count of properties in the property set indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="5920c-117">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="5920c-117">_ulPropTag_</span></span>
  
> <span data-ttu-id="5920c-118">in Property-Tag für die Eigenschaft, nach der im durch den _rgprop_ -Parameter angegebenen Eigenschaftensatz gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="5920c-118">[in] Property tag for the property to search for in the property set indicated by the  _rgprop_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5920c-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5920c-119">Return value</span></span>

 <span data-ttu-id="5920c-120">**PpropFindProp** gibt eine [SPropValue](spropvalue.md) -Struktur zurück, die die Eigenschaft definiert, die mit dem Eingabe Eigenschafts übereinstimmt, oder NULL, wenn keine Übereinstimmung vorliegt.</span><span class="sxs-lookup"><span data-stu-id="5920c-120">**PpropFindProp** returns an [SPropValue](spropvalue.md) structure defining the property that matches the input property tag, or NULL if there is no match.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5920c-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5920c-121">Remarks</span></span>

<span data-ttu-id="5920c-122">Wenn das angegebene Property-Tag eine Eigenschaft vom Typ PT_UNSPECIFIED angibt, findet die **PpropFindProp** -Funktion nur eine Übereinstimmung für den Eigenschaftenbezeichner im-Tag.</span><span class="sxs-lookup"><span data-stu-id="5920c-122">If the given property tag indicates a property of type PT_UNSPECIFIED, the **PpropFindProp** function finds a match only for the property identifier in the tag.</span></span> <span data-ttu-id="5920c-123">Andernfalls findet es eine Übereinstimmung für das gesamte Property-Tag, einschließlich des Eigenschaftentyps, und gibt die identifizierte Eigenschaft zurück.</span><span class="sxs-lookup"><span data-stu-id="5920c-123">Otherwise, it finds a match for the entire property tag, including the property type, and returns the property identified.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5920c-124">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="5920c-124">MFCMAPI reference</span></span>

<span data-ttu-id="5920c-125">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="5920c-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5920c-126">**Datei**</span><span class="sxs-lookup"><span data-stu-id="5920c-126">**File**</span></span>|<span data-ttu-id="5920c-127">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="5920c-127">**Function**</span></span>|<span data-ttu-id="5920c-128">**Comment**</span><span class="sxs-lookup"><span data-stu-id="5920c-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5920c-129">ContentsTableListCtrl. cpp</span><span class="sxs-lookup"><span data-stu-id="5920c-129">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="5920c-130">CContentsTableListCtrl:: BuildDataItem</span><span class="sxs-lookup"><span data-stu-id="5920c-130">CContentsTableListCtrl::BuildDataItem</span></span>  <br/> |<span data-ttu-id="5920c-131">MFCMAPI verwendet die **PpropFindProp** -Methode, um Eigenschaften in einem Eigenschaftensatz zu suchen, der der Liste hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="5920c-131">MFCMAPI uses the **PpropFindProp** method to find properties in a property set being added to the list.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5920c-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5920c-132">See also</span></span>



[<span data-ttu-id="5920c-133">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="5920c-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

