---
title: GREEN-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251434
localization_priority: Normal
ms.assetid: eccec432-32d3-15c2-06b3-dd02b6313d4c
description: Gibt die Grünkomponente einer Farbe zurück.
ms.openlocfilehash: 04bdadc0fa34dc4f51061d428b9366a433b669a5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797141"
---
# <a name="green-function"></a><span data-ttu-id="79fea-103">GREEN Function</span><span class="sxs-lookup"><span data-stu-id="79fea-103">GREEN Function</span></span>

<span data-ttu-id="79fea-104">Gibt die Grünkomponente einer Farbe zurück.</span><span class="sxs-lookup"><span data-stu-id="79fea-104">Returns the green component of a color.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="79fea-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="79fea-105">Syntax</span></span>

<span data-ttu-id="79fea-106">Grün (** *Ausdruck* **)</span><span class="sxs-lookup"><span data-stu-id="79fea-106">GREEN(** *expression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="79fea-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="79fea-107">Parameters</span></span>

|<span data-ttu-id="79fea-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="79fea-108">**Name**</span></span>|<span data-ttu-id="79fea-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="79fea-109">**Required/Optional**</span></span>|<span data-ttu-id="79fea-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="79fea-110">**Data Type**</span></span>|<span data-ttu-id="79fea-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="79fea-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="79fea-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="79fea-112">_expression_</span></span> <br/> |<span data-ttu-id="79fea-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="79fea-113">Required</span></span>  <br/> |<span data-ttu-id="79fea-114">**Variiert**</span><span class="sxs-lookup"><span data-stu-id="79fea-114">**Varies**</span></span> <br/> |<span data-ttu-id="79fea-115">Ein Index einer Farbe in das Dokument Farbe Tabelle ein Ausdruck, der in einer benutzerdefinierten Farbe (wie RGB oder HSL) oder ein Bezug auf eine Zelle, die eine Farbe Index oder Farbe Ergebnis enthält aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="79fea-115">An index of a color in the document's color table, an expression that resolves to a custom color (such as RGB or HSL), or a reference to a cell that contains a color index or color result.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="79fea-116">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="79fea-116">Return value</span></span>

<span data-ttu-id="79fea-117">Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="79fea-117">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="79fea-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="79fea-118">Remarks</span></span>

<span data-ttu-id="79fea-119">Der Rückgabewert ist eine Zahl im Bereich von 0 bis einschließlich 255 oder Bezug auf eine Zelle, die als Index aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="79fea-119">The return value is a number in the range 0 to 255, inclusive, or a cell reference that resolves to an index.</span></span> <span data-ttu-id="79fea-120">Wenn *Ausdruck* ungültig ist, wird 0 (Schwarz) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="79fea-120">If  *expression*  is invalid, it returns 0 (black).</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="79fea-121">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="79fea-121">Example 1</span></span>

<span data-ttu-id="79fea-122">Grün (Sheet4! FillForegnd)</span><span class="sxs-lookup"><span data-stu-id="79fea-122">GREEN(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="79fea-123">Gibt den Wert der Grünkomponente der Vordergrundfüllfarbe von Sheet.4 zurück.</span><span class="sxs-lookup"><span data-stu-id="79fea-123">Returns the green component of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="79fea-124">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="79fea-124">Example 2</span></span>

<span data-ttu-id="79fea-125">GREEN(11)</span><span class="sxs-lookup"><span data-stu-id="79fea-125">GREEN(11)</span></span>
  
<span data-ttu-id="79fea-126">Gibt 128 zurück, wenn das Dokument die Standardfarbpalette von Visio verwendet, wobei Dunkelgelb die Farbe mit Index 11 darstellt.</span><span class="sxs-lookup"><span data-stu-id="79fea-126">Returns 128 if the document uses the default Visio color palette, where dark yellow is the color at index 11.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="79fea-127">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="79fea-127">Example 3</span></span>

<span data-ttu-id="79fea-128">GREEN(RGB(10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="79fea-128">GREEN(RGB(10, 20, 30))</span></span>
  
<span data-ttu-id="79fea-129">Gibt 20 zurück.</span><span class="sxs-lookup"><span data-stu-id="79fea-129">Returns 20.</span></span>
  

