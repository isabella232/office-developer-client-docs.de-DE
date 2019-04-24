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
description: Gibt die grüne Komponente einer Farbe zurück.
ms.openlocfilehash: 0412e4519c2964b05d7663805d7773e8dc5deaab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360207"
---
# <a name="green-function"></a><span data-ttu-id="3fba3-103">GREEN Function</span><span class="sxs-lookup"><span data-stu-id="3fba3-103">GREEN Function</span></span>

<span data-ttu-id="3fba3-104">Gibt die grüne Komponente einer Farbe zurück.</span><span class="sxs-lookup"><span data-stu-id="3fba3-104">Returns the green component of a color.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="3fba3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3fba3-105">Syntax</span></span>

<span data-ttu-id="3fba3-106">Grün (\* \* *Ausdruck* \* \*)</span><span class="sxs-lookup"><span data-stu-id="3fba3-106">GREEN(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3fba3-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="3fba3-107">Parameters</span></span>

|<span data-ttu-id="3fba3-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="3fba3-108">**Name**</span></span>|<span data-ttu-id="3fba3-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="3fba3-109">**Required/Optional**</span></span>|<span data-ttu-id="3fba3-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="3fba3-110">**Data Type**</span></span>|<span data-ttu-id="3fba3-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3fba3-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3fba3-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="3fba3-112">_expression_</span></span> <br/> |<span data-ttu-id="3fba3-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="3fba3-113">Required</span></span>  <br/> |<span data-ttu-id="3fba3-114">**Variiert**</span><span class="sxs-lookup"><span data-stu-id="3fba3-114">**Varies**</span></span> <br/> |<span data-ttu-id="3fba3-115">Ein Index einer Farbe in der Farbtabelle des Dokuments, ein Ausdruck, der in eine benutzerdefinierte Farbe (wie RGB oder GSL) aufgelöst wird, oder ein Bezug auf eine Zelle, die einen Farbindex oder ein Farbergebnis enthält.</span><span class="sxs-lookup"><span data-stu-id="3fba3-115">An index of a color in the document's color table, an expression that resolves to a custom color (such as RGB or HSL), or a reference to a cell that contains a color index or color result.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="3fba3-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3fba3-116">Return value</span></span>

<span data-ttu-id="3fba3-117">Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="3fba3-117">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3fba3-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3fba3-118">Remarks</span></span>

<span data-ttu-id="3fba3-119">Der Rückgabewert ist eine Zahl im Bereich von 0 bis einschließlich 255, oder ein Zellbezug, der als Index aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="3fba3-119">The return value is a number in the range 0 to 255, inclusive, or a cell reference that resolves to an index.</span></span> <span data-ttu-id="3fba3-120">Wenn *Ausdruck* ungültig ist, gibt er 0 (schwarz) zurück.</span><span class="sxs-lookup"><span data-stu-id="3fba3-120">If  *expression*  is invalid, it returns 0 (black).</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="3fba3-121">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3fba3-121">Example 1</span></span>

<span data-ttu-id="3fba3-122">Grün (Blatt. 4! Zelle FillForegnd</span><span class="sxs-lookup"><span data-stu-id="3fba3-122">GREEN(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="3fba3-123">Gibt den Wert der Grünkomponente der Vordergrundfüllfarbe von Sheet.4 zurück.</span><span class="sxs-lookup"><span data-stu-id="3fba3-123">Returns the green component of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="3fba3-124">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3fba3-124">Example 2</span></span>

<span data-ttu-id="3fba3-125">GRÜN (11)</span><span class="sxs-lookup"><span data-stu-id="3fba3-125">GREEN(11)</span></span>
  
<span data-ttu-id="3fba3-126">Gibt 128 zurück, wenn das Dokument die Standardfarbpalette von Visio verwendet, wobei Dunkelgelb die Farbe mit Index 11 darstellt.</span><span class="sxs-lookup"><span data-stu-id="3fba3-126">Returns 128 if the document uses the default Visio color palette, where dark yellow is the color at index 11.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="3fba3-127">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="3fba3-127">Example 3</span></span>

<span data-ttu-id="3fba3-128">GREEN(RGB(10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="3fba3-128">GREEN(RGB(10, 20, 30))</span></span>
  
<span data-ttu-id="3fba3-129">Gibt 20 zurück.</span><span class="sxs-lookup"><span data-stu-id="3fba3-129">Returns 20.</span></span>
  

