---
title: SETF-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251496
localization_priority: Normal
ms.assetid: fcf415c1-171f-b75f-6e40-2bbdbe8b1cfb
description: Legt die Formel einer Zelle fest.
ms.openlocfilehash: 63050de92394ebbdce6cfe053e15347ca3ce5c7f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425974"
---
# <a name="setf-function"></a><span data-ttu-id="f8a0d-103">SETF Function</span><span class="sxs-lookup"><span data-stu-id="f8a0d-103">SETF Function</span></span>

<span data-ttu-id="f8a0d-104">Legt die Formel einer Zelle fest.</span><span class="sxs-lookup"><span data-stu-id="f8a0d-104">Sets a cell's formula.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f8a0d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8a0d-105">Syntax</span></span>

<span data-ttu-id="f8a0d-106">Setf (GETREF (\* \* *Cell* \* \*), \* \* *Formel* \* \*)</span><span class="sxs-lookup"><span data-stu-id="f8a0d-106">SETF( GETREF(\*\* *cell* \*\* ), \*\* *formula* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f8a0d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8a0d-107">Parameters</span></span>

|<span data-ttu-id="f8a0d-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="f8a0d-108">**Name**</span></span>|<span data-ttu-id="f8a0d-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="f8a0d-109">**Required/Optional**</span></span>|<span data-ttu-id="f8a0d-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="f8a0d-110">**Data Type**</span></span>|<span data-ttu-id="f8a0d-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f8a0d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f8a0d-112">_Zelle_</span><span class="sxs-lookup"><span data-stu-id="f8a0d-112">_cell_</span></span> <br/> |<span data-ttu-id="f8a0d-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="f8a0d-113">Required</span></span>  <br/> |<span data-ttu-id="f8a0d-114">**String**</span><span class="sxs-lookup"><span data-stu-id="f8a0d-114">**String**</span></span> <br/> |<span data-ttu-id="f8a0d-115">Die Zelle, deren Formel festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f8a0d-115">The cell whose formula to set.</span></span>  <br/> |
| <span data-ttu-id="f8a0d-116">_formula_</span><span class="sxs-lookup"><span data-stu-id="f8a0d-116">_formula_</span></span> <br/> |<span data-ttu-id="f8a0d-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="f8a0d-117">Required</span></span>  <br/> |<span data-ttu-id="f8a0d-118">**String**</span><span class="sxs-lookup"><span data-stu-id="f8a0d-118">**String**</span></span> <br/> |<span data-ttu-id="f8a0d-119">Die zu verwendende Formel.</span><span class="sxs-lookup"><span data-stu-id="f8a0d-119">The formula to use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f8a0d-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f8a0d-120">Remarks</span></span>

<span data-ttu-id="f8a0d-121">Bei der Auswertung wird das Ergebnis des Ausdrucks in der _Formel_ zur neuen Formel in _Cell_.</span><span class="sxs-lookup"><span data-stu-id="f8a0d-121">When evaluated, the result of the expression in  _formula_ becomes the new formula in  _cell_.</span></span> <span data-ttu-id="f8a0d-122">Wenn die _Formel_ in Anführungszeichen eingeschlossen ist, wird der zitierte Ausdruck in _Cell_geschrieben.</span><span class="sxs-lookup"><span data-stu-id="f8a0d-122">If  _formula_ is enclosed in quotation marks, the quoted expression is written to  _cell_.</span></span> <span data-ttu-id="f8a0d-123">Um eine _Zelle_ auf eine Zeichenfolge festzulegen, müssen Sie die _Formel_ in drei Gruppen von Anführungszeichen einschließen.</span><span class="sxs-lookup"><span data-stu-id="f8a0d-123">To set  _cell_ to a string, enclose  _formula_ in three sets of quotation marks.</span></span> 
  
<span data-ttu-id="f8a0d-p102">Die Zielzelle muss mithilfe eines GETREF()-Bezugs oder als Zeichenfolge angegeben werden, um eine Zirkularität zu vermeiden. Die Verwendung von GETREF wird bevorzugt, da Bezüge in Microsoft Visio angepasst werden können, wenn das Shape in ein anderes Dokument verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="f8a0d-p102">The target cell must be specified using a GETREF() reference or as a string to avoid circularity. Using GETREF is preferred, because Microsoft Visio can adjust references when the shape is moved to a different document.</span></span>
  
<span data-ttu-id="f8a0d-126">Wenn _Cell_ nicht mit getref oder als Zeichenfolge angegeben wird, gibt die Funktion einen Fehler zurück, und die Formel der Zelle wird nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="f8a0d-126">If  _cell_ is not specified using GETREF or as a string, the function returns an error, and no cell's formula is changed.</span></span> <span data-ttu-id="f8a0d-127">Wenn die _Formel_ einen Syntaxfehler enthält, gibt die Funktion einen Fehler zurück, und die Formel in _Cell_ wird nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="f8a0d-127">If  _formula_ contains a syntax error, the function returns an error, and the formula in  _cell_ is not changed.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="f8a0d-128">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f8a0d-128">Example 1</span></span>

<span data-ttu-id="f8a0d-129">SETF (GETREF (Scratch. a1), 1,5 in \* 6 + 1 ft)</span><span class="sxs-lookup"><span data-stu-id="f8a0d-129">SETF( GETREF(Scratch.A1), 1.5 in \* 6 + 1 ft)</span></span>
  
<span data-ttu-id="f8a0d-130">Legt die Formel von Scratch.A1 auf 39 cm fest.</span><span class="sxs-lookup"><span data-stu-id="f8a0d-130">Sets the formula of Scratch.A1 to 21 inches.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="f8a0d-131">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f8a0d-131">Example 2</span></span>

<span data-ttu-id="f8a0d-132">SETF (GETREF (Scratch. a1), "1,5 in \* 6 + 1 ft")</span><span class="sxs-lookup"><span data-stu-id="f8a0d-132">SETF( GETREF(Scratch.A1), "1.5 in \* 6 + 1 ft")</span></span>
  
<span data-ttu-id="f8a0d-133">Legt die Formel für Scratch.</span><span class="sxs-lookup"><span data-stu-id="f8a0d-133">Sets the formula of Scratch.</span></span> <span data-ttu-id="f8a0d-134">A1 auf den Ausdruck 1,5 in\*6 + 1 ft.</span><span class="sxs-lookup"><span data-stu-id="f8a0d-134">A1 to the expression 1.5 in\*6+1 ft.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="f8a0d-135">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="f8a0d-135">Example 3</span></span>

<span data-ttu-id="f8a0d-136">SETF( GETREF(Scratch.A1), """Sag """"ahh""""""")</span><span class="sxs-lookup"><span data-stu-id="f8a0d-136">SETF( GETREF(Scratch.A1), """Say """"ahh""""""")</span></span>
  
<span data-ttu-id="f8a0d-137">Legt die Formel von Scratch.A1 auf die Zeichenfolge "Sag ""ahh""" fest, die in Sag "ahh" ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="f8a0d-137">Sets the formula of Scratch.A1 to the string "Say ""ahh""" which evaluates to Say "ahh".</span></span>
  

