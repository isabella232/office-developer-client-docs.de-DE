---
title: Informationen zu Funktionen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251825
localization_priority: Normal
ms.assetid: 871b8601-8117-bc51-17b9-6002234b4bfb
description: 'Eine Funktion führt eine einzelne wohldefinierte Aufgabe aus. Die meisten Funktionen akzeptieren eine bestimmte Anzahl von Argumenten als Eingabe. Obwohl der Typ und die Anzahl von Argumenten von der Funktion abhängen, verwenden sämtliche Funktionen dieselbe allgemeine Syntax:'
ms.openlocfilehash: 21cf02d1bb3d6a33daa10ba62efc29c5b35a11cf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796369"
---
# <a name="about-functions"></a><span data-ttu-id="dd5b0-105">Informationen zu Funktionen</span><span class="sxs-lookup"><span data-stu-id="dd5b0-105">About Functions</span></span>

<span data-ttu-id="dd5b0-p102">Eine Funktion führt eine einzelne wohldefinierte Aufgabe aus. Die meisten Funktionen akzeptieren eine bestimmte Anzahl von Argumenten als Eingabe. Obwohl der Typ und die Anzahl von Argumenten von der Funktion abhängen, verwenden sämtliche Funktionen dieselbe allgemeine Syntax:</span><span class="sxs-lookup"><span data-stu-id="dd5b0-p102">A function performs a single well-defined task. Most functions take a number of arguments as input. Although the type and number of arguments depend on the function, all functions have the same general syntax:</span></span>
  
 <span data-ttu-id="dd5b0-109">**Funktion (** _argument1_, _argument2_,...</span><span class="sxs-lookup"><span data-stu-id="dd5b0-109">**FUNCTION(** _argument1_,  _argument2_, …</span></span>  <span data-ttu-id="dd5b0-110">_argumentN_ [, _Argumenta|_ |  _Argument_ **])**</span><span class="sxs-lookup"><span data-stu-id="dd5b0-110">_argumentN_ [,  _argumentA_ |  _argument_ **])**</span></span>
  
|<span data-ttu-id="dd5b0-111">**Syntaxelement**</span><span class="sxs-lookup"><span data-stu-id="dd5b0-111">**Syntax element**</span></span>|<span data-ttu-id="dd5b0-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dd5b0-112">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="dd5b0-113">( )</span><span class="sxs-lookup"><span data-stu-id="dd5b0-113"></span></span>  <br/> | <span data-ttu-id="dd5b0-114">Wenn eine Funktion keine Argumente akzeptiert, muss ihr ein leerer Satz Klammern () folgen.</span><span class="sxs-lookup"><span data-stu-id="dd5b0-114">If a function takes no arguments, it must be followed by an empty set of parentheses ( ).</span></span>  <br/> |
| <span data-ttu-id="dd5b0-115">,</span><span class="sxs-lookup"><span data-stu-id="dd5b0-115"></span></span>  <br/> | <span data-ttu-id="dd5b0-116">Argumente werden durch ein Komma getrennt.</span><span class="sxs-lookup"><span data-stu-id="dd5b0-116">Arguments are separated by a comma.</span></span>  <br/> |
| <span data-ttu-id="dd5b0-117">...</span><span class="sxs-lookup"><span data-stu-id="dd5b0-117"></span></span>  <br/> | <span data-ttu-id="dd5b0-118">Wird nur zur Notation verwendet, nicht in eine Funktion einfügen.</span><span class="sxs-lookup"><span data-stu-id="dd5b0-118">Used for notation only; do not include in a function.</span></span>  <br/> |
| <span data-ttu-id="dd5b0-119">[ ]</span><span class="sxs-lookup"><span data-stu-id="dd5b0-119"></span></span>  <br/> | <span data-ttu-id="dd5b0-p104">Optionales Argument. Wird nur zur Notation verwendet, nicht in eine Funktion einfügen.</span><span class="sxs-lookup"><span data-stu-id="dd5b0-p104">Optional argument. Used for notation only; do not include in a function.</span></span>  <br/> |
| |  <br/> | <span data-ttu-id="dd5b0-122">Wahl; Sie können _Argumenta|_ oder _Argument_enthalten.</span><span class="sxs-lookup"><span data-stu-id="dd5b0-122">A choice; you can include  _argumentA_ or  _argument_.</span></span> <span data-ttu-id="dd5b0-123">Wird nur zur Notation verwendet, nicht in eine Funktion einfügen.</span><span class="sxs-lookup"><span data-stu-id="dd5b0-123">Used for notation only; do not include in a function.</span></span>  <br/> |
   
<span data-ttu-id="dd5b0-p106">Viele Funktionen, die Sie in Formeln verwenden können, ähneln denen, die Sie bereits in Tabellenkalkulationsprogrammen gesehen haben: mathematische Funktionen wie SUM oder SQRT; trigonometrische Funktionen wie SIN oder COS oder logische Funktionen wie IF oder NOT. Viele andere Funktionen stehen nur in Microsoft Office Visio zur Verfügung, z. B. GUARD, GRAVITY und RUNADDON.</span><span class="sxs-lookup"><span data-stu-id="dd5b0-p106">Many functions that you can use in formulas resemble those you have seen in spreadsheet programs: mathematical, such as SUM or SQRT; trigonometric, such as SIN or COS; or logical, such as IF or NOT. Many other functions are unique to Microsoft Office Visio, such as GUARD, GRAVITY, and RUNADDON.</span></span>
  
<span data-ttu-id="dd5b0-126">Weitere Informationen zu bestimmten Funktionen finden Sie in dieser ShapeSheet-Referenz.</span><span class="sxs-lookup"><span data-stu-id="dd5b0-126">For more information on specific functions, see this ShapeSheet Reference.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="dd5b0-127">Bestimmte Funktionen werden werden in durch Visio generierten Formeln jedoch nicht dargestellt im Dialogfeld **Formel bearbeiten** oder in dieser Referenz beschrieben, da sie für die interne Verwendung reserviert sind und nicht in anderen Formeln verwendet werden sollte.</span><span class="sxs-lookup"><span data-stu-id="dd5b0-127">Certain functions appear in formulas generated by Visio, but are not shown in the **Edit Formula** dialog box or described in this reference because they are reserved for internal use and should not be used in other formulas.</span></span> <span data-ttu-id="dd5b0-128">Es folgen Beispiele: ELLIPSE_THETA, _ELLIPSE_ECC, _UCON_C1 und _SHAPEMIN.</span><span class="sxs-lookup"><span data-stu-id="dd5b0-128">Following are examples: ELLIPSE_THETA, _ELLIPSE_ECC, _UCON_C1, and _SHAPEMIN.</span></span> 
  

