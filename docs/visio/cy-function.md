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
description: Gibt einen Currency-Wert zurück.
ms.openlocfilehash: 65c88d69669e2fa7f708402d9d50dfe035456edb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433556"
---
# <a name="cy-function"></a><span data-ttu-id="624f5-103">CY Function</span><span class="sxs-lookup"><span data-stu-id="624f5-103">CY Function</span></span>

<span data-ttu-id="624f5-104">Gibt einen Currency-Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="624f5-104">Returns a currency value.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="624f5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="624f5-105">Syntax</span></span>

<span data-ttu-id="624f5-106">CY (\* \* *Wert* \* \*, \* \* *cyID* \* \*)</span><span class="sxs-lookup"><span data-stu-id="624f5-106">CY(\*\* *value* \*\*, \*\* *cyID* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="624f5-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="624f5-107">Parameters</span></span>

|<span data-ttu-id="624f5-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="624f5-108">**Name**</span></span>|<span data-ttu-id="624f5-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="624f5-109">**Required/Optional**</span></span>|<span data-ttu-id="624f5-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="624f5-110">**Data Type**</span></span>|<span data-ttu-id="624f5-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="624f5-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="624f5-112">_value_</span><span class="sxs-lookup"><span data-stu-id="624f5-112">_value_</span></span> <br/> |<span data-ttu-id="624f5-113">Optional</span><span class="sxs-lookup"><span data-stu-id="624f5-113">Optional</span></span>  <br/> |<span data-ttu-id="624f5-114">**Nummer oder Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="624f5-114">**Number or String**</span></span> <br/> |<span data-ttu-id="624f5-115">Eine Zahl oder eine Zeichenfolge, die währungsspezifische Formatierung enthält.</span><span class="sxs-lookup"><span data-stu-id="624f5-115">A number or a string that includes currency-specific formatting.</span></span> <span data-ttu-id="624f5-116">Wenn dieser Parameter nicht angegeben wird, wird der Währungswert entsprechend dem Währungsformat in der Region und den Spracheinstellungen des Systems formatiert.</span><span class="sxs-lookup"><span data-stu-id="624f5-116">If not specified, the currency value is formatted according to the currency style in the system's Region and Language settings.</span></span>  <br/> |
| <span data-ttu-id="624f5-117">_cyID_</span><span class="sxs-lookup"><span data-stu-id="624f5-117">_cyID_</span></span> <br/> |<span data-ttu-id="624f5-118">Optional</span><span class="sxs-lookup"><span data-stu-id="624f5-118">Optional</span></span>  <br/> |<span data-ttu-id="624f5-119">**Number**</span><span class="sxs-lookup"><span data-stu-id="624f5-119">**Number**</span></span> <br/> |<span data-ttu-id="624f5-120">Eine numerische Währungs-ID oder eine aus drei Zeichen bestehende Zeichenfolge für die ISO 4217-Abkürzung.</span><span class="sxs-lookup"><span data-stu-id="624f5-120">A numeric currency ID or a three-character quoted string for the ISO 4217 abbreviation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="624f5-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="624f5-121">Remarks</span></span>

<span data-ttu-id="624f5-122">Wenn Sie eine andere Währung angeben möchten, müssen Sie eine gültige _cyID_einfügen.</span><span class="sxs-lookup"><span data-stu-id="624f5-122">To specify a different currency, you must include a valid  _cyID_.</span></span> <span data-ttu-id="624f5-123">Eine entsprechende Liste finden Sie unter [Informationen zu Währungskonstanten](about-currency-constants.md).</span><span class="sxs-lookup"><span data-stu-id="624f5-123">For a list, see [About currency constants](about-currency-constants.md).</span></span>
  
<span data-ttu-id="624f5-124">Wenn der _Wert_ mit dem angegebenen Währungstyp nicht kompatibel ist oder wenn ein ungültiges Argument wie "not a Number" angegeben ist, wird ein #VALUE!</span><span class="sxs-lookup"><span data-stu-id="624f5-124">If  _value_ is incompatible with the designated currency type, or if an invalid argument such as "not a number" is specified, a #VALUE!</span></span> <span data-ttu-id="624f5-125">zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="624f5-125">error is returned.</span></span> <span data-ttu-id="624f5-126">Wenn der _Wert_ größer als 922.337.203.685.477,5807 oder kleiner als-922.337.203.685.477,5808 ist, wird ein #VALUE!</span><span class="sxs-lookup"><span data-stu-id="624f5-126">If  _value_ is greater than 922,337,203,685,477.5807 or less than -922,337,203,685,477.5808, a #VALUE!</span></span> <span data-ttu-id="624f5-127">zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="624f5-127">error is returned.</span></span> 
  
<span data-ttu-id="624f5-128">Zur besseren Genauigkeit bei sehr großen Währungswerten, die Brüche einer Einheit wie 3,6 Billionen, verwenden Sie String-Argumente für _value_.</span><span class="sxs-lookup"><span data-stu-id="624f5-128">For better precision with very large currency values that include fractions of a unit, such as 3.6 trillion, use string arguments for  _value_.</span></span>
  
<span data-ttu-id="624f5-129">Durch Angeben eines ungültigen _cyID_ wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="624f5-129">Specifying an invalid  _cyID_ returns an error.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="624f5-130">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="624f5-130">Example 1</span></span>

<span data-ttu-id="624f5-131">Wenn der Benutzer in den Regions- und Spracheinstellungen US-Dollar festgelegt hat:</span><span class="sxs-lookup"><span data-stu-id="624f5-131">If the user's Region and Language settings specify United States dollars:</span></span>
  
<span data-ttu-id="624f5-132">CY (999998.993)</span><span class="sxs-lookup"><span data-stu-id="624f5-132">CY(999998.993)</span></span>
  
<span data-ttu-id="624f5-133">Gibt $999.998,99 zurück.</span><span class="sxs-lookup"><span data-stu-id="624f5-133">Returns $999,998.99</span></span>
  
## <a name="example-2"></a><span data-ttu-id="624f5-134">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="624f5-134">Example 2</span></span>

<span data-ttu-id="624f5-135">CY(12345678,993. "USD")</span><span class="sxs-lookup"><span data-stu-id="624f5-135">CY(12345678.993, "USD")</span></span>
  
<span data-ttu-id="624f5-136">Gibt $12.345.678,99 zurück.</span><span class="sxs-lookup"><span data-stu-id="624f5-136">Returns $12,345,678.99</span></span>
  
## <a name="example-3"></a><span data-ttu-id="624f5-137">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="624f5-137">Example 3</span></span>

<span data-ttu-id="624f5-138">CY(12345678,993. "EUR")</span><span class="sxs-lookup"><span data-stu-id="624f5-138">CY(12345678.993, "DEM")</span></span>
  
<span data-ttu-id="624f5-139">Gibt 12.345.678,99 € zurück.</span><span class="sxs-lookup"><span data-stu-id="624f5-139">Returns 12,345,678.99 DEM</span></span>
  
## <a name="example-4"></a><span data-ttu-id="624f5-140">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="624f5-140">Example 4</span></span>

<span data-ttu-id="624f5-141">CY(12345678,7832. "XXX")</span><span class="sxs-lookup"><span data-stu-id="624f5-141">CY(12345678.7832, "XXX")</span></span>
  
<span data-ttu-id="624f5-142">Gibt 12.345.678,78 zurück.</span><span class="sxs-lookup"><span data-stu-id="624f5-142">Returns 12,345,678.78</span></span>
  

