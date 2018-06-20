---
title: THEMECBV Function
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ef62f63f-b2ce-4d12-a294-93dbdc9a869d
description: Gibt einen RGB-Wert oder eine ganze Zahl, die einen Index in der Farbpalette des Dokuments darstellt, in dem die Farbe (Anzahl) als Argument übergeben wurde durch den angegebenen Farbton oder eine Schattierung Wert in den Farbverlauf Einstellungen des aktiven Designs gespeichert geändert wurden.
ms.openlocfilehash: 878da505a840234445d3e16d3b8a68e31eaf5fda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798272"
---
# <a name="themecbv-function"></a><span data-ttu-id="e924a-103">THEMECBV Function</span><span class="sxs-lookup"><span data-stu-id="e924a-103">THEMECBV Function</span></span>

<span data-ttu-id="e924a-104">Gibt einen RGB-Wert oder eine ganze Zahl, die einen Index in der Farbpalette des Dokuments darstellt, in dem die Farbe (Anzahl) als Argument übergeben wurde durch den angegebenen Farbton oder eine Schattierung Wert in den Farbverlauf Einstellungen des aktiven Designs gespeichert geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="e924a-104">Returns an RGB value or an integer that represents an index in the document's color palette, where the color (number) passed in as an argument has been modified by the specified tint or shade value stored in the gradient settings of the active theme.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="e924a-105">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="e924a-105">Version Information</span></span>

<span data-ttu-id="e924a-106">Hinzugefügte Version: Visio 2013</span><span class="sxs-lookup"><span data-stu-id="e924a-106">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e924a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e924a-107">Syntax</span></span>

 <span data-ttu-id="e924a-108">**THEMECBV** ( _Farbe_, _Gradient_stop_number_)</span><span class="sxs-lookup"><span data-stu-id="e924a-108">**THEMECBV**( _color_,  _gradient_stop_number_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="e924a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e924a-109">Parameters</span></span>

|<span data-ttu-id="e924a-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="e924a-110">**Name**</span></span>|<span data-ttu-id="e924a-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="e924a-111">**Required/Optional**</span></span>|<span data-ttu-id="e924a-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="e924a-112">**Data Type**</span></span>|<span data-ttu-id="e924a-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e924a-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e924a-114">_Farbe_</span><span class="sxs-lookup"><span data-stu-id="e924a-114">_color_</span></span> <br/> |<span data-ttu-id="e924a-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e924a-115">Required</span></span>  <br/> |<span data-ttu-id="e924a-116">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="e924a-116">**Number**</span></span> <br/> |<span data-ttu-id="e924a-117">Eine Zahl, die einen Index in der Farbpalette des Dokuments darstellt.</span><span class="sxs-lookup"><span data-stu-id="e924a-117">A number representing an index in the document's color palette.</span></span>  <br/> |
| <span data-ttu-id="e924a-118">_gradient_stop_number_</span><span class="sxs-lookup"><span data-stu-id="e924a-118">_gradient_stop_number_</span></span> <br/> |<span data-ttu-id="e924a-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e924a-119">Required</span></span>  <br/> |<span data-ttu-id="e924a-120">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="e924a-120">**Number**</span></span> <br/> |<span data-ttu-id="e924a-121">Farbverlaufstopp (Farbton oder eine Schattierung) in den Farbverlauf Einstellungen des aktiven Designs auf die Farbe anwenden gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e924a-121">The gradient stop (tint or shade) stored in the gradient settings of the active theme to apply to the color.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="e924a-122">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="e924a-122">Return value</span></span>

 <span data-ttu-id="e924a-123">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="e924a-123">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e924a-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e924a-124">Remarks</span></span>

> [!NOTE]
> <span data-ttu-id="e924a-125">Die THEMECBV-Funktion hat keine Auswirkung auf die Farbe als Argument übergeben wird, wenn die QuickStyle, die mit dem Shape zugewiesen ist keinen Farbverlauf verfügt.</span><span class="sxs-lookup"><span data-stu-id="e924a-125">The THEMECBV function does nothing to the color passed in as an argument if the QuickStyle that is assigned to the shape does not have a gradient.</span></span> 
  
<span data-ttu-id="e924a-126">Die Farbverlauf Einstellungen in einem Design sind eine Reihe von nummerierten Farbverlaufstopps, die ein "Aufhellen" (Farbton) oder "Abdunkeln" (Schatten) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e924a-126">The gradient settings in a theme are a series of numbered gradient stops that correspond to a "lightening" (tint) or "darkening" (shade).</span></span> <span data-ttu-id="e924a-127">Diese Graustufen und Farbtöne gelten für eine Basis Farbe, um einen Farbverlauf Effekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e924a-127">These shades and tints are applied to a base color to create a gradient color effect.</span></span>
  
<span data-ttu-id="e924a-128">Die **THEMECBV** -Funktion übernimmt eine Farbe Eingabe und gibt die Farbe aus, nachdem es durch den Farbton oder die Schattierung des angegebenen Farbverlaufstopps geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="e924a-128">The **THEMECBV** function takes a color input and outputs the color after it has been modified by the tint or shade of the specified gradient stop.</span></span> <span data-ttu-id="e924a-129">Die Farbtöne und Schattierungen stammen das Design-Definition, wenn die aktuelle Schnellformatvorlage für eine graduelle Füllung enthält.</span><span class="sxs-lookup"><span data-stu-id="e924a-129">The tints and shades come from the theme's definition, if the current quick style contains a gradient fill.</span></span> <span data-ttu-id="e924a-130">Wenn die aktive Schnellformatvorlage keine angegeben wird, dass eine graduelle Füllung oder auf das Shape kein Design festgelegt ist, gibt diese Formel einfach die Farbe, die für das erste Argument übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="e924a-130">If the active Quick Style does not specify a gradient fill or the shape is set to No Theme, then this formula simply returns the color that was passed in for the first argument.</span></span> 
  
## <a name="example"></a><span data-ttu-id="e924a-131">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e924a-131">Example</span></span>

 `THEMECBV(FillForegnd, 5)`
  
<span data-ttu-id="e924a-132">Gibt die Farbe erstellt wird, den Farbton oder die Schattierung in der fünften Farbverlaufstopp des Farbverlaufs auf die in die Zelle **FillForegnd** angegebene Farbe angewendet.</span><span class="sxs-lookup"><span data-stu-id="e924a-132">Returns the color created by applying the tint or shade in the fifth gradient stop of the gradient to the color specified in the **FillForegnd** cell.</span></span> 
  
 `THEMECBV(RGB(255,0,0), 2)`
  
<span data-ttu-id="e924a-133">Gibt eine Schattierung oder einen Farbton durch Anwenden des zweiten Unterbrechungspunkts auf einen Basiskalender Farbe Rot erstellten Rot fest.</span><span class="sxs-lookup"><span data-stu-id="e924a-133">Returns a shade or tint of red created by applying the second gradient stop to a base color of red.</span></span>
  

