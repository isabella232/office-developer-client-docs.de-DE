---
title: THEMECBV Function
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ef62f63f-b2ce-4d12-a294-93dbdc9a869d
description: Gibt einen RGB-Wert oder eine ganze Zahl zurück, die einen Index in der Farbpalette des Dokuments darstellt, wobei die Farbe (Zahl), die als Argument übergeben wurde, durch den angegebenen Farbton oder Farbton geändert wurde, der in den Farbverlaufseinstellungen des aktiven Designs gespeichert ist.
ms.openlocfilehash: 014dc04c5114e296cd2226f3cf04dfb729817578
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429138"
---
# <a name="themecbv-function"></a><span data-ttu-id="8f7fb-103">THEMECBV Function</span><span class="sxs-lookup"><span data-stu-id="8f7fb-103">THEMECBV Function</span></span>

<span data-ttu-id="8f7fb-104">Gibt einen RGB-Wert oder eine ganze Zahl zurück, die einen Index in der Farbpalette des Dokuments darstellt, wobei die Farbe (Zahl), die als Argument übergeben wurde, durch den angegebenen Farbton oder Farbton geändert wurde, der in den Farbverlaufseinstellungen des aktiven Designs gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="8f7fb-104">Returns an RGB value or an integer that represents an index in the document's color palette, where the color (number) passed in as an argument has been modified by the specified tint or shade value stored in the gradient settings of the active theme.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="8f7fb-105">Informationen zur Version</span><span class="sxs-lookup"><span data-stu-id="8f7fb-105">Version Information</span></span>

<span data-ttu-id="8f7fb-106">Hinzugefügte Version: Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="8f7fb-106">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8f7fb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f7fb-107">Syntax</span></span>

 <span data-ttu-id="8f7fb-108">**THEMECBV** ( _Farbe_, _gradient_stop_number_)</span><span class="sxs-lookup"><span data-stu-id="8f7fb-108">**THEMECBV**( _color_,  _gradient_stop_number_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="8f7fb-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f7fb-109">Parameters</span></span>

|<span data-ttu-id="8f7fb-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="8f7fb-110">**Name**</span></span>|<span data-ttu-id="8f7fb-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="8f7fb-111">**Required/Optional**</span></span>|<span data-ttu-id="8f7fb-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="8f7fb-112">**Data Type**</span></span>|<span data-ttu-id="8f7fb-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8f7fb-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8f7fb-114">_color_</span><span class="sxs-lookup"><span data-stu-id="8f7fb-114">_color_</span></span> <br/> |<span data-ttu-id="8f7fb-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8f7fb-115">Required</span></span>  <br/> |<span data-ttu-id="8f7fb-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="8f7fb-116">**Number**</span></span> <br/> |<span data-ttu-id="8f7fb-117">Eine Zahl, die einen Index in der Farbpalette des Dokuments darstellt.</span><span class="sxs-lookup"><span data-stu-id="8f7fb-117">A number representing an index in the document's color palette.</span></span>  <br/> |
| <span data-ttu-id="8f7fb-118">_gradient_stop_number_</span><span class="sxs-lookup"><span data-stu-id="8f7fb-118">_gradient_stop_number_</span></span> <br/> |<span data-ttu-id="8f7fb-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8f7fb-119">Required</span></span>  <br/> |<span data-ttu-id="8f7fb-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="8f7fb-120">**Number**</span></span> <br/> |<span data-ttu-id="8f7fb-121">Der Farbverlaufsstopp (Farbton oder Schattierung), der in den Farbverlaufseinstellungen des aktiven Designs gespeichert ist und auf die Farbe angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8f7fb-121">The gradient stop (tint or shade) stored in the gradient settings of the active theme to apply to the color.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="8f7fb-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8f7fb-122">Return value</span></span>

 <span data-ttu-id="8f7fb-123">**Number**</span><span class="sxs-lookup"><span data-stu-id="8f7fb-123">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8f7fb-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8f7fb-124">Remarks</span></span>

> [!NOTE]
> <span data-ttu-id="8f7fb-125">Die THEMECBV-Funktion bewirkt keine Farbe, die als Argument übergeben wird, wenn die QuickStyle, die dem Shape zugewiesen ist, keinen Farbverlauf aufweist.</span><span class="sxs-lookup"><span data-stu-id="8f7fb-125">The THEMECBV function does nothing to the color passed in as an argument if the QuickStyle that is assigned to the shape does not have a gradient.</span></span> 
  
<span data-ttu-id="8f7fb-126">Die Farbverlaufseinstellungen in einem Design sind eine Reihe von nummerierten Farbverlaufs Unterbrechungen, die einer "Aufhellung" (Tönung) oder "Verdunkelung" (Farbton) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="8f7fb-126">The gradient settings in a theme are a series of numbered gradient stops that correspond to a "lightening" (tint) or "darkening" (shade).</span></span> <span data-ttu-id="8f7fb-127">Diese Schattierungen und Farbtöne werden auf eine Grundfarbe angewendet, um einen Farbverlauf zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8f7fb-127">These shades and tints are applied to a base color to create a gradient color effect.</span></span>
  
<span data-ttu-id="8f7fb-128">Die **THEMECBV** -Funktion verwendet eine Farb Eingabe und gibt die Farbe aus, nachdem Sie durch den Farbton oder die Schattierung des angegebenen Farbverlaufsstopps geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="8f7fb-128">The **THEMECBV** function takes a color input and outputs the color after it has been modified by the tint or shade of the specified gradient stop.</span></span> <span data-ttu-id="8f7fb-129">Die Farbtöne und Schattierungen stammen aus der Definition des Designs, wenn die aktuelle Schnellformatvorlage eine graduelle Füllung enthält.</span><span class="sxs-lookup"><span data-stu-id="8f7fb-129">The tints and shades come from the theme's definition, if the current quick style contains a gradient fill.</span></span> <span data-ttu-id="8f7fb-130">Wenn die aktive Schnellformatvorlage keine Farbverlaufsfüllung angibt oder die Form auf kein Design festgelegt ist, gibt diese Formel einfach die Farbe zurück, die für das erste Argument übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="8f7fb-130">If the active Quick Style does not specify a gradient fill or the shape is set to No Theme, then this formula simply returns the color that was passed in for the first argument.</span></span> 
  
## <a name="example"></a><span data-ttu-id="8f7fb-131">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8f7fb-131">Example</span></span>

 `THEMECBV(FillForegnd, 5)`
  
<span data-ttu-id="8f7fb-132">Gibt die Farbe zurück, die durch Anwenden des Farbtons oder der Schattierung im fünften Farbverlaufsstopp des Farbverlaufs mit der in der Zelle **Zelle FillForegnd** angegebenen Farbe erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="8f7fb-132">Returns the color created by applying the tint or shade in the fifth gradient stop of the gradient to the color specified in the **FillForegnd** cell.</span></span> 
  
 `THEMECBV(RGB(255,0,0), 2)`
  
<span data-ttu-id="8f7fb-133">Gibt eine Schattierung oder einen Farbton rot zurück, indem der zweite Farbverlaufsstopp auf eine rote Basisfarbe angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="8f7fb-133">Returns a shade or tint of red created by applying the second gradient stop to a base color of red.</span></span>
  

