---
title: HUE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251440
localization_priority: Normal
ms.assetid: 0f5c6097-eef5-5f58-e2ef-2c348e42dc9a
description: Gibt den Wert der Farbtonkomponente einer Farbe zurück.
ms.openlocfilehash: 39fdd160f5cd792e95930a3e7c7cea3c37ed16c1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439492"
---
# <a name="hue-function"></a><span data-ttu-id="ded49-103">HUE Function</span><span class="sxs-lookup"><span data-stu-id="ded49-103">HUE Function</span></span>

<span data-ttu-id="ded49-104">Gibt den Wert der Farbtonkomponente einer Farbe zurück.</span><span class="sxs-lookup"><span data-stu-id="ded49-104">Returns the value of a color's hue component.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="ded49-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ded49-105">Syntax</span></span>

<span data-ttu-id="ded49-106">HUE (\* \* *Expression* \* \*)</span><span class="sxs-lookup"><span data-stu-id="ded49-106">HUE(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ded49-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ded49-107">Parameters</span></span>

|<span data-ttu-id="ded49-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="ded49-108">**Name**</span></span>|<span data-ttu-id="ded49-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="ded49-109">**Required/Optional**</span></span>|<span data-ttu-id="ded49-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="ded49-110">**Data Type**</span></span>|<span data-ttu-id="ded49-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ded49-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ded49-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="ded49-112">_expression_</span></span> <br/> |<span data-ttu-id="ded49-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ded49-113">Required</span></span>  <br/> |<span data-ttu-id="ded49-114">**String**</span><span class="sxs-lookup"><span data-stu-id="ded49-114">**String**</span></span> <br/> |<span data-ttu-id="ded49-115">Ein Ausdruck, der eine Farbe ergibt.</span><span class="sxs-lookup"><span data-stu-id="ded49-115">An expression that evaluates to a color.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="ded49-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ded49-116">Return value</span></span>

<span data-ttu-id="ded49-117">Zahl</span><span class="sxs-lookup"><span data-stu-id="ded49-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ded49-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ded49-118">Remarks</span></span>

<span data-ttu-id="ded49-p101">Der zurückgegebene Wert ist eine Zahl im Bereich von 0 bis einschließlich 239. Die Eingabe ist ein Index einer Farbe aus der Farbtabelle des Dokuments, ein Ausdruck, der in eine angepasste Farbe (wie RGB oder HSL) aufgelöst wird oder ein Verweis auf eine Zelle, die einen Farbindex oder ein Farbergebnis enthält. Die Funktion gibt bei einer ungültigen Eingabe 0 zurück.</span><span class="sxs-lookup"><span data-stu-id="ded49-p101">The return value is a number in the range 0 to 239, inclusive. The input is an index of a color in the document's color table, an expression that resolves to a custom color (like RGB or HSL), or a reference to a cell that contains a color index or color result. The function returns 0 for invalid input.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="ded49-122">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ded49-122">Example 1</span></span>

<span data-ttu-id="ded49-123">Farbton (Blatt. 4! Zelle FillForegnd</span><span class="sxs-lookup"><span data-stu-id="ded49-123">HUE(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="ded49-124">Gibt den Wert der Farbtonkomponente der Vordergrundfüllfarbe von Sheet.4 zurück.</span><span class="sxs-lookup"><span data-stu-id="ded49-124">Returns the hue of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="ded49-125">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ded49-125">Example 2</span></span>

<span data-ttu-id="ded49-126">FARBTON (7)</span><span class="sxs-lookup"><span data-stu-id="ded49-126">HUE(7)</span></span>
  
<span data-ttu-id="ded49-127">Gibt 120 zurück, wenn das Dokument die Farbpalette von Microsoft Visio verwendet, wobei Zyan die Farbe mit Index 7 darstellt.</span><span class="sxs-lookup"><span data-stu-id="ded49-127">Returns 120 if the document uses the default Microsoft Visio color palette, where cyan is the color at index 7.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="ded49-128">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="ded49-128">Example 3</span></span>

<span data-ttu-id="ded49-129">HUE(HSL(10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="ded49-129">HUE(HSL(10, 20, 30) )</span></span>
  
<span data-ttu-id="ded49-130">Gibt 10 zurück.</span><span class="sxs-lookup"><span data-stu-id="ded49-130">Returns 10.</span></span>
  

