---
title: FPropContainsProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FPropContainsProp
api_type:
- COM
ms.assetid: 43da5b59-7691-49aa-b83c-753d43bfd8fd
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ea56996ad56bb4ce93d103a75eba2c29e6059a87
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328042"
---
# <a name="fpropcontainsprop"></a><span data-ttu-id="86e5f-103">FPropContainsProp</span><span class="sxs-lookup"><span data-stu-id="86e5f-103">FPropContainsProp</span></span>

<span data-ttu-id="86e5f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="86e5f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="86e5f-105">Vergleicht zwei Eigenschaftswerte, in der Regel Zeichenfolgen oder binäre Arrays, um zu sehen, ob eine die andere enthält.</span><span class="sxs-lookup"><span data-stu-id="86e5f-105">Compares two property values, generally strings or binary arrays, to see if one contains the other.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="86e5f-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="86e5f-106">Header file:</span></span>  <br/> |<span data-ttu-id="86e5f-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="86e5f-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="86e5f-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="86e5f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="86e5f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="86e5f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="86e5f-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="86e5f-110">Called by:</span></span>  <br/> |<span data-ttu-id="86e5f-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="86e5f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropContainsProp(
  LPSPropValue lpSPropValueDst,
  LPSPropValue lpSPropValueSrc,
  ULONG ulFuzzyLevel
);
```

## <a name="parameters"></a><span data-ttu-id="86e5f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="86e5f-112">Parameters</span></span>

<span data-ttu-id="86e5f-113">_lpSPropValueDst_</span><span class="sxs-lookup"><span data-stu-id="86e5f-113">_lpSPropValueDst_</span></span>
  
> <span data-ttu-id="86e5f-114">in Zeiger auf eine [SPropValue](spropvalue.md) -Struktur, die den Eigenschaftswert definiert, der die Suchzeichenfolge enthalten kann, auf die durch den _lpSPropValueSrc_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="86e5f-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the property value that might contain the search string pointed to by the  _lpSPropValueSrc_ parameter.</span></span> 
    
<span data-ttu-id="86e5f-115">_lpSPropValueSrc_</span><span class="sxs-lookup"><span data-stu-id="86e5f-115">_lpSPropValueSrc_</span></span>
  
> <span data-ttu-id="86e5f-116">in Zeiger auf eine **SPropValue** -Struktur, die die Suchzeichenfolge definiert, die **FPropContainsProp** im Eigenschaftswert sucht, der durch den _lpSPropValueDst_ -Parameter verweist.</span><span class="sxs-lookup"><span data-stu-id="86e5f-116">[in] Pointer to an **SPropValue** structure defining the search string that **FPropContainsProp** is seeking in the property value pointed to by the  _lpSPropValueDst_ parameter.</span></span> 
    
<span data-ttu-id="86e5f-117">_ulFuzzyLevel_</span><span class="sxs-lookup"><span data-stu-id="86e5f-117">_ulFuzzyLevel_</span></span>
  
> <span data-ttu-id="86e5f-118">in Optionseinstellungen definieren die Genauigkeitsstufe für den Vergleich.</span><span class="sxs-lookup"><span data-stu-id="86e5f-118">[in] Option settings defining the level of preciseness to use in the comparison.</span></span> 

  - <span data-ttu-id="86e5f-119">Die **unteren 16 Bits** gelten für die Eigenschaften vom Typ PT_BINARY und PT_String8.</span><span class="sxs-lookup"><span data-stu-id="86e5f-119">The **lower 16 bits** apply to properties of type PT_BINARY and PT_STRING8.</span></span> <span data-ttu-id="86e5f-120">Sie müssen auf einen der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="86e5f-120">They must be set to exactly one of the following values:</span></span>
      
    - <span data-ttu-id="86e5f-121">FL_FULLSTRING: die _lpSPropValueSrc_ -Suchzeichenfolge muss dem durch _lpSPropValueDst_angegebenen Eigenschaftswert entsprechen.</span><span class="sxs-lookup"><span data-stu-id="86e5f-121">FL_FULLSTRING: The  _lpSPropValueSrc_ search string must be equal to the property value identified by  _lpSPropValueDst_.</span></span>
        
    - <span data-ttu-id="86e5f-122">FL_PREFIX: die _lpSPropValueSrc_ -Suchzeichenfolge muss am Anfang des durch _lpSPropValueDst_angegebenen Eigenschaftswerts angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="86e5f-122">FL_PREFIX: The  _lpSPropValueSrc_ search string must appear at the beginning of the property value identified by  _lpSPropValueDst_.</span></span> <span data-ttu-id="86e5f-123">Die beiden Werte sollten nur bis zur Länge der durch _lpSPropValueSrc_angegebenen Suchzeichenfolge verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="86e5f-123">The two values should be compared only up to the length of the search string indicated by  _lpSPropValueSrc_.</span></span> 
        
    - <span data-ttu-id="86e5f-124">FL_SUBSTRING: die _lpSPropValueSrc_ -Suchzeichenfolge muss an beliebiger Stelle im von _lpSPropValueDst_angegebenen Eigenschaftswert enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="86e5f-124">FL_SUBSTRING: The  _lpSPropValueSrc_ search string must be contained anywhere in the property value identified by  _lpSPropValueDst_.</span></span> 
      
  - <span data-ttu-id="86e5f-125">Die **oberen 16 Bits** gelten nur für Eigenschaften vom Typ PT_String8.</span><span class="sxs-lookup"><span data-stu-id="86e5f-125">The **upper 16 bits** apply only to properties of type PT_STRING8.</span></span> <span data-ttu-id="86e5f-126">Sie können in einer beliebigen Kombination auf die folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="86e5f-126">They can be set to the following values in any combination:</span></span>
    
    - <span data-ttu-id="86e5f-127">FL_IGNORECASE: der Vergleich sollte ohne Berücksichtigung der Groß-/Kleinschreibung vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="86e5f-127">FL_IGNORECASE: The comparison should be made without considering case sensitivity.</span></span> 
        
    - <span data-ttu-id="86e5f-128">FL_IGNORENONSPACE: der Vergleich sollte Unicode-definierte Zeichen, die nicht im Abstand stehen, wie diakritische Marken, ignorieren.</span><span class="sxs-lookup"><span data-stu-id="86e5f-128">FL_IGNORENONSPACE: The comparison should ignore Unicode-defined nonspacing characters such as diacritical marks.</span></span> 
        
    - <span data-ttu-id="86e5f-129">FL_LOOSE: der Vergleich sollte nach Möglichkeit eine Übereinstimmung aufweisen, wobei die Groß-/Kleinschreibung und die Zeichen ohne Abstand ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="86e5f-129">FL_LOOSE: The comparison should indicate a match whenever possible, ignoring case sensitivity and nonspacing characters.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="86e5f-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="86e5f-130">Return value</span></span>

<span data-ttu-id="86e5f-131">TRUE</span><span class="sxs-lookup"><span data-stu-id="86e5f-131">TRUE</span></span> 
  
> <span data-ttu-id="86e5f-132">Die Parameter sind alle gültig, und die _lpSPropValueSrc_ -Suchzeichenfolge ist im Wert der _lpSPropValueDst_ -Eigenschaft enthalten.</span><span class="sxs-lookup"><span data-stu-id="86e5f-132">The parameters are all valid and the  _lpSPropValueSrc_ search string is contained as specified in the  _lpSPropValueDst_ property value.</span></span> 
    
<span data-ttu-id="86e5f-133">FALSE</span><span class="sxs-lookup"><span data-stu-id="86e5f-133">FALSE</span></span> 
  
> <span data-ttu-id="86e5f-134">Die verglichenen Eigenschaftswerte sind nicht vom Typ PT_STRING8 oder PT_BINARY, die Eigenschaftswerte sind unterschiedlichen Typen, oder die _lpSPropValueSrc_ -Suchzeichenfolge ist nicht wie im Wert der _lpSPropValueDst_ -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="86e5f-134">The property values being compared are not of type PT_STRING8 or PT_BINARY, the property values are of different types, or the  _lpSPropValueSrc_ search string is not contained as specified in the  _lpSPropValueDst_ property value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="86e5f-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="86e5f-135">Remarks</span></span>

<span data-ttu-id="86e5f-136">Die Vergleichsmethode hängt von den Eigenschaftentypen ab, die in den [SPropValue](spropvalue.md) -Eigenschaftsdefinitionen und der heuristischen Heuristik im _ulFuzzyLevel_ -Parameter angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="86e5f-136">The comparison method depends on the property types specified in the [SPropValue](spropvalue.md) property definitions and the fuzzy level heuristic provided in the  _ulFuzzyLevel_ parameter.</span></span> <span data-ttu-id="86e5f-137">Die [FPropCompareProp](fpropcompareprop.md) -und **FPropContainsProp** -Funktionen können verwendet werden, um Einschränkungen für das Generieren einer Tabelle vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="86e5f-137">The [FPropCompareProp](fpropcompareprop.md) and **FPropContainsProp** functions can be used to prepare restrictions for generating a table.</span></span> 
  
<span data-ttu-id="86e5f-138">Die oberen 16 Bits von _ulFuzzyLevel_ werden für den Eigenschaftentyp PT_BINARY ignoriert.</span><span class="sxs-lookup"><span data-stu-id="86e5f-138">The upper 16 bits of  _ulFuzzyLevel_ are ignored for property type PT_BINARY.</span></span> <span data-ttu-id="86e5f-139">Wenn die Einstellungen in _ulFuzzyLevel_ fehlen oder ungültig sind, wird eine exakte Übereinstimmung mit vollständiger Zeichenfolge ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="86e5f-139">If the settings in  _ulFuzzyLevel_ are missing or invalid, a full-string exact match is performed.</span></span> <span data-ttu-id="86e5f-140">Weitere Informationen zur Eigenschafts Kapselung finden Sie in der [SContentRestriction](scontentrestriction.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="86e5f-140">For more information about property containment, see the [SContentRestriction](scontentrestriction.md) structure.</span></span> 
  

