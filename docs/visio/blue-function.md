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
description: Gibt die blaue Komponente einer Farbe zurück. Der Rückgabewert ist eine ganze Zahl im Wertebereich von 0 bis 255. Bei einer ungültigen Eingabe wird 0 zurückgegeben.
ms.openlocfilehash: adefbe0f8c2df0ead0f3e50cd5d4945501972865
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439037"
---
# <a name="blue-function"></a><span data-ttu-id="15d1f-105">BLUE Function</span><span class="sxs-lookup"><span data-stu-id="15d1f-105">BLUE Function</span></span>

<span data-ttu-id="15d1f-106">Gibt die blaue Komponente einer Farbe zurück.</span><span class="sxs-lookup"><span data-stu-id="15d1f-106">Returns the blue component of a color.</span></span> <span data-ttu-id="15d1f-107">Der Rückgabewert ist eine ganze Zahl im Wertebereich von 0 bis 255.</span><span class="sxs-lookup"><span data-stu-id="15d1f-107">The return value is an integer in the range of 0 to 255, inclusive.</span></span> <span data-ttu-id="15d1f-108">Bei einer ungültigen Eingabe wird 0 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="15d1f-108">The function returns 0 for invalid input.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="15d1f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="15d1f-109">Syntax</span></span>

<span data-ttu-id="15d1f-110">BLAU (\* \* *Ausdruck* \* \*)</span><span class="sxs-lookup"><span data-stu-id="15d1f-110">BLUE(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="15d1f-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="15d1f-111">Parameters</span></span>

|<span data-ttu-id="15d1f-112">**Name**</span><span class="sxs-lookup"><span data-stu-id="15d1f-112">**Name**</span></span>|<span data-ttu-id="15d1f-113">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="15d1f-113">**Required/Optional**</span></span>|<span data-ttu-id="15d1f-114">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="15d1f-114">**Data Type**</span></span>|<span data-ttu-id="15d1f-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="15d1f-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="15d1f-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="15d1f-116">_expression_</span></span> <br/> |<span data-ttu-id="15d1f-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="15d1f-117">Required</span></span>  <br/> |<span data-ttu-id="15d1f-118">**String**</span><span class="sxs-lookup"><span data-stu-id="15d1f-118">**String**</span></span> <br/> |<span data-ttu-id="15d1f-119">Ein Index einer Farbe aus der Farbtabelle des Dokuments, ein Ausdruck, der zu einer benutzerdefinierten Farbe (wie RGB oder HSL) aufgelöst wird, oder ein Bezug auf eine Zelle, die einen Farbindex oder ein Farbergebnis enthält.</span><span class="sxs-lookup"><span data-stu-id="15d1f-119">An index of a color in the document's color table, an expression that resolves to a custom color (like RGB or HSL), or a reference to a cell that contains a color index or color result.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="15d1f-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="15d1f-120">Return value</span></span>

<span data-ttu-id="15d1f-121">Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="15d1f-121">Integer</span></span>
  
## <a name="example-1"></a><span data-ttu-id="15d1f-122">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="15d1f-122">Example 1</span></span>

<span data-ttu-id="15d1f-123">BLAU (Blatt. 4! Zelle FillForegnd</span><span class="sxs-lookup"><span data-stu-id="15d1f-123">BLUE(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="15d1f-124">Gibt die Blaukomponente der Vordergrundfüllfarbe von Sheet.4 zurück.</span><span class="sxs-lookup"><span data-stu-id="15d1f-124">Returns the blue component of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="15d1f-125">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="15d1f-125">Example 2</span></span>

<span data-ttu-id="15d1f-126">BLAU (13)</span><span class="sxs-lookup"><span data-stu-id="15d1f-126">BLUE(13)</span></span>
  
<span data-ttu-id="15d1f-127">Gibt 128 zurück, wenn das Dokument die Standardfarbpalette von Visio verwendet, wobei Cyan die Farbe mit Index 13 ist.</span><span class="sxs-lookup"><span data-stu-id="15d1f-127">Returns 128 if the document uses the default Visio color palette, where cyan is the color at index 13.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="15d1f-128">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="15d1f-128">Example 3</span></span>

<span data-ttu-id="15d1f-129">BLUE(RGB(10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="15d1f-129">BLUE(RGB(10, 20, 30))</span></span>
  
<span data-ttu-id="15d1f-130">Gibt 30 zurück.</span><span class="sxs-lookup"><span data-stu-id="15d1f-130">Returns 30.</span></span>
  

