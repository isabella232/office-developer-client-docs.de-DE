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
ms.openlocfilehash: abf33e4167d836aeb88fdefb30ba05840e80ce63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791743"
---
# <a name="fpropcontainsprop"></a><span data-ttu-id="1c4fb-103">FPropContainsProp</span><span class="sxs-lookup"><span data-stu-id="1c4fb-103">FPropContainsProp</span></span>

<span data-ttu-id="1c4fb-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1c4fb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1c4fb-105">Vergleicht zwei Eigenschaftswerte, im Allgemeinen Zeichenfolgen oder binäre Arrays, um festzustellen, ob eines der anderen enthält.</span><span class="sxs-lookup"><span data-stu-id="1c4fb-105">Compares two property values, generally strings or binary arrays, to see if one contains the other.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1c4fb-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="1c4fb-106">Header file:</span></span>  <br/> |<span data-ttu-id="1c4fb-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="1c4fb-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="1c4fb-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="1c4fb-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1c4fb-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1c4fb-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1c4fb-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="1c4fb-110">Called by:</span></span>  <br/> |<span data-ttu-id="1c4fb-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="1c4fb-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropContainsProp(
  LPSPropValue lpSPropValueDst,
  LPSPropValue lpSPropValueSrc,
  ULONG ulFuzzyLevel
);
```

## <a name="parameters"></a><span data-ttu-id="1c4fb-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c4fb-112">Parameters</span></span>

<span data-ttu-id="1c4fb-113">_lpSPropValueDst_</span><span class="sxs-lookup"><span data-stu-id="1c4fb-113">_lpSPropValueDst_</span></span>
  
> <span data-ttu-id="1c4fb-114">[in] Zeiger auf eine [SPropValue](spropvalue.md) Struktur definieren den Wert der Eigenschaft, der die zu suchende Zeichenfolge enthalten möglicherweise auf den durch den Parameter _LpSPropValueSrc_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="1c4fb-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the property value that might contain the search string pointed to by the  _lpSPropValueSrc_ parameter.</span></span> 
    
<span data-ttu-id="1c4fb-115">_lpSPropValueSrc_</span><span class="sxs-lookup"><span data-stu-id="1c4fb-115">_lpSPropValueSrc_</span></span>
  
> <span data-ttu-id="1c4fb-116">[in] Zeiger auf eine **SPropValue** -Struktur, die die zu suchende Zeichenfolge, die **FPropContainsProp** Suchvorgänge ist in der Eigenschaftswert, der auf den durch den Parameter _LpSPropValueDst_ definieren.</span><span class="sxs-lookup"><span data-stu-id="1c4fb-116">[in] Pointer to an **SPropValue** structure defining the search string that **FPropContainsProp** is seeking in the property value pointed to by the  _lpSPropValueDst_ parameter.</span></span> 
    
<span data-ttu-id="1c4fb-117">_ulFuzzyLevel_</span><span class="sxs-lookup"><span data-stu-id="1c4fb-117">_ulFuzzyLevel_</span></span>
  
> <span data-ttu-id="1c4fb-118">[in] Optionen definieren die Ebene der Webseitenentwicklung im Vergleich zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="1c4fb-118">[in] Option settings defining the level of preciseness to use in the comparison.</span></span> 

  - <span data-ttu-id="1c4fb-119">Die **unteren 16 Bit** gelten für Eigenschaften vom Typ, PT_BINARY und PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="1c4fb-119">The **lower 16 bits** apply to properties of type PT_BINARY and PT_STRING8.</span></span> <span data-ttu-id="1c4fb-120">Sie müssen auf genau einem der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="1c4fb-120">They must be set to exactly one of the following values:</span></span>
      
    - <span data-ttu-id="1c4fb-121">FL_FULLSTRING: Die _LpSPropValueSrc_ Suchzeichenfolge muss der Wert der Eigenschaft _LpSPropValueDst_identifizierten entsprechen.</span><span class="sxs-lookup"><span data-stu-id="1c4fb-121">FL_FULLSTRING: The  _lpSPropValueSrc_ search string must be equal to the property value identified by  _lpSPropValueDst_.</span></span>
        
    - <span data-ttu-id="1c4fb-122">FL_PREFIX: Die _LpSPropValueSrc_ Suchzeichenfolge muss am Anfang der Wert der Eigenschaft _LpSPropValueDst_identifizierten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="1c4fb-122">FL_PREFIX: The  _lpSPropValueSrc_ search string must appear at the beginning of the property value identified by  _lpSPropValueDst_.</span></span> <span data-ttu-id="1c4fb-123">Die beiden Werte sollten nur bis zur Länge der Suchzeichenfolge angegeben durch _LpSPropValueSrc_verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="1c4fb-123">The two values should be compared only up to the length of the search string indicated by  _lpSPropValueSrc_.</span></span> 
        
    - <span data-ttu-id="1c4fb-124">FL_SUBSTRING: Die _LpSPropValueSrc_ Suchzeichenfolge muss an einer beliebigen Stelle im _LpSPropValueDst_identifizierten-Eigenschaftenwert enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="1c4fb-124">FL_SUBSTRING: The  _lpSPropValueSrc_ search string must be contained anywhere in the property value identified by  _lpSPropValueDst_.</span></span> 
      
  - <span data-ttu-id="1c4fb-125">Die **oberen 16 Bit** gelten nur für Eigenschaften vom Typ PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="1c4fb-125">The **upper 16 bits** apply only to properties of type PT_STRING8.</span></span> <span data-ttu-id="1c4fb-126">Sie können auf die folgenden Werte in beliebiger Kombination festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="1c4fb-126">They can be set to the following values in any combination:</span></span>
    
    - <span data-ttu-id="1c4fb-127">FL_IGNORECASE: Ohne Berücksichtigung der Groß-/Kleinschreibung sollte der Vergleich durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1c4fb-127">FL_IGNORECASE: The comparison should be made without considering case sensitivity.</span></span> 
        
    - <span data-ttu-id="1c4fb-128">FL_IGNORENONSPACE: Der Vergleich sollten definierten Unicode Zeichen ohne Zwischenraum wie diakritischen Zeichen ignorieren.</span><span class="sxs-lookup"><span data-stu-id="1c4fb-128">FL_IGNORENONSPACE: The comparison should ignore Unicode-defined nonspacing characters such as diacritical marks.</span></span> 
        
    - <span data-ttu-id="1c4fb-129">FL_LOOSE: Der Vergleich sollte eine Übereinstimmung nach Möglichkeit ignorieren Fall angeben Empfindlichkeit und Zeichen ohne Zwischenraum.</span><span class="sxs-lookup"><span data-stu-id="1c4fb-129">FL_LOOSE: The comparison should indicate a match whenever possible, ignoring case sensitivity and nonspacing characters.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1c4fb-130">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="1c4fb-130">Return value</span></span>

<span data-ttu-id="1c4fb-131">TRUE</span><span class="sxs-lookup"><span data-stu-id="1c4fb-131">TRUE</span></span> 
  
> <span data-ttu-id="1c4fb-132">Die Parameter gültig sind und die _LpSPropValueSrc_ zu suchende Zeichenfolge enthalten ist der Wert der _LpSPropValueDst_ -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="1c4fb-132">The parameters are all valid and the  _lpSPropValueSrc_ search string is contained as specified in the  _lpSPropValueDst_ property value.</span></span> 
    
<span data-ttu-id="1c4fb-133">FALSE</span><span class="sxs-lookup"><span data-stu-id="1c4fb-133">FALSE</span></span> 
  
> <span data-ttu-id="1c4fb-134">Die verglichenen Eigenschaftswerte sind nicht vom Typ PT_STRING8 oder PT_BINARY, die Eigenschaftswerte werden verschiedene Typen oder nicht enthalten, die zu suchende Zeichenfolge _LpSPropValueSrc_ wie in der Wert der _LpSPropValueDst_ -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="1c4fb-134">The property values being compared are not of type PT_STRING8 or PT_BINARY, the property values are of different types, or the  _lpSPropValueSrc_ search string is not contained as specified in the  _lpSPropValueDst_ property value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1c4fb-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1c4fb-135">Remarks</span></span>

<span data-ttu-id="1c4fb-136">Die Vergleichsmethode hängt davon ab, die in die Definitionen der [SPropValue](spropvalue.md) -Eigenschaft angegebene Eigenschaftentypen und die fuzzy Ebene Heuristik im _UlFuzzyLevel_ -Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="1c4fb-136">The comparison method depends on the property types specified in the [SPropValue](spropvalue.md) property definitions and the fuzzy level heuristic provided in the  _ulFuzzyLevel_ parameter.</span></span> <span data-ttu-id="1c4fb-137">Die Funktionen [FPropCompareProp](fpropcompareprop.md) und **FPropContainsProp** können verwendet werden, um Einschränkungen zum Generieren einer Tabelle vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="1c4fb-137">The [FPropCompareProp](fpropcompareprop.md) and **FPropContainsProp** functions can be used to prepare restrictions for generating a table.</span></span> 
  
<span data-ttu-id="1c4fb-138">Die oberen 16 Bit _UlFuzzyLevel_ werden für den Eigenschaftentyp PT_BINARY ignoriert.</span><span class="sxs-lookup"><span data-stu-id="1c4fb-138">The upper 16 bits of  _ulFuzzyLevel_ are ignored for property type PT_BINARY.</span></span> <span data-ttu-id="1c4fb-139">Wenn die Einstellungen in _UlFuzzyLevel_ fehlt oder ist ungültig sind, wird eine genaue Übereinstimmung Full-Zeichenfolge durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="1c4fb-139">If the settings in  _ulFuzzyLevel_ are missing or invalid, a full-string exact match is performed.</span></span> <span data-ttu-id="1c4fb-140">Weitere Informationen zur Eigenschaft Beschränkung finden Sie unter der Struktur [SContentRestriction](scontentrestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="1c4fb-140">For more information about property containment, see the [SContentRestriction](scontentrestriction.md) structure.</span></span> 
  

