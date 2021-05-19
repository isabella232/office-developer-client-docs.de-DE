---
title: CY-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253223
localization_priority: Normal
ms.assetid: abb27f90-21b4-08cd-6995-9520fbcebd78
description: Gibt einen Währungswert zurück.
ms.openlocfilehash: 65c88d69669e2fa7f708402d9d50dfe035456edb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433556"
---
# <a name="cy-function"></a><span data-ttu-id="2783f-103">CY Function</span><span class="sxs-lookup"><span data-stu-id="2783f-103">CY Function</span></span>

<span data-ttu-id="2783f-104">Gibt einen Währungswert zurück.</span><span class="sxs-lookup"><span data-stu-id="2783f-104">Returns a currency value.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="2783f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2783f-105">Syntax</span></span>

<span data-ttu-id="2783f-106">CY(\*\* *value* \*\*, \*\* *cyID* \*\* )</span><span class="sxs-lookup"><span data-stu-id="2783f-106">CY(\*\* *value* \*\*, \*\* *cyID* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2783f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2783f-107">Parameters</span></span>

|<span data-ttu-id="2783f-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="2783f-108">**Name**</span></span>|<span data-ttu-id="2783f-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="2783f-109">**Required/Optional**</span></span>|<span data-ttu-id="2783f-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="2783f-110">**Data Type**</span></span>|<span data-ttu-id="2783f-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2783f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2783f-112">_value_</span><span class="sxs-lookup"><span data-stu-id="2783f-112">_value_</span></span> <br/> |<span data-ttu-id="2783f-113">Optional.</span><span class="sxs-lookup"><span data-stu-id="2783f-113">Optional</span></span>  <br/> |<span data-ttu-id="2783f-114">**Nummer oder Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2783f-114">**Number or String**</span></span> <br/> |<span data-ttu-id="2783f-115">Eine Zahl oder eine Zeichenfolge, die währungsspezifische Formatierungen enthält.</span><span class="sxs-lookup"><span data-stu-id="2783f-115">A number or a string that includes currency-specific formatting.</span></span> <span data-ttu-id="2783f-116">Wenn dieser Wert nicht angegeben wird, wird der Währungswert gemäß der Währungsformatvorlage in den Einstellungen Region und Sprache des Systems formatiert.</span><span class="sxs-lookup"><span data-stu-id="2783f-116">If not specified, the currency value is formatted according to the currency style in the system's Region and Language settings.</span></span>  <br/> |
| <span data-ttu-id="2783f-117">_cyID_</span><span class="sxs-lookup"><span data-stu-id="2783f-117">_cyID_</span></span> <br/> |<span data-ttu-id="2783f-118">Optional.</span><span class="sxs-lookup"><span data-stu-id="2783f-118">Optional</span></span>  <br/> |<span data-ttu-id="2783f-119">**Number**</span><span class="sxs-lookup"><span data-stu-id="2783f-119">**Number**</span></span> <br/> |<span data-ttu-id="2783f-120">Eine numerische Währungs-ID oder eine zeichenfolge mit drei Zeichen für die ISO 4217-Abkürzung.</span><span class="sxs-lookup"><span data-stu-id="2783f-120">A numeric currency ID or a three-character quoted string for the ISO 4217 abbreviation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2783f-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2783f-121">Remarks</span></span>

<span data-ttu-id="2783f-122">Um eine andere Währung anzugeben, müssen Sie eine gültige _cyID angeben._</span><span class="sxs-lookup"><span data-stu-id="2783f-122">To specify a different currency, you must include a valid  _cyID_.</span></span> <span data-ttu-id="2783f-123">Eine entsprechende Liste finden Sie unter [Informationen zu Währungskonstanten](about-currency-constants.md).</span><span class="sxs-lookup"><span data-stu-id="2783f-123">For a list, see [About currency constants](about-currency-constants.md).</span></span>
  
<span data-ttu-id="2783f-124">Wenn  _der Wert_ mit dem angegebenen Währungstyp nicht kompatibel ist oder wenn ein ungültiges Argument wie "keine Zahl" angegeben wird, wird #VALUE!</span><span class="sxs-lookup"><span data-stu-id="2783f-124">If  _value_ is incompatible with the designated currency type, or if an invalid argument such as "not a number" is specified, a #VALUE!</span></span> <span data-ttu-id="2783f-125">zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2783f-125">error is returned.</span></span> <span data-ttu-id="2783f-126">Wenn  _der_ Wert größer als 922.337.203.685.477,5807 oder kleiner als -922.337.203.685.477,5808 ist, ist #VALUE!</span><span class="sxs-lookup"><span data-stu-id="2783f-126">If  _value_ is greater than 922,337,203,685,477.5807 or less than -922,337,203,685,477.5808, a #VALUE!</span></span> <span data-ttu-id="2783f-127">zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2783f-127">error is returned.</span></span> 
  
<span data-ttu-id="2783f-128">Für eine bessere Genauigkeit bei sehr großen Währungswerten, die Bruchteile einer Einheit enthalten, z. B. 3,6 Billionen, verwenden Sie Zeichenfolgenargumente für  _den Wert_.</span><span class="sxs-lookup"><span data-stu-id="2783f-128">For better precision with very large currency values that include fractions of a unit, such as 3.6 trillion, use string arguments for  _value_.</span></span>
  
<span data-ttu-id="2783f-129">Das Angeben einer ungültigen  _cyID_ gibt einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="2783f-129">Specifying an invalid  _cyID_ returns an error.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="2783f-130">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2783f-130">Example 1</span></span>

<span data-ttu-id="2783f-131">Wenn der Benutzer in den Regions- und Spracheinstellungen US-Dollar festgelegt hat:</span><span class="sxs-lookup"><span data-stu-id="2783f-131">If the user's Region and Language settings specify United States dollars:</span></span>
  
<span data-ttu-id="2783f-132">CY(999998.993)</span><span class="sxs-lookup"><span data-stu-id="2783f-132">CY(999998.993)</span></span>
  
<span data-ttu-id="2783f-133">Gibt $999.998,99 zurück.</span><span class="sxs-lookup"><span data-stu-id="2783f-133">Returns $999,998.99</span></span>
  
## <a name="example-2"></a><span data-ttu-id="2783f-134">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2783f-134">Example 2</span></span>

<span data-ttu-id="2783f-135">CY(12345678,993. "USD")</span><span class="sxs-lookup"><span data-stu-id="2783f-135">CY(12345678.993, "USD")</span></span>
  
<span data-ttu-id="2783f-136">Gibt $12.345.678,99 zurück.</span><span class="sxs-lookup"><span data-stu-id="2783f-136">Returns $12,345,678.99</span></span>
  
## <a name="example-3"></a><span data-ttu-id="2783f-137">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="2783f-137">Example 3</span></span>

<span data-ttu-id="2783f-138">CY(12345678,993. "EUR")</span><span class="sxs-lookup"><span data-stu-id="2783f-138">CY(12345678.993, "DEM")</span></span>
  
<span data-ttu-id="2783f-139">Gibt 12.345.678,99 € zurück.</span><span class="sxs-lookup"><span data-stu-id="2783f-139">Returns 12,345,678.99 DEM</span></span>
  
## <a name="example-4"></a><span data-ttu-id="2783f-140">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="2783f-140">Example 4</span></span>

<span data-ttu-id="2783f-141">CY(12345678,7832. "XXX")</span><span class="sxs-lookup"><span data-stu-id="2783f-141">CY(12345678.7832, "XXX")</span></span>
  
<span data-ttu-id="2783f-142">Gibt 12.345.678,78 zurück.</span><span class="sxs-lookup"><span data-stu-id="2783f-142">Returns 12,345,678.78</span></span>
  

