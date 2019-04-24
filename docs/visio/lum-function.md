---
title: LUM-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251460
localization_priority: Normal
ms.assetid: 38e6bba7-1bf2-3d31-0912-707002454f5d
description: Gibt den Wert der Helligkeitskomponente einer Farbe zurück.
ms.openlocfilehash: 17fa43f8e2cd7422428f92724e351436233c2d62
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357981"
---
# <a name="lum-function"></a><span data-ttu-id="c4fc8-103">LUM Function</span><span class="sxs-lookup"><span data-stu-id="c4fc8-103">LUM Function</span></span>

<span data-ttu-id="c4fc8-104">Gibt den Wert der Helligkeitskomponente einer Farbe zurück.</span><span class="sxs-lookup"><span data-stu-id="c4fc8-104">Returns the value of a color's luminosity component.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="c4fc8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4fc8-105">Syntax</span></span>

<span data-ttu-id="c4fc8-106">LUM (\* \* *Expression* \* \*)</span><span class="sxs-lookup"><span data-stu-id="c4fc8-106">LUM(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c4fc8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4fc8-107">Parameters</span></span>

|<span data-ttu-id="c4fc8-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="c4fc8-108">**Name**</span></span>|<span data-ttu-id="c4fc8-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="c4fc8-109">**Required/Optional**</span></span>|<span data-ttu-id="c4fc8-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="c4fc8-110">**Data Type**</span></span>|<span data-ttu-id="c4fc8-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c4fc8-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c4fc8-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="c4fc8-112">_expression_</span></span> <br/> |<span data-ttu-id="c4fc8-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c4fc8-113">Required</span></span>  <br/> |<span data-ttu-id="c4fc8-114">**Numerisch**</span><span class="sxs-lookup"><span data-stu-id="c4fc8-114">**Numeric**</span></span> <br/> |<span data-ttu-id="c4fc8-115">Der Farbindex aus der Farbpalette des Dokuments oder ein Bezug auf eine Zelle, die einen Farbindex enthält.</span><span class="sxs-lookup"><span data-stu-id="c4fc8-115">The index of a color in the document's color table, or a reference to a cell that contains a color index.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c4fc8-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c4fc8-116">Return value</span></span>

<span data-ttu-id="c4fc8-117">Zahl</span><span class="sxs-lookup"><span data-stu-id="c4fc8-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c4fc8-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c4fc8-118">Remarks</span></span>

<span data-ttu-id="c4fc8-p101">Der Rückgabewert ist eine Zahl im Bereich von 0 bis einschließlich 240. Bei einer ungültigen Eingabe wird 0 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c4fc8-p101">The return value is a number in the range 0 to 240, inclusive. The function returns 0 for invalid input.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="c4fc8-121">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c4fc8-121">Example 1</span></span>

<span data-ttu-id="c4fc8-122">LUM (Sheet. 4! Zelle FillForegnd</span><span class="sxs-lookup"><span data-stu-id="c4fc8-122">LUM(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="c4fc8-123">Gibt die Farbkomponente Helligkeit der Vordergrundfüllfarbe von Sheet.4 zurück.</span><span class="sxs-lookup"><span data-stu-id="c4fc8-123">Returns the luminosity of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="c4fc8-124">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c4fc8-124">Example 2</span></span>

<span data-ttu-id="c4fc8-125">LUM (6)</span><span class="sxs-lookup"><span data-stu-id="c4fc8-125">LUM(6)</span></span>
  
<span data-ttu-id="c4fc8-126">Gibt 120 zurück, wenn das Dokument die Standardfarbpalette von Visio verwendet, wobei Magenta die Farbe mit Index 6 ist.</span><span class="sxs-lookup"><span data-stu-id="c4fc8-126">Returns 120 if the document uses the default Visio color palette, where magenta is the color at index 6.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="c4fc8-127">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="c4fc8-127">Example 3</span></span>

<span data-ttu-id="c4fc8-128">LUM(HSL(10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="c4fc8-128">LUM(HSL(10, 20, 30))</span></span>
  
<span data-ttu-id="c4fc8-129">Gibt 30 zurück.</span><span class="sxs-lookup"><span data-stu-id="c4fc8-129">Returns 30.</span></span>
  

