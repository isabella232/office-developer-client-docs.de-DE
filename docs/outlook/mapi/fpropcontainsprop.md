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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ea56996ad56bb4ce93d103a75eba2c29e6059a87
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432631"
---
# <a name="fpropcontainsprop"></a><span data-ttu-id="aa437-103">FPropContainsProp</span><span class="sxs-lookup"><span data-stu-id="aa437-103">FPropContainsProp</span></span>

<span data-ttu-id="aa437-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aa437-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aa437-105">Vergleicht zwei Eigenschaftswerte, in der Regel Zeichenfolgen oder binäre Arrays, um zu sehen, ob einer den anderen enthält.</span><span class="sxs-lookup"><span data-stu-id="aa437-105">Compares two property values, generally strings or binary arrays, to see if one contains the other.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="aa437-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="aa437-106">Header file:</span></span>  <br/> |<span data-ttu-id="aa437-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="aa437-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="aa437-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="aa437-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="aa437-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="aa437-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="aa437-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="aa437-110">Called by:</span></span>  <br/> |<span data-ttu-id="aa437-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="aa437-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropContainsProp(
  LPSPropValue lpSPropValueDst,
  LPSPropValue lpSPropValueSrc,
  ULONG ulFuzzyLevel
);
```

## <a name="parameters"></a><span data-ttu-id="aa437-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa437-112">Parameters</span></span>

<span data-ttu-id="aa437-113">_lpSPropValueDst_</span><span class="sxs-lookup"><span data-stu-id="aa437-113">_lpSPropValueDst_</span></span>
  
> <span data-ttu-id="aa437-114">[in] Zeiger auf eine [SPropValue-Struktur,](spropvalue.md) die den Eigenschaftswert definiert, der die Suchzeichenfolge enthalten kann, auf die der  _lpSPropValueSrc-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="aa437-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the property value that might contain the search string pointed to by the  _lpSPropValueSrc_ parameter.</span></span> 
    
<span data-ttu-id="aa437-115">_lpSPropValueSrc_</span><span class="sxs-lookup"><span data-stu-id="aa437-115">_lpSPropValueSrc_</span></span>
  
> <span data-ttu-id="aa437-116">[in] Zeiger auf eine **SPropValue-Struktur,** die die Suchzeichenfolge definiert, die **FPropContainsProp** in dem Eigenschaftswert sucht, auf den der  _lpSPropValueDst-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="aa437-116">[in] Pointer to an **SPropValue** structure defining the search string that **FPropContainsProp** is seeking in the property value pointed to by the  _lpSPropValueDst_ parameter.</span></span> 
    
<span data-ttu-id="aa437-117">_ulFuzzyLevel_</span><span class="sxs-lookup"><span data-stu-id="aa437-117">_ulFuzzyLevel_</span></span>
  
> <span data-ttu-id="aa437-118">[in] Optionseinstellungen, die die im Vergleich zu verwendende Präzisionsstufe definieren.</span><span class="sxs-lookup"><span data-stu-id="aa437-118">[in] Option settings defining the level of preciseness to use in the comparison.</span></span> 

  - <span data-ttu-id="aa437-119">Die **unteren 16 Bit** gelten für Eigenschaften vom Typ PT_BINARY und PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="aa437-119">The **lower 16 bits** apply to properties of type PT_BINARY and PT_STRING8.</span></span> <span data-ttu-id="aa437-120">Sie müssen auf genau einen der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="aa437-120">They must be set to exactly one of the following values:</span></span>
      
    - <span data-ttu-id="aa437-121">FL_FULLSTRING: Die _lpSPropValueSrc-Suchzeichenfolge_ muss gleich dem Eigenschaftswert sein, der von _lpSPropValueDst identifiziert wird._</span><span class="sxs-lookup"><span data-stu-id="aa437-121">FL_FULLSTRING: The  _lpSPropValueSrc_ search string must be equal to the property value identified by  _lpSPropValueDst_.</span></span>
        
    - <span data-ttu-id="aa437-122">FL_PREFIX: Die _lpSPropValueSrc-Suchzeichenfolge_ muss am Anfang des durch _lpSPropValueDst identifizierten Eigenschaftswerts angezeigt werden._</span><span class="sxs-lookup"><span data-stu-id="aa437-122">FL_PREFIX: The  _lpSPropValueSrc_ search string must appear at the beginning of the property value identified by  _lpSPropValueDst_.</span></span> <span data-ttu-id="aa437-123">Die beiden Werte sollten nur bis zur Länge der suchzeichenfolge verglichen werden, die von _lpSPropValueSrc angegeben wird._</span><span class="sxs-lookup"><span data-stu-id="aa437-123">The two values should be compared only up to the length of the search string indicated by  _lpSPropValueSrc_.</span></span> 
        
    - <span data-ttu-id="aa437-124">FL_SUBSTRING: Die _lpSPropValueSrc-Suchzeichenfolge_ muss an einer beliebigen Stelle im Eigenschaftswert enthalten sein, der von _lpSPropValueDst identifiziert wird._</span><span class="sxs-lookup"><span data-stu-id="aa437-124">FL_SUBSTRING: The  _lpSPropValueSrc_ search string must be contained anywhere in the property value identified by  _lpSPropValueDst_.</span></span> 
      
  - <span data-ttu-id="aa437-125">Die **oberen 16 Bit gelten** nur für Eigenschaften vom Typ PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="aa437-125">The **upper 16 bits** apply only to properties of type PT_STRING8.</span></span> <span data-ttu-id="aa437-126">Sie können in beliebiger Kombination auf die folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="aa437-126">They can be set to the following values in any combination:</span></span>
    
    - <span data-ttu-id="aa437-127">FL_IGNORECASE: Der Vergleich sollte ohne Berücksichtigung der Fallempfindlichkeit vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="aa437-127">FL_IGNORECASE: The comparison should be made without considering case sensitivity.</span></span> 
        
    - <span data-ttu-id="aa437-128">FL_IGNORENONSPACE: Der Vergleich sollte Unicode-definierte Zeichen ohne Abstand ignorieren, z. B. diakritische Zeichen.</span><span class="sxs-lookup"><span data-stu-id="aa437-128">FL_IGNORENONSPACE: The comparison should ignore Unicode-defined nonspacing characters such as diacritical marks.</span></span> 
        
    - <span data-ttu-id="aa437-129">FL_LOOSE: Der Vergleich sollte nach Möglichkeit eine Übereinstimmung angeben, wobei die Zwischenfallempfindlichkeit und zeichenfreier Abstand ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="aa437-129">FL_LOOSE: The comparison should indicate a match whenever possible, ignoring case sensitivity and nonspacing characters.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="aa437-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aa437-130">Return value</span></span>

<span data-ttu-id="aa437-131">TRUE</span><span class="sxs-lookup"><span data-stu-id="aa437-131">TRUE</span></span> 
  
> <span data-ttu-id="aa437-132">Die Parameter sind alle gültig, und die  _lpSPropValueSrc-Suchzeichenfolge_ ist wie im  _lpSPropValueDst-Eigenschaftswert_ angegeben enthalten.</span><span class="sxs-lookup"><span data-stu-id="aa437-132">The parameters are all valid and the  _lpSPropValueSrc_ search string is contained as specified in the  _lpSPropValueDst_ property value.</span></span> 
    
<span data-ttu-id="aa437-133">FALSE</span><span class="sxs-lookup"><span data-stu-id="aa437-133">FALSE</span></span> 
  
> <span data-ttu-id="aa437-134">Die zu vergleichenden Eigenschaftswerte sind nicht vom Typ PT_STRING8 oder PT_BINARY, die Eigenschaftswerte sind unterschiedliche Typen, oder die  _lpSPropValueSrc-Suchzeichenfolge_ ist nicht wie im  _lpSPropValueDst-Eigenschaftswert_ angegeben enthalten.</span><span class="sxs-lookup"><span data-stu-id="aa437-134">The property values being compared are not of type PT_STRING8 or PT_BINARY, the property values are of different types, or the  _lpSPropValueSrc_ search string is not contained as specified in the  _lpSPropValueDst_ property value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="aa437-135">Hinweise</span><span class="sxs-lookup"><span data-stu-id="aa437-135">Remarks</span></span>

<span data-ttu-id="aa437-136">Die Vergleichsmethode hängt von den in den [SPropValue-Eigenschaftsdefinitionen](spropvalue.md) angegebenen Eigenschaftstypen und der im  _ulFuzzyLevel-Parameter_ bereitgestellten Heuristik auf Fuzzyebene ab.</span><span class="sxs-lookup"><span data-stu-id="aa437-136">The comparison method depends on the property types specified in the [SPropValue](spropvalue.md) property definitions and the fuzzy level heuristic provided in the  _ulFuzzyLevel_ parameter.</span></span> <span data-ttu-id="aa437-137">Die [Funktionen FPropCompareProp](fpropcompareprop.md) und **FPropContainsProp** können verwendet werden, um Einschränkungen für das Generieren einer Tabelle vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="aa437-137">The [FPropCompareProp](fpropcompareprop.md) and **FPropContainsProp** functions can be used to prepare restrictions for generating a table.</span></span> 
  
<span data-ttu-id="aa437-138">Die oberen 16 Bits von  _ulFuzzyLevel_ werden für Eigenschaftentyptypen PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="aa437-138">The upper 16 bits of  _ulFuzzyLevel_ are ignored for property type PT_BINARY.</span></span> <span data-ttu-id="aa437-139">Wenn die Einstellungen in  _ulFuzzyLevel_ fehlen oder ungültig sind, wird eine genaue Übereinstimmung mit der vollständigen Zeichenfolge ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aa437-139">If the settings in  _ulFuzzyLevel_ are missing or invalid, a full-string exact match is performed.</span></span> <span data-ttu-id="aa437-140">Weitere Informationen zum Eindämmung von Eigenschaften finden Sie in der [SContentRestriction-Struktur.](scontentrestriction.md)</span><span class="sxs-lookup"><span data-stu-id="aa437-140">For more information about property containment, see the [SContentRestriction](scontentrestriction.md) structure.</span></span> 
  

