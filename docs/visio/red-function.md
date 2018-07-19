---
title: RED-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251487
localization_priority: Normal
ms.assetid: a95fd86d-ebc1-66b6-e7d9-9c8ea84d23ab
description: Gibt die Rotkomponente einer Farbe zurück.
ms.openlocfilehash: 801ebb64564df81f72c41cb720fe53f0f1b4c10d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19797769"
---
# <a name="red-function"></a><span data-ttu-id="f463a-103">RED Function</span><span class="sxs-lookup"><span data-stu-id="f463a-103">RED Function</span></span>

<span data-ttu-id="f463a-104">Gibt die Rotkomponente einer Farbe zurück.</span><span class="sxs-lookup"><span data-stu-id="f463a-104">Returns the red component of a color.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f463a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f463a-105">Syntax</span></span>

<span data-ttu-id="f463a-106">Rot (** *Ausdruck* **)</span><span class="sxs-lookup"><span data-stu-id="f463a-106">RED(** *expression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f463a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f463a-107">Parameters</span></span>

|<span data-ttu-id="f463a-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="f463a-108">**Name**</span></span>|<span data-ttu-id="f463a-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="f463a-109">**Required/Optional**</span></span>|<span data-ttu-id="f463a-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="f463a-110">**Data Type**</span></span>|<span data-ttu-id="f463a-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f463a-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f463a-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="f463a-112">_expression_</span></span> <br/> |<span data-ttu-id="f463a-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="f463a-113">Required</span></span>  <br/> |<span data-ttu-id="f463a-114">**Varies**</span><span class="sxs-lookup"><span data-stu-id="f463a-114">**Varies**</span></span> <br/> |<span data-ttu-id="f463a-115">Ein Index einer Farbe aus der Farbtabelle des Dokuments, ein Ausdruck, der zu einer benutzerdefinierten Farbe (wie RGB oder HSL) aufgelöst wird, oder ein Bezug auf eine Zelle, die einen Farbindex oder ein Farbergebnis enthält.</span><span class="sxs-lookup"><span data-stu-id="f463a-115">An index of a color in the document's color table, an expression that resolves to a custom color (like RGB or HSL), or a reference to a cell that contains a color index or color result.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="f463a-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f463a-116">Return value</span></span>

<span data-ttu-id="f463a-117">Zahl</span><span class="sxs-lookup"><span data-stu-id="f463a-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f463a-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f463a-118">Remarks</span></span>

<span data-ttu-id="f463a-119">Der Rückgabewert ist eine Zahl im Bereich von 0 bis einschließlich 255 oder Bezug auf eine Zelle, die als Index aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="f463a-119">The return value is a number in the range 0 to 255, inclusive, or a cell reference that resolves to an index.</span></span> <span data-ttu-id="f463a-120">Wenn der _Ausdruck_ ungültig ist, gibt diese Funktion 0 (Schwarz).</span><span class="sxs-lookup"><span data-stu-id="f463a-120">If  _expression_ is invalid, this function returns 0 (black).</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="f463a-121">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f463a-121">Example 1</span></span>

<span data-ttu-id="f463a-122">RED(22)</span><span class="sxs-lookup"><span data-stu-id="f463a-122">RED(22)</span></span>
  
<span data-ttu-id="f463a-123">Gibt 51 zurück, wenn das Dokument die Farbpalette von Microsoft Office Visio verwendet, wobei Dunkelgrau die Farbe mit Index 22 ist.</span><span class="sxs-lookup"><span data-stu-id="f463a-123">Returns 51 if the document uses the default Microsoft Office Visio color palette, where dark gray is the color at index 22.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="f463a-124">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f463a-124">Example 2</span></span>

<span data-ttu-id="f463a-125">Red(char.Color)</span><span class="sxs-lookup"><span data-stu-id="f463a-125">RED(Char.Color)</span></span>
  
<span data-ttu-id="f463a-126">Gibt den Wert der Rotkomponente der Farbe der aktuellen Schriftart zurück.</span><span class="sxs-lookup"><span data-stu-id="f463a-126">Returns the value of the red component of the current font color.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="f463a-127">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="f463a-127">Example 3</span></span>

<span data-ttu-id="f463a-128">RED(RGB(10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="f463a-128">RED(RGB(10, 20, 30))</span></span>
  
<span data-ttu-id="f463a-129">Gibt 10 zurück.</span><span class="sxs-lookup"><span data-stu-id="f463a-129">Returns 10.</span></span>
  

