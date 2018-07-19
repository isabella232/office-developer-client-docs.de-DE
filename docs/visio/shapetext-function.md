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
description: Ruft den Text aus einem Shape ab.
ms.openlocfilehash: 53a0cb6e485ae2fd233792e1ebd9765426b7f798
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798062"
---
# <a name="shapetext-function"></a><span data-ttu-id="fc6e5-103">SHAPETEXT Function</span><span class="sxs-lookup"><span data-stu-id="fc6e5-103">SHAPETEXT Function</span></span>

<span data-ttu-id="fc6e5-104">Ruft den Text aus einem Shape ab.</span><span class="sxs-lookup"><span data-stu-id="fc6e5-104">Gets the text from a shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="fc6e5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fc6e5-105">Syntax</span></span>

<span data-ttu-id="fc6e5-106">SHAPETEXT (** *Shapename! TheText* ** ** *[, Flag]* **)</span><span class="sxs-lookup"><span data-stu-id="fc6e5-106">SHAPETEXT (** *shapename!TheText* ** ** *[,flag]* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="fc6e5-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc6e5-107">Parameters</span></span>

|<span data-ttu-id="fc6e5-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="fc6e5-108">**Name**</span></span>|<span data-ttu-id="fc6e5-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="fc6e5-109">**Required/Optional**</span></span>|<span data-ttu-id="fc6e5-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="fc6e5-110">**Data Type**</span></span>|<span data-ttu-id="fc6e5-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fc6e5-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="fc6e5-112">_Shapename! TheText_</span><span class="sxs-lookup"><span data-stu-id="fc6e5-112">_shapename!TheText_</span></span> <br/> |<span data-ttu-id="fc6e5-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="fc6e5-113">Required</span></span>  <br/> ||<span data-ttu-id="fc6e5-114">Ein Verweis auf die Zelle TheText mit der in der Ziel-Shape.</span><span class="sxs-lookup"><span data-stu-id="fc6e5-114">A reference to the cell named TheText in the target shape.</span></span>  <span data-ttu-id="fc6e5-115">_Shapename!_</span><span class="sxs-lookup"><span data-stu-id="fc6e5-115">_Shapename!_</span></span> <span data-ttu-id="fc6e5-116">ist der Name des Shapes, von dem Sie den Text abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="fc6e5-116">is the name of the shape from which you want to retrieve the text.</span></span>  <br/> |
| <span data-ttu-id="fc6e5-117">_Flag_</span><span class="sxs-lookup"><span data-stu-id="fc6e5-117">_flag_</span></span> <br/> |<span data-ttu-id="fc6e5-118">Optional</span><span class="sxs-lookup"><span data-stu-id="fc6e5-118">Optional</span></span>  <br/> |<span data-ttu-id="fc6e5-119">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="fc6e5-119">**Numeric**</span></span> <br/> |<span data-ttu-id="fc6e5-p102">Ein Bit, das das Format des Texts bestimmt. Wenn das Standard-Flag (0) verwendet wird, wird der Text genauso wie im Shape dargestellt.</span><span class="sxs-lookup"><span data-stu-id="fc6e5-p102">A bit that specifies the format of the text. The default flag (0) shows the text exactly as it is shown in the shape.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="fc6e5-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fc6e5-122">Return value</span></span>

<span data-ttu-id="fc6e5-123">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="fc6e5-123">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fc6e5-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fc6e5-124">Remarks</span></span>

<span data-ttu-id="fc6e5-125">Sie können eine beliebige Kombination folgender Flags mit der Funktion SHAPETEXT verwenden.</span><span class="sxs-lookup"><span data-stu-id="fc6e5-125">You can use any combination of the following flags with the SHAPETEXT function.</span></span>
  
|<span data-ttu-id="fc6e5-126">**Wert**</span><span class="sxs-lookup"><span data-stu-id="fc6e5-126">**Flag**</span></span>|<span data-ttu-id="fc6e5-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fc6e5-127">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fc6e5-128">0</span><span class="sxs-lookup"><span data-stu-id="fc6e5-128">0</span></span>  <br/> |<span data-ttu-id="fc6e5-129">Zeigt den Text genau wie in dem Shape an.</span><span class="sxs-lookup"><span data-stu-id="fc6e5-129">Show text exactly as shown in shape.</span></span>  <br/> |
|<span data-ttu-id="fc6e5-130">1</span><span class="sxs-lookup"><span data-stu-id="fc6e5-130">1</span></span>  <br/> |<span data-ttu-id="fc6e5-131">Willkürliche Bindestriche einschließen.</span><span class="sxs-lookup"><span data-stu-id="fc6e5-131">Include discretionary hyphens.</span></span>  <br/> |
|<span data-ttu-id="fc6e5-132">2</span><span class="sxs-lookup"><span data-stu-id="fc6e5-132">2</span></span>  <br/> |<span data-ttu-id="fc6e5-133">Keinen erweiterten Text in Feldern einschließen.</span><span class="sxs-lookup"><span data-stu-id="fc6e5-133">Don't include expanded text in fields.</span></span>  <br/> |
|<span data-ttu-id="fc6e5-134">4</span><span class="sxs-lookup"><span data-stu-id="fc6e5-134">4</span></span>  <br/> |<span data-ttu-id="fc6e5-135">Tabulatorzeichen in ein einzelnes Leerzeichen konvertieren.</span><span class="sxs-lookup"><span data-stu-id="fc6e5-135">Convert tabs to a single space.</span></span>  <br/> |
|<span data-ttu-id="fc6e5-136">8</span><span class="sxs-lookup"><span data-stu-id="fc6e5-136">8</span></span>  <br/> |<span data-ttu-id="fc6e5-137">Tabulatorzeichen in mehrere Leerzeichen konvertieren.</span><span class="sxs-lookup"><span data-stu-id="fc6e5-137">Convert tabs to a set of spaces.</span></span>  <br/> |
|<span data-ttu-id="fc6e5-138">16</span><span class="sxs-lookup"><span data-stu-id="fc6e5-138">16</span></span>  <br/> |<span data-ttu-id="fc6e5-139">Zeilenschaltungen und Zeilenumbrüche in Leerzeichen konvertieren.</span><span class="sxs-lookup"><span data-stu-id="fc6e5-139">Convert carriage returns and line feeds to spaces.</span></span>  <br/> |
|<span data-ttu-id="fc6e5-140">32</span><span class="sxs-lookup"><span data-stu-id="fc6e5-140">32</span></span>  <br/> |<span data-ttu-id="fc6e5-141">Typografische Anführungszeichen in normale Anführungszeichen konvertieren.</span><span class="sxs-lookup"><span data-stu-id="fc6e5-141">Convert typographer quotes to regular quotes.</span></span>  <br/> |
|<span data-ttu-id="fc6e5-142">64</span><span class="sxs-lookup"><span data-stu-id="fc6e5-142">64</span></span>  <br/> |<span data-ttu-id="fc6e5-143">Benachbarte Leerzeichen in ein einzelnes Leerzeichen konvertieren.</span><span class="sxs-lookup"><span data-stu-id="fc6e5-143">Convert adjacent white space to a single space.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="fc6e5-144">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fc6e5-144">Example 1</span></span>

<span data-ttu-id="fc6e5-145">SHAPETEXT(sheetN!theText)</span><span class="sxs-lookup"><span data-stu-id="fc6e5-145">SHAPETEXT(sheetN!theText)</span></span>
  
<span data-ttu-id="fc6e5-146">Gibt den Text aus dem Shape namens sheetN genau so zurück, wie er in dem Shape angezeigt ist.</span><span class="sxs-lookup"><span data-stu-id="fc6e5-146">Returns the text of the shape named sheetN, exactly as it is shown in the shape.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="fc6e5-147">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fc6e5-147">Example 2</span></span>

<span data-ttu-id="fc6e5-148">SHAPETEXT(theText)</span><span class="sxs-lookup"><span data-stu-id="fc6e5-148">SHAPETEXT(theText)</span></span>
  
<span data-ttu-id="fc6e5-149">Gibt den Text aus dem aktuellen Shape genau so zurück, wie er in dem Shape angezeigt ist.</span><span class="sxs-lookup"><span data-stu-id="fc6e5-149">Returns the text of the current shape exactly as it is shown in the shape.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="fc6e5-150">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="fc6e5-150">Example 3</span></span>

<span data-ttu-id="fc6e5-151">SHAPETEXT(DerText, 84)</span><span class="sxs-lookup"><span data-stu-id="fc6e5-151">SHAPETEXT(theText, 84)</span></span>
  
<span data-ttu-id="fc6e5-p103">Gibt den Text des aktuellen Shapes zurück. Außerdem werden benachbarte Leerzeichen in ein einzelnes Leerzeichen (64), Zeilenschaltungen und Zeilenumbrüche (16) in Leerzeichen und Tabulatoren in ein einzelnes Leerzeichen konvertiert. Die Summe dieser Flags ist 84.</span><span class="sxs-lookup"><span data-stu-id="fc6e5-p103">Returns the text of the current shape. It also converts adjacent white space to a single space (64), converts carriage returns and line feeds to spaces (16), and converts tabs to a single space (4). The sum of these flags is 84.</span></span>
  

