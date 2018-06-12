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
description: Gibt den Wert der Sättigung-Komponente eine Farbe zurück.
ms.openlocfilehash: 54f3fa68c567c2a32e8cfd37c406387cd6973ce3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797968"
---
# <a name="sat-function"></a><span data-ttu-id="d24bf-103">SAT Function</span><span class="sxs-lookup"><span data-stu-id="d24bf-103">SAT Function</span></span>

<span data-ttu-id="d24bf-104">Gibt den Wert der Sättigung-Komponente eine Farbe zurück.</span><span class="sxs-lookup"><span data-stu-id="d24bf-104">Returns the value of a color's saturation component.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d24bf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d24bf-105">Syntax</span></span>

<span data-ttu-id="d24bf-106">SAT (** *Ausdruck* **)</span><span class="sxs-lookup"><span data-stu-id="d24bf-106">SAT(** *expression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d24bf-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d24bf-107">Parameters</span></span>

|<span data-ttu-id="d24bf-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="d24bf-108">**Name**</span></span>|<span data-ttu-id="d24bf-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="d24bf-109">**Required/Optional**</span></span>|<span data-ttu-id="d24bf-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="d24bf-110">**Data Type**</span></span>|<span data-ttu-id="d24bf-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d24bf-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d24bf-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="d24bf-112">_expression_</span></span> <br/> |<span data-ttu-id="d24bf-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d24bf-113">Required</span></span>  <br/> |<span data-ttu-id="d24bf-114">**Variiert**</span><span class="sxs-lookup"><span data-stu-id="d24bf-114">**Varies**</span></span> <br/> |<span data-ttu-id="d24bf-115">Ein Index einer Farbe aus der Farbtabelle des Dokuments, ein Ausdruck, der zu einer benutzerdefinierten Farbe (wie RGB oder HSL) aufgelöst wird, oder ein Bezug auf eine Zelle, die einen Farbindex oder ein Farbergebnis enthält.</span><span class="sxs-lookup"><span data-stu-id="d24bf-115">An index of a color in the document's color table, an expression that resolves to a custom color (like RGB or HSL), or a reference to a cell that contains a color index or color result.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="d24bf-116">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="d24bf-116">Return value</span></span>

<span data-ttu-id="d24bf-117">Numeric</span><span class="sxs-lookup"><span data-stu-id="d24bf-117">Numeric</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d24bf-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d24bf-118">Remarks</span></span>

<span data-ttu-id="d24bf-p101">Der Rückgabewert ist eine Zahl im Bereich von 0 bis einschließlich 240. Bei einer ungültigen Eingabe wird 0 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d24bf-p101">The return value is a number in the range 0 to 240, inclusive. The function returns 0 for invalid input.</span></span>
  
## <a name="example-1"></a><span data-ttu-id="d24bf-121">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d24bf-121">Example 1</span></span>

<span data-ttu-id="d24bf-122">SAT (Sheet4! FillForegnd)</span><span class="sxs-lookup"><span data-stu-id="d24bf-122">SAT(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="d24bf-123">Gibt den Wert der Sättigung der Vordergrundfüllfarbe von Sheet.4 zurück.</span><span class="sxs-lookup"><span data-stu-id="d24bf-123">Returns the saturation of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="d24bf-124">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d24bf-124">Example 2</span></span>

<span data-ttu-id="d24bf-125">SAT(8)</span><span class="sxs-lookup"><span data-stu-id="d24bf-125">SAT(8)</span></span>
  
<span data-ttu-id="d24bf-126">Gibt 240 zurück, wenn das Dokument die Farbpalette von Visio verwendet, wobei Dunkelrot die Farbe mit Index 8 ist.</span><span class="sxs-lookup"><span data-stu-id="d24bf-126">Returns 240 if the document uses the default Visio color palette, where dark red is the color at index 8.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="d24bf-127">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="d24bf-127">Example 3</span></span>

<span data-ttu-id="d24bf-128">SAT(HSL(10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="d24bf-128">SAT(HSL(10, 20, 30))</span></span>
  
<span data-ttu-id="d24bf-129">Gibt 20 zurück.</span><span class="sxs-lookup"><span data-stu-id="d24bf-129">Returns 20.</span></span>
  

