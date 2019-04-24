---
title: FORMATEX-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251590
localization_priority: Normal
ms.assetid: d375c971-fee2-baa3-dc4f-a26018e70e8a
description: Gibt das Ergebnis des in srcUnit ausgewerteten Ausdrucks als eine Zeichenfolge zurück, die gemäß dem in dstUnit-Format formatiert ist.
ms.openlocfilehash: e341cbcb16cc273f0413f98c195f77ad08946ab1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328630"
---
# <a name="formatex-function"></a><span data-ttu-id="3ace2-103">FORMATEX Function</span><span class="sxs-lookup"><span data-stu-id="3ace2-103">FORMATEX Function</span></span>

<span data-ttu-id="3ace2-104">Gibt das Ergebnis des in srcUnit ausgewerteten Ausdrucks als eine Zeichenfolge zurück, die gemäß dem in dstUnit-Format formatiert ist.</span><span class="sxs-lookup"><span data-stu-id="3ace2-104">Returns the result of expression evaluated in srcUnit as a string formatted according to format expressed in dstUnit.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="3ace2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3ace2-105">Syntax</span></span>

<span data-ttu-id="3ace2-106">FORMATEX (\* \* *Expression* \* *, "* \* *Format* \* *", [* \* *srcUnit* \* *], [* \* *dstUnit* \* *]; [* \* \*\* \* \* \*\*</span><span class="sxs-lookup"><span data-stu-id="3ace2-106">FORMATEX(\*\* *expression* \*\*," \*\* *format* \*\* ",[ \*\* *srcUnit* \*\* ],[ \*\* *dstUnit* \*\* ],[ \*\* *langID* \*\* ][, \*\* *calID* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3ace2-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="3ace2-107">Parameters</span></span>

|<span data-ttu-id="3ace2-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="3ace2-108">**Name**</span></span>|<span data-ttu-id="3ace2-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="3ace2-109">**Required/Optional**</span></span>|<span data-ttu-id="3ace2-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="3ace2-110">**Data Type**</span></span>|<span data-ttu-id="3ace2-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3ace2-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3ace2-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="3ace2-112">_expression_</span></span> <br/> |<span data-ttu-id="3ace2-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="3ace2-113">Required</span></span>  <br/> |<span data-ttu-id="3ace2-114">**String**</span><span class="sxs-lookup"><span data-stu-id="3ace2-114">**String**</span></span> <br/> |<span data-ttu-id="3ace2-115">Eine Kombination aus Konstanten, Operatoren, Funktionen und Bezügen auf ShapeSheet-Zellen, die einen Wert ergeben.</span><span class="sxs-lookup"><span data-stu-id="3ace2-115">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value.</span></span>  <br/> |
| <span data-ttu-id="3ace2-116">_format_</span><span class="sxs-lookup"><span data-stu-id="3ace2-116">_format_</span></span> <br/> |<span data-ttu-id="3ace2-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="3ace2-117">Required</span></span>  <br/> |<span data-ttu-id="3ace2-118">**String**</span><span class="sxs-lookup"><span data-stu-id="3ace2-118">**String**</span></span> <br/> |<span data-ttu-id="3ace2-119">Das zum Formatieren der Zeichenfolge verwendete Format Bild.</span><span class="sxs-lookup"><span data-stu-id="3ace2-119">The format picture used to format the string.</span></span> <span data-ttu-id="3ace2-120">Weitere Informationen zum Formatieren von Bildern finden Sie unter Informationen [zum Formatieren von Bildern](about-format-pictures.md).</span><span class="sxs-lookup"><span data-stu-id="3ace2-120">For more information about format pictures, see [About Format Pictures](about-format-pictures.md).</span></span>  <br/> |
| <span data-ttu-id="3ace2-121">_srcUnit_</span><span class="sxs-lookup"><span data-stu-id="3ace2-121">_srcUnit_</span></span> <br/> |<span data-ttu-id="3ace2-122">Optional</span><span class="sxs-lookup"><span data-stu-id="3ace2-122">Optional</span></span>  <br/> |<span data-ttu-id="3ace2-123">**String**</span><span class="sxs-lookup"><span data-stu-id="3ace2-123">**String**</span></span> <br/> | <span data-ttu-id="3ace2-124">Einheiten zum Auswerten von expression (in, cm usw.).</span><span class="sxs-lookup"><span data-stu-id="3ace2-124">Units used to evaluate expression (in, cm, and so forth).</span></span>  <br/> |
| <span data-ttu-id="3ace2-125">_dstUnit_</span><span class="sxs-lookup"><span data-stu-id="3ace2-125">_dstUnit_</span></span> <br/> |<span data-ttu-id="3ace2-126">Optional</span><span class="sxs-lookup"><span data-stu-id="3ace2-126">Optional</span></span>  <br/> |<span data-ttu-id="3ace2-127">**String**</span><span class="sxs-lookup"><span data-stu-id="3ace2-127">**String**</span></span> <br/> |<span data-ttu-id="3ace2-128">Einheiten, die für das Ergebnis von expression verwendet werden sollen (in, cm usw.).</span><span class="sxs-lookup"><span data-stu-id="3ace2-128">Units to use for the result of expression (in, cm, and so forth).</span></span>  <br/> |
| <span data-ttu-id="3ace2-129">_langID_</span><span class="sxs-lookup"><span data-stu-id="3ace2-129">_langID_</span></span> <br/> |<span data-ttu-id="3ace2-130">Optional</span><span class="sxs-lookup"><span data-stu-id="3ace2-130">Optional</span></span>  <br/> |<span data-ttu-id="3ace2-131">**Number**</span><span class="sxs-lookup"><span data-stu-id="3ace2-131">**Number**</span></span> <br/> |<span data-ttu-id="3ace2-132">Die Sprache, die beim Formatieren von Datums-/Zeitangaben in Microsoft Office System verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3ace2-132">The language used when formatting Microsoft Office System date/time pictures.</span></span>  <br/> |
| <span data-ttu-id="3ace2-133">_calID_</span><span class="sxs-lookup"><span data-stu-id="3ace2-133">_calID_</span></span> <br/> |<span data-ttu-id="3ace2-134">Optional</span><span class="sxs-lookup"><span data-stu-id="3ace2-134">Optional</span></span>  <br/> |<span data-ttu-id="3ace2-135">**Number**</span><span class="sxs-lookup"><span data-stu-id="3ace2-135">**Number**</span></span> <br/> |<span data-ttu-id="3ace2-136">Der Kalender, der beim Formatieren von Datums-/Zeitangaben in Microsoft Office System verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3ace2-136">The calendar used when formatting Microsoft Office System date/time pictures.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="3ace2-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3ace2-137">Return value</span></span>

<span data-ttu-id="3ace2-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="3ace2-138">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3ace2-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3ace2-139">Remarks</span></span>

<span data-ttu-id="3ace2-140">Der Typ des Ausdrucks und der in der Formatierungsangabe angegebene Typ bestimmen das Verhalten der zurückgegebenen Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="3ace2-140">The type of the expression and the type specified in the format picture govern the behavior of the returned string.</span></span> <span data-ttu-id="3ace2-141">format muss für den Typ des Ausdrucks gültig sein.</span><span class="sxs-lookup"><span data-stu-id="3ace2-141">The format must be appropriate for the type of expression.</span></span>
  
<span data-ttu-id="3ace2-142">Mit dem srcUnit-Argument werden typenlose Ergebnisse eines Ausdrucks skaliert, z. B. 3 + 4.</span><span class="sxs-lookup"><span data-stu-id="3ace2-142">The srcUnit argument is used to scale untyped expression results, such as 3 + 4.</span></span> <span data-ttu-id="3ace2-143">Wenn das Ergebnis von expression ausdrücklich einen Typ besitzt, z. B. 3 cm + 8 cm, wird srcUnit ignoriert.</span><span class="sxs-lookup"><span data-stu-id="3ace2-143">If the result of expression has an explicit type, such as 3 ft + 8 ft, then srcUnit is ignored.</span></span>
  
<span data-ttu-id="3ace2-144">Mit dem dstUnit-Argument werden die Maßeinheiten für das formatierte Ergebnis bestimmt.</span><span class="sxs-lookup"><span data-stu-id="3ace2-144">The dstUnit argument is used to specify the units used for the formatted result.</span></span> <span data-ttu-id="3ace2-145">Wenn dstUnit nicht angegeben wurde, werden die Einheiten für das Ergebnis des Ausdrucks verwendet.</span><span class="sxs-lookup"><span data-stu-id="3ace2-145">If dstUnit is not specified, the units for the result of the expression are used.</span></span>
  
<span data-ttu-id="3ace2-146">Ein Fehler wird zurückgegeben, wenn das Ergebnis von expression und der erwartete Typ in format unterschiedlich sind, wenn in format Syntaxfehler enthalten sind oder die als srcUnit bzw. dstUnit übergebenen Einheiten nicht erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="3ace2-146">Returns an error if the result of expression and the type expected in format are of a different kind, if there are syntax errors in format, or if it does not recognize the units passed as srcUnit or dstUnit.</span></span>
  
## <a name="example"></a><span data-ttu-id="3ace2-147">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3ace2-147">Example</span></span>

<span data-ttu-id="3ace2-148">FORMATEX(5.5, "0,00 u", "cm", "ft")</span><span class="sxs-lookup"><span data-stu-id="3ace2-148">FORMATEX(5.5, "0.00 u", "cm", "ft")</span></span> 
  
<span data-ttu-id="3ace2-149">Gibt 0,18 Fuß zurück.</span><span class="sxs-lookup"><span data-stu-id="3ace2-149">Returns 0.18 feet.</span></span> 
  

