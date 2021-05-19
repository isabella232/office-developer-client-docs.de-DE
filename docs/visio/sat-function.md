---
title: SAT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251494
localization_priority: Normal
ms.assetid: 407817fb-9e4a-d2ca-6125-2440d2a417c6
description: Gibt den Wert der Sättigungskomponente einer Farbe zurück.
ms.openlocfilehash: 3b3fd8e13ca9af4f0aea00d2f78c7b5c27be1932
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415005"
---
# <a name="sat-function"></a><span data-ttu-id="11370-103">SAT Function</span><span class="sxs-lookup"><span data-stu-id="11370-103">SAT Function</span></span>

<span data-ttu-id="11370-104">Gibt den Wert der Sättigungskomponente einer Farbe zurück.</span><span class="sxs-lookup"><span data-stu-id="11370-104">Returns the value of a color's saturation component.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="11370-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="11370-105">Syntax</span></span>

<span data-ttu-id="11370-106">SAT(\*\* *Expression* \*\* )</span><span class="sxs-lookup"><span data-stu-id="11370-106">SAT(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="11370-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="11370-107">Parameters</span></span>

|<span data-ttu-id="11370-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="11370-108">**Name**</span></span>|<span data-ttu-id="11370-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="11370-109">**Required/Optional**</span></span>|<span data-ttu-id="11370-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="11370-110">**Data Type**</span></span>|<span data-ttu-id="11370-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="11370-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="11370-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="11370-112">_expression_</span></span> <br/> |<span data-ttu-id="11370-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="11370-113">Required</span></span>  <br/> |<span data-ttu-id="11370-114">**Variiert**</span><span class="sxs-lookup"><span data-stu-id="11370-114">**Varies**</span></span> <br/> |<span data-ttu-id="11370-115">Ein Index einer Farbe aus der Farbtabelle des Dokuments, ein Ausdruck, der zu einer benutzerdefinierten Farbe (wie RGB oder HSL) aufgelöst wird, oder ein Bezug auf eine Zelle, die einen Farbindex oder ein Farbergebnis enthält.</span><span class="sxs-lookup"><span data-stu-id="11370-115">An index of a color in the document's color table, an expression that resolves to a custom color (like RGB or HSL), or a reference to a cell that contains a color index or color result.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="11370-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="11370-116">Return value</span></span>

<span data-ttu-id="11370-117">Numeric</span><span class="sxs-lookup"><span data-stu-id="11370-117">Numeric</span></span>
  
## <a name="remarks"></a><span data-ttu-id="11370-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="11370-118">Remarks</span></span>

<span data-ttu-id="11370-p101">Der Rückgabewert ist eine Zahl im Bereich von 0 bis einschließlich 240. Bei einer ungültigen Eingabe wird 0 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="11370-p101">The return value is a number in the range 0 to 240, inclusive. The function returns 0 for invalid input.</span></span>
  
## <a name="example-1"></a><span data-ttu-id="11370-121">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="11370-121">Example 1</span></span>

<span data-ttu-id="11370-122">SAT(Sheet.4! FillForegnd)</span><span class="sxs-lookup"><span data-stu-id="11370-122">SAT(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="11370-123">Gibt den Wert der Sättigung der Vordergrundfüllfarbe von Sheet.4 zurück.</span><span class="sxs-lookup"><span data-stu-id="11370-123">Returns the saturation of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="11370-124">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="11370-124">Example 2</span></span>

<span data-ttu-id="11370-125">SAT(8)</span><span class="sxs-lookup"><span data-stu-id="11370-125">SAT(8)</span></span>
  
<span data-ttu-id="11370-126">Gibt 240 zurück, wenn das Dokument die Farbpalette von Visio verwendet, wobei Dunkelrot die Farbe mit Index 8 ist.</span><span class="sxs-lookup"><span data-stu-id="11370-126">Returns 240 if the document uses the default Visio color palette, where dark red is the color at index 8.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="11370-127">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="11370-127">Example 3</span></span>

<span data-ttu-id="11370-128">SAT(HSL(10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="11370-128">SAT(HSL(10, 20, 30))</span></span>
  
<span data-ttu-id="11370-129">Gibt 20 zurück.</span><span class="sxs-lookup"><span data-stu-id="11370-129">Returns 20.</span></span>
  

