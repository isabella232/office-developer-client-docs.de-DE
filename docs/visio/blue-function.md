---
title: BLUE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251402
localization_priority: Normal
ms.assetid: da9fb933-4e2c-3e2a-1879-6e70db0cd830
description: Gibt die Blaukomponente einer Farbe zurück. Der Rückgabewert ist eine ganze Zahl im Bereich von 0 bis einschließlich 255. Die Funktion gibt 0 für ungültige Eingabe.
ms.openlocfilehash: 6a86a0ee91054c89f2def95c0e3521508462bdaa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796530"
---
# <a name="blue-function"></a><span data-ttu-id="ddfe2-105">BLUE Function</span><span class="sxs-lookup"><span data-stu-id="ddfe2-105">BLUE Function</span></span>

<span data-ttu-id="ddfe2-106">Gibt die Blaukomponente einer Farbe zurück.</span><span class="sxs-lookup"><span data-stu-id="ddfe2-106">Returns the blue component of a color.</span></span> <span data-ttu-id="ddfe2-107">Der Rückgabewert ist eine ganze Zahl im Bereich von 0 bis einschließlich 255.</span><span class="sxs-lookup"><span data-stu-id="ddfe2-107">The return value is an integer in the range of 0 to 255, inclusive.</span></span> <span data-ttu-id="ddfe2-108">Die Funktion gibt 0 für ungültige Eingabe.</span><span class="sxs-lookup"><span data-stu-id="ddfe2-108">The function returns 0 for invalid input.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="ddfe2-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ddfe2-109">Syntax</span></span>

<span data-ttu-id="ddfe2-110">BLUE (** *Ausdruck* **)</span><span class="sxs-lookup"><span data-stu-id="ddfe2-110">BLUE(** *expression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ddfe2-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ddfe2-111">Parameters</span></span>

|<span data-ttu-id="ddfe2-112">**Name**</span><span class="sxs-lookup"><span data-stu-id="ddfe2-112">**Name**</span></span>|<span data-ttu-id="ddfe2-113">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="ddfe2-113">**Required/Optional**</span></span>|<span data-ttu-id="ddfe2-114">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="ddfe2-114">**Data Type**</span></span>|<span data-ttu-id="ddfe2-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ddfe2-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ddfe2-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="ddfe2-116">_expression_</span></span> <br/> |<span data-ttu-id="ddfe2-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ddfe2-117">Required</span></span>  <br/> |<span data-ttu-id="ddfe2-118">**String**</span><span class="sxs-lookup"><span data-stu-id="ddfe2-118">**String**</span></span> <br/> |<span data-ttu-id="ddfe2-119">Ein Index einer Farbe aus der Farbtabelle des Dokuments, ein Ausdruck, der zu einer benutzerdefinierten Farbe (wie RGB oder HSL) aufgelöst wird, oder ein Bezug auf eine Zelle, die einen Farbindex oder ein Farbergebnis enthält.</span><span class="sxs-lookup"><span data-stu-id="ddfe2-119">An index of a color in the document's color table, an expression that resolves to a custom color (like RGB or HSL), or a reference to a cell that contains a color index or color result.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="ddfe2-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ddfe2-120">Return value</span></span>

<span data-ttu-id="ddfe2-121">Integer</span><span class="sxs-lookup"><span data-stu-id="ddfe2-121">Integer</span></span>
  
## <a name="example-1"></a><span data-ttu-id="ddfe2-122">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ddfe2-122">Example 1</span></span>

<span data-ttu-id="ddfe2-123">Blau (Sheet4! FillForegnd)</span><span class="sxs-lookup"><span data-stu-id="ddfe2-123">BLUE(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="ddfe2-124">Gibt die Blaukomponente der Vordergrundfüllfarbe von Sheet.4 zurück.</span><span class="sxs-lookup"><span data-stu-id="ddfe2-124">Returns the blue component of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="ddfe2-125">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ddfe2-125">Example 2</span></span>

<span data-ttu-id="ddfe2-126">BLUE(13)</span><span class="sxs-lookup"><span data-stu-id="ddfe2-126">BLUE(13)</span></span>
  
<span data-ttu-id="ddfe2-127">Gibt 128 zurück, wenn das Dokument die Standardfarbpalette von Visio verwendet, wobei Cyan die Farbe mit Index 13 ist.</span><span class="sxs-lookup"><span data-stu-id="ddfe2-127">Returns 128 if the document uses the default Visio color palette, where cyan is the color at index 13.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="ddfe2-128">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="ddfe2-128">Example 3</span></span>

<span data-ttu-id="ddfe2-129">BLUE(RGB(10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="ddfe2-129">BLUE(RGB(10, 20, 30))</span></span>
  
<span data-ttu-id="ddfe2-130">Gibt 30 zurück.</span><span class="sxs-lookup"><span data-stu-id="ddfe2-130">Returns 30.</span></span>
  

