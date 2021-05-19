---
title: SHAPETEXT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251788
localization_priority: Normal
ms.assetid: 87ea5e8f-c3e0-009f-4bf8-8c34fbdb83a6
description: Ruft den Text aus einer Form ab.
ms.openlocfilehash: bb9b1fbe5900cd051828ed6c7ff07546567c1b23
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419345"
---
# <a name="shapetext-function"></a><span data-ttu-id="c140f-103">SHAPETEXT Function</span><span class="sxs-lookup"><span data-stu-id="c140f-103">SHAPETEXT Function</span></span>

<span data-ttu-id="c140f-104">Ruft den Text aus einer Form ab.</span><span class="sxs-lookup"><span data-stu-id="c140f-104">Gets the text from a shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c140f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c140f-105">Syntax</span></span>

<span data-ttu-id="c140f-106">SHAPETEXT (\*\* *shapename! TheText* \*\* \*\* *[,flag]* \*\* )</span><span class="sxs-lookup"><span data-stu-id="c140f-106">SHAPETEXT (\*\* *shapename!TheText* \*\* \*\* *[,flag]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c140f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c140f-107">Parameters</span></span>

|<span data-ttu-id="c140f-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="c140f-108">**Name**</span></span>|<span data-ttu-id="c140f-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="c140f-109">**Required/Optional**</span></span>|<span data-ttu-id="c140f-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="c140f-110">**Data Type**</span></span>|<span data-ttu-id="c140f-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c140f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c140f-112">_shapename! TheText_</span><span class="sxs-lookup"><span data-stu-id="c140f-112">_shapename!TheText_</span></span> <br/> |<span data-ttu-id="c140f-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c140f-113">Required</span></span>  <br/> ||<span data-ttu-id="c140f-114">Ein Verweis auf die Zelle mit dem Namen TheText in der Zielform.</span><span class="sxs-lookup"><span data-stu-id="c140f-114">A reference to the cell named TheText in the target shape.</span></span>  <span data-ttu-id="c140f-115">_Shapename!_</span><span class="sxs-lookup"><span data-stu-id="c140f-115">_Shapename!_</span></span> <span data-ttu-id="c140f-116">ist der Name der Form, aus der Sie den Text abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="c140f-116">is the name of the shape from which you want to retrieve the text.</span></span>  <br/> |
| <span data-ttu-id="c140f-117">_Flag_</span><span class="sxs-lookup"><span data-stu-id="c140f-117">_flag_</span></span> <br/> |<span data-ttu-id="c140f-118">Optional.</span><span class="sxs-lookup"><span data-stu-id="c140f-118">Optional</span></span>  <br/> |<span data-ttu-id="c140f-119">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="c140f-119">**Numeric**</span></span> <br/> |<span data-ttu-id="c140f-p102">Ein Bit, das das Format des Texts bestimmt. Wenn das Standard-Flag (0) verwendet wird, wird der Text genauso wie im Shape dargestellt.</span><span class="sxs-lookup"><span data-stu-id="c140f-p102">A bit that specifies the format of the text. The default flag (0) shows the text exactly as it is shown in the shape.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c140f-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c140f-122">Return value</span></span>

<span data-ttu-id="c140f-123">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c140f-123">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c140f-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c140f-124">Remarks</span></span>

<span data-ttu-id="c140f-125">Sie können eine beliebige Kombination folgender Flags mit der Funktion SHAPETEXT verwenden.</span><span class="sxs-lookup"><span data-stu-id="c140f-125">You can use any combination of the following flags with the SHAPETEXT function.</span></span>
  
|<span data-ttu-id="c140f-126">**Wert**</span><span class="sxs-lookup"><span data-stu-id="c140f-126">**Flag**</span></span>|<span data-ttu-id="c140f-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c140f-127">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c140f-128">0</span><span class="sxs-lookup"><span data-stu-id="c140f-128">0</span></span>  <br/> |<span data-ttu-id="c140f-129">Zeigt den Text genau wie in dem Shape an.</span><span class="sxs-lookup"><span data-stu-id="c140f-129">Show text exactly as shown in shape.</span></span>  <br/> |
|<span data-ttu-id="c140f-130">1</span><span class="sxs-lookup"><span data-stu-id="c140f-130">1</span></span>  <br/> |<span data-ttu-id="c140f-131">Willkürliche Bindestriche einschließen.</span><span class="sxs-lookup"><span data-stu-id="c140f-131">Include discretionary hyphens.</span></span>  <br/> |
|<span data-ttu-id="c140f-132">2</span><span class="sxs-lookup"><span data-stu-id="c140f-132">2</span></span>  <br/> |<span data-ttu-id="c140f-133">Keinen erweiterten Text in Feldern einschließen.</span><span class="sxs-lookup"><span data-stu-id="c140f-133">Don't include expanded text in fields.</span></span>  <br/> |
|<span data-ttu-id="c140f-134">4 </span><span class="sxs-lookup"><span data-stu-id="c140f-134">4</span></span>  <br/> |<span data-ttu-id="c140f-135">Tabulatorzeichen in ein einzelnes Leerzeichen konvertieren.</span><span class="sxs-lookup"><span data-stu-id="c140f-135">Convert tabs to a single space.</span></span>  <br/> |
|<span data-ttu-id="c140f-136">8 </span><span class="sxs-lookup"><span data-stu-id="c140f-136">8</span></span>  <br/> |<span data-ttu-id="c140f-137">Tabulatorzeichen in mehrere Leerzeichen konvertieren.</span><span class="sxs-lookup"><span data-stu-id="c140f-137">Convert tabs to a set of spaces.</span></span>  <br/> |
|<span data-ttu-id="c140f-138">16 </span><span class="sxs-lookup"><span data-stu-id="c140f-138">16</span></span>  <br/> |<span data-ttu-id="c140f-139">Zeilenschaltungen und Zeilenumbrüche in Leerzeichen konvertieren.</span><span class="sxs-lookup"><span data-stu-id="c140f-139">Convert carriage returns and line feeds to spaces.</span></span>  <br/> |
|<span data-ttu-id="c140f-140">32</span><span class="sxs-lookup"><span data-stu-id="c140f-140">32</span></span>  <br/> |<span data-ttu-id="c140f-141">Typografische Anführungszeichen in normale Anführungszeichen konvertieren.</span><span class="sxs-lookup"><span data-stu-id="c140f-141">Convert typographer quotes to regular quotes.</span></span>  <br/> |
|<span data-ttu-id="c140f-142">64</span><span class="sxs-lookup"><span data-stu-id="c140f-142">64</span></span>  <br/> |<span data-ttu-id="c140f-143">Benachbarte Leerzeichen in ein einzelnes Leerzeichen konvertieren.</span><span class="sxs-lookup"><span data-stu-id="c140f-143">Convert adjacent white space to a single space.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="c140f-144">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c140f-144">Example 1</span></span>

<span data-ttu-id="c140f-145">SHAPETEXT(sheetN!theText)</span><span class="sxs-lookup"><span data-stu-id="c140f-145">SHAPETEXT(sheetN!theText)</span></span>
  
<span data-ttu-id="c140f-146">Gibt den Text aus dem Shape namens sheetN genau so zurück, wie er in dem Shape angezeigt ist.</span><span class="sxs-lookup"><span data-stu-id="c140f-146">Returns the text of the shape named sheetN, exactly as it is shown in the shape.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="c140f-147">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c140f-147">Example 2</span></span>

<span data-ttu-id="c140f-148">SHAPETEXT(theText)</span><span class="sxs-lookup"><span data-stu-id="c140f-148">SHAPETEXT(theText)</span></span>
  
<span data-ttu-id="c140f-149">Gibt den Text aus dem aktuellen Shape genau so zurück, wie er in dem Shape angezeigt ist.</span><span class="sxs-lookup"><span data-stu-id="c140f-149">Returns the text of the current shape exactly as it is shown in the shape.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="c140f-150">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="c140f-150">Example 3</span></span>

<span data-ttu-id="c140f-151">SHAPETEXT(DerText, 84)</span><span class="sxs-lookup"><span data-stu-id="c140f-151">SHAPETEXT(theText, 84)</span></span>
  
<span data-ttu-id="c140f-p103">Gibt den Text des aktuellen Shapes zurück. Außerdem werden benachbarte Leerzeichen in ein einzelnes Leerzeichen (64), Zeilenschaltungen und Zeilenumbrüche (16) in Leerzeichen und Tabulatoren in ein einzelnes Leerzeichen konvertiert. Die Summe dieser Flags ist 84.</span><span class="sxs-lookup"><span data-stu-id="c140f-p103">Returns the text of the current shape. It also converts adjacent white space to a single space (64), converts carriage returns and line feeds to spaces (16), and converts tabs to a single space (4). The sum of these flags is 84.</span></span>
  

