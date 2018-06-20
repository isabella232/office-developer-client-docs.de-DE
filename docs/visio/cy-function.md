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
ms.openlocfilehash: ea7696e7628939466730b9c054a706a7a9fa264e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796759"
---
# <a name="cy-function"></a><span data-ttu-id="daa7e-103">CY Function</span><span class="sxs-lookup"><span data-stu-id="daa7e-103">CY Function</span></span>

<span data-ttu-id="daa7e-104">Gibt einen Währungswert zurück.</span><span class="sxs-lookup"><span data-stu-id="daa7e-104">Returns a currency value.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="daa7e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="daa7e-105">Syntax</span></span>

<span data-ttu-id="daa7e-106">CY (** *Wert* **, ** *CyID* **)</span><span class="sxs-lookup"><span data-stu-id="daa7e-106">CY(** *value* **, ** *cyID* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="daa7e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="daa7e-107">Parameters</span></span>

|<span data-ttu-id="daa7e-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="daa7e-108">**Name**</span></span>|<span data-ttu-id="daa7e-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="daa7e-109">**Required/Optional**</span></span>|<span data-ttu-id="daa7e-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="daa7e-110">**Data Type**</span></span>|<span data-ttu-id="daa7e-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="daa7e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="daa7e-112">_Value_</span><span class="sxs-lookup"><span data-stu-id="daa7e-112">_value_</span></span> <br/> |<span data-ttu-id="daa7e-113">Optional</span><span class="sxs-lookup"><span data-stu-id="daa7e-113">Optional</span></span>  <br/> |<span data-ttu-id="daa7e-114">**Zahl oder eine Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="daa7e-114">**Number or String**</span></span> <br/> |<span data-ttu-id="daa7e-115">Eine Zahl oder eine Zeichenfolge, die Währung-spezifischen Formatierung enthält.</span><span class="sxs-lookup"><span data-stu-id="daa7e-115">A number or a string that includes currency-specific formatting.</span></span> <span data-ttu-id="daa7e-116">Wenn nicht angegeben, wird der Währungswert entsprechend das Währungsformat in die Standardeinstellungen des Systems Region und Sprache formatiert.</span><span class="sxs-lookup"><span data-stu-id="daa7e-116">If not specified, the currency value is formatted according to the currency style in the system's Region and Language settings.</span></span>  <br/> |
| <span data-ttu-id="daa7e-117">_cyID_</span><span class="sxs-lookup"><span data-stu-id="daa7e-117">_cyID_</span></span> <br/> |<span data-ttu-id="daa7e-118">Optional</span><span class="sxs-lookup"><span data-stu-id="daa7e-118">Optional</span></span>  <br/> |<span data-ttu-id="daa7e-119">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="daa7e-119">**Number**</span></span> <br/> |<span data-ttu-id="daa7e-120">Eine numerische Währung-ID oder eine Zeichenfolge mit drei Zeichen in Anführungszeichen für die Abkürzung ISO 4217.</span><span class="sxs-lookup"><span data-stu-id="daa7e-120">A numeric currency ID or a three-character quoted string for the ISO 4217 abbreviation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="daa7e-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="daa7e-121">Remarks</span></span>

<span data-ttu-id="daa7e-122">Um eine andere Währung angeben, müssen Sie eine gültige _CyID_einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="daa7e-122">To specify a different currency, you must include a valid  _cyID_.</span></span> <span data-ttu-id="daa7e-123">Eine Liste finden Sie unter [About Currency-Konstanten](about-currency-constants.md).</span><span class="sxs-lookup"><span data-stu-id="daa7e-123">For a list, see [About currency constants](about-currency-constants.md).</span></span>
  
<span data-ttu-id="daa7e-124">Wenn der _Wert_ nicht kompatibel mit dem angegebenen Währungstyp ist oder wenn ein ungültiges Argument wie "keine Zahl" angegeben ist, wird ein #VALUE!</span><span class="sxs-lookup"><span data-stu-id="daa7e-124">If  _value_ is incompatible with the designated currency type, or if an invalid argument such as "not a number" is specified, a #VALUE!</span></span> <span data-ttu-id="daa7e-125">Fehler wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="daa7e-125">error is returned.</span></span> <span data-ttu-id="daa7e-126">Wenn der _Wert größer als 922,337,203,685,477.5807 oder kleiner als -922.337.203.685.477,5808 ist, wird ein #VALUE!_</span><span class="sxs-lookup"><span data-stu-id="daa7e-126">If  _value_ is greater than 922,337,203,685,477.5807 or less than -922,337,203,685,477.5808, a #VALUE!</span></span> <span data-ttu-id="daa7e-127">Fehler wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="daa7e-127">error is returned.</span></span> 
  
<span data-ttu-id="daa7e-128">Verwenden Sie für eine bessere Genauigkeit mit sehr großen Währungswerten mit Bruchzahlangaben für eine Einheit wie 3.6 Billionen, Zeichenfolge-Argumente _Wert_.</span><span class="sxs-lookup"><span data-stu-id="daa7e-128">For better precision with very large currency values that include fractions of a unit, such as 3.6 trillion, use string arguments for  _value_.</span></span>
  
<span data-ttu-id="daa7e-129">Angabe einer ungültigen _CyID_ wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="daa7e-129">Specifying an invalid  _cyID_ returns an error.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="daa7e-130">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="daa7e-130">Example 1</span></span>

<span data-ttu-id="daa7e-131">Wenn der Benutzer in den Regions- und Spracheinstellungen US-Dollar festgelegt hat:</span><span class="sxs-lookup"><span data-stu-id="daa7e-131">If the user's Region and Language settings specify United States dollars:</span></span>
  
<span data-ttu-id="daa7e-132">CY(999998.993)</span><span class="sxs-lookup"><span data-stu-id="daa7e-132">CY(999998.993)</span></span>
  
<span data-ttu-id="daa7e-133">Gibt $999.998,99 zurück.</span><span class="sxs-lookup"><span data-stu-id="daa7e-133">Returns $999,998.99</span></span>
  
## <a name="example-2"></a><span data-ttu-id="daa7e-134">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="daa7e-134">Example 2</span></span>

<span data-ttu-id="daa7e-135">CY(12345678,993. "USD")</span><span class="sxs-lookup"><span data-stu-id="daa7e-135">CY(12345678.993, "USD")</span></span>
  
<span data-ttu-id="daa7e-136">Gibt $12.345.678,99 zurück.</span><span class="sxs-lookup"><span data-stu-id="daa7e-136">Returns $12,345,678.99</span></span>
  
## <a name="example-3"></a><span data-ttu-id="daa7e-137">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="daa7e-137">Example 3</span></span>

<span data-ttu-id="daa7e-138">CY(12345678,993. "EUR")</span><span class="sxs-lookup"><span data-stu-id="daa7e-138">CY(12345678.993, "DEM")</span></span>
  
<span data-ttu-id="daa7e-139">Gibt 12.345.678,99 € zurück.</span><span class="sxs-lookup"><span data-stu-id="daa7e-139">Returns 12,345,678.99 DEM</span></span>
  
## <a name="example-4"></a><span data-ttu-id="daa7e-140">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="daa7e-140">Example 4</span></span>

<span data-ttu-id="daa7e-141">CY(12345678,7832. "XXX")</span><span class="sxs-lookup"><span data-stu-id="daa7e-141">CY(12345678.7832, "XXX")</span></span>
  
<span data-ttu-id="daa7e-142">Gibt 12.345.678,78 zurück.</span><span class="sxs-lookup"><span data-stu-id="daa7e-142">Returns 12,345,678.78</span></span>
  

