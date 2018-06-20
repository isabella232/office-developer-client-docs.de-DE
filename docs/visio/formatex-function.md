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
description: Gibt das Ergebnis von Expression in SrcUnit als Zeichenfolge ausgewertet formatiert entsprechend Format wurde.
ms.openlocfilehash: 08d123967272e0ab4e25990bcfab55cc80cef55d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797069"
---
# <a name="formatex-function"></a><span data-ttu-id="8d6bf-103">FORMATEX-Funktion</span><span class="sxs-lookup"><span data-stu-id="8d6bf-103">FORMATEX Function</span></span>

<span data-ttu-id="8d6bf-104">Gibt das Ergebnis von Expression in SrcUnit als Zeichenfolge ausgewertet formatiert entsprechend Format wurde.</span><span class="sxs-lookup"><span data-stu-id="8d6bf-104">Returns the result of expression evaluated in srcUnit as a string formatted according to format expressed in dstUnit.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="8d6bf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d6bf-105">Syntax</span></span>

<span data-ttu-id="8d6bf-106">FORMATEX (** *Ausdruck* **, "** *Format* **", [** *SrcUnit* **], [** *DstUnit* **], [** *LangID* **] [, ** *CalID* **])</span><span class="sxs-lookup"><span data-stu-id="8d6bf-106">FORMATEX(** *expression* **," ** *format* ** ",[ ** *srcUnit* ** ],[ ** *dstUnit* ** ],[ ** *langID* ** ][, ** *calID* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8d6bf-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d6bf-107">Parameters</span></span>

|<span data-ttu-id="8d6bf-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="8d6bf-108">**Name**</span></span>|<span data-ttu-id="8d6bf-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="8d6bf-109">**Required/Optional**</span></span>|<span data-ttu-id="8d6bf-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="8d6bf-110">**Data Type**</span></span>|<span data-ttu-id="8d6bf-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8d6bf-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8d6bf-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="8d6bf-112">_expression_</span></span> <br/> |<span data-ttu-id="8d6bf-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8d6bf-113">Required</span></span>  <br/> |<span data-ttu-id="8d6bf-114">**String**</span><span class="sxs-lookup"><span data-stu-id="8d6bf-114">**String**</span></span> <br/> |<span data-ttu-id="8d6bf-115">Eine Kombination aus Konstanten, Operatoren, Funktionen und Bezügen auf ShapeSheet-Zellen, die einen Wert ergeben.</span><span class="sxs-lookup"><span data-stu-id="8d6bf-115">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value.</span></span>  <br/> |
| <span data-ttu-id="8d6bf-116">_format_</span><span class="sxs-lookup"><span data-stu-id="8d6bf-116">_format_</span></span> <br/> |<span data-ttu-id="8d6bf-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8d6bf-117">Required</span></span>  <br/> |<span data-ttu-id="8d6bf-118">**String**</span><span class="sxs-lookup"><span data-stu-id="8d6bf-118">**String**</span></span> <br/> |<span data-ttu-id="8d6bf-119">Die Formatierungsangabe zum Formatieren der Zeichenfolge verwendet.</span><span class="sxs-lookup"><span data-stu-id="8d6bf-119">The format picture used to format the string.</span></span> <span data-ttu-id="8d6bf-120">Weitere Informationen zu Formatierungsangaben finden Sie unter [Informationen zu Formatierungsangaben](about-format-pictures.md).</span><span class="sxs-lookup"><span data-stu-id="8d6bf-120">For more information about format pictures, see [About Format Pictures](about-format-pictures.md).</span></span>  <br/> |
| <span data-ttu-id="8d6bf-121">_srcUnit_</span><span class="sxs-lookup"><span data-stu-id="8d6bf-121">_srcUnit_</span></span> <br/> |<span data-ttu-id="8d6bf-122">Optional</span><span class="sxs-lookup"><span data-stu-id="8d6bf-122">Optional</span></span>  <br/> |<span data-ttu-id="8d6bf-123">**String**</span><span class="sxs-lookup"><span data-stu-id="8d6bf-123">**String**</span></span> <br/> | <span data-ttu-id="8d6bf-124">Einheiten zum Auswerten von Expression (in, cm usw.).</span><span class="sxs-lookup"><span data-stu-id="8d6bf-124">Units used to evaluate expression (in, cm, and so forth).</span></span>  <br/> |
| <span data-ttu-id="8d6bf-125">_dstUnit_</span><span class="sxs-lookup"><span data-stu-id="8d6bf-125">_dstUnit_</span></span> <br/> |<span data-ttu-id="8d6bf-126">Optional</span><span class="sxs-lookup"><span data-stu-id="8d6bf-126">Optional</span></span>  <br/> |<span data-ttu-id="8d6bf-127">**String**</span><span class="sxs-lookup"><span data-stu-id="8d6bf-127">**String**</span></span> <br/> |<span data-ttu-id="8d6bf-128">Einheiten, die für das Ergebnis von Expression (in, cm usw.) verwendet.</span><span class="sxs-lookup"><span data-stu-id="8d6bf-128">Units to use for the result of expression (in, cm, and so forth).</span></span>  <br/> |
| <span data-ttu-id="8d6bf-129">_langID_</span><span class="sxs-lookup"><span data-stu-id="8d6bf-129">_langID_</span></span> <br/> |<span data-ttu-id="8d6bf-130">Optional</span><span class="sxs-lookup"><span data-stu-id="8d6bf-130">Optional</span></span>  <br/> |<span data-ttu-id="8d6bf-131">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="8d6bf-131">**Number**</span></span> <br/> |<span data-ttu-id="8d6bf-132">Die Sprache, die beim Formatieren von Datums-/Zeitangaben in Microsoft Office System verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8d6bf-132">The language used when formatting Microsoft Office System date/time pictures.</span></span>  <br/> |
| <span data-ttu-id="8d6bf-133">_calID_</span><span class="sxs-lookup"><span data-stu-id="8d6bf-133">_calID_</span></span> <br/> |<span data-ttu-id="8d6bf-134">Optional</span><span class="sxs-lookup"><span data-stu-id="8d6bf-134">Optional</span></span>  <br/> |<span data-ttu-id="8d6bf-135">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="8d6bf-135">**Number**</span></span> <br/> |<span data-ttu-id="8d6bf-136">Der Kalender, der beim Formatieren von Datums-/Zeitangaben in Microsoft Office System verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8d6bf-136">The calendar used when formatting Microsoft Office System date/time pictures.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="8d6bf-137">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="8d6bf-137">Return value</span></span>

<span data-ttu-id="8d6bf-138">String</span><span class="sxs-lookup"><span data-stu-id="8d6bf-138">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8d6bf-139">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8d6bf-139">Remarks</span></span>

<span data-ttu-id="8d6bf-140">Der Typ des Ausdrucks und der in der Formatierungsangabe angegebene Typ bestimmen das Verhalten der zurückgegebenen Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="8d6bf-140">The type of the expression and the type specified in the format picture govern the behavior of the returned string.</span></span> <span data-ttu-id="8d6bf-141">Das Format muss für den Typ des Ausdrucks.</span><span class="sxs-lookup"><span data-stu-id="8d6bf-141">The format must be appropriate for the type of expression.</span></span>
  
<span data-ttu-id="8d6bf-142">Das Argument SrcUnit wird verwendet, um die Ergebnisse nicht typisierter Ausdruck, wie etwa 3 + 4 skalieren.</span><span class="sxs-lookup"><span data-stu-id="8d6bf-142">The srcUnit argument is used to scale untyped expression results, such as 3 + 4.</span></span> <span data-ttu-id="8d6bf-143">Wenn das Ergebnis von Expression ausdrücklich einen Typ besitzt, wird beispielsweise 3 ft + 8 ft, SrcUnit ignoriert.</span><span class="sxs-lookup"><span data-stu-id="8d6bf-143">If the result of expression has an explicit type, such as 3 ft + 8 ft, then srcUnit is ignored.</span></span>
  
<span data-ttu-id="8d6bf-144">Das Argument DstUnit wird verwendet, um die Maßeinheiten für das formatierte Ergebnis bestimmt.</span><span class="sxs-lookup"><span data-stu-id="8d6bf-144">The dstUnit argument is used to specify the units used for the formatted result.</span></span> <span data-ttu-id="8d6bf-145">Wenn DstUnit nicht angegeben ist, werden die Einheiten für das Ergebnis des Ausdrucks verwendet.</span><span class="sxs-lookup"><span data-stu-id="8d6bf-145">If dstUnit is not specified, the units for the result of the expression are used.</span></span>
  
<span data-ttu-id="8d6bf-146">Gibt ein Fehler, wenn das Ergebnis von Expression und der erwartete Typ in Format unterschiedlich sind Wenn formatPicture Syntaxfehler im Format, oder wenn es nicht erkennt, dass die Einheiten als SrcUnit oder DstUnit übergeben.</span><span class="sxs-lookup"><span data-stu-id="8d6bf-146">Returns an error if the result of expression and the type expected in format are of a different kind, if there are syntax errors in format, or if it does not recognize the units passed as srcUnit or dstUnit.</span></span>
  
## <a name="example"></a><span data-ttu-id="8d6bf-147">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8d6bf-147">Example</span></span>

<span data-ttu-id="8d6bf-148">FORMATEX(5.5, "0,00 u", "cm", "ft")</span><span class="sxs-lookup"><span data-stu-id="8d6bf-148">FORMATEX(5.5, "0.00 u", "cm", "ft")</span></span> 
  
<span data-ttu-id="8d6bf-149">Gibt 0,18 Fuß zurück.</span><span class="sxs-lookup"><span data-stu-id="8d6bf-149">Returns 0.18 feet.</span></span> 
  

