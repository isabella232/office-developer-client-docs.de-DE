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
ms.openlocfilehash: 14995b0f7e3c1cc8346d47965038902b8ca4e8bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415978"
---
# <a name="about-functions"></a><span data-ttu-id="d0d21-105">Informationen zu Funktionen</span><span class="sxs-lookup"><span data-stu-id="d0d21-105">About Functions</span></span>

<span data-ttu-id="d0d21-p102">Eine Funktion führt eine einzelne wohldefinierte Aufgabe aus. Die meisten Funktionen akzeptieren eine bestimmte Anzahl von Argumenten als Eingabe. Obwohl der Typ und die Anzahl von Argumenten von der Funktion abhängen, verwenden sämtliche Funktionen dieselbe allgemeine Syntax:</span><span class="sxs-lookup"><span data-stu-id="d0d21-p102">A function performs a single well-defined task. Most functions take a number of arguments as input. Although the type and number of arguments depend on the function, all functions have the same general syntax:</span></span>
  
 <span data-ttu-id="d0d21-109">**FUNCTION(** _argument1_,  _argument2_, ...</span><span class="sxs-lookup"><span data-stu-id="d0d21-109">**FUNCTION(** _argument1_,  _argument2_, …</span></span>  <span data-ttu-id="d0d21-110">_argumentN_ [, _argumentA_  |   _argument_ **])**</span><span class="sxs-lookup"><span data-stu-id="d0d21-110">_argumentN_ [,  _argumentA_ |  _argument_ **])**</span></span>
  
|<span data-ttu-id="d0d21-111">**Syntaxelement**</span><span class="sxs-lookup"><span data-stu-id="d0d21-111">**Syntax element**</span></span>|<span data-ttu-id="d0d21-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d0d21-112">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="d0d21-113">( )</span><span class="sxs-lookup"><span data-stu-id="d0d21-113">( )</span></span>  <br/> | <span data-ttu-id="d0d21-114">Wenn eine Funktion keine Argumente akzeptiert, muss ihr ein leerer Satz Klammern () folgen.</span><span class="sxs-lookup"><span data-stu-id="d0d21-114">If a function takes no arguments, it must be followed by an empty set of parentheses ( ).</span></span>  <br/> |
| <span data-ttu-id="d0d21-115">,</span><span class="sxs-lookup"><span data-stu-id="d0d21-115">,</span></span>  <br/> | <span data-ttu-id="d0d21-116">Argumente werden durch ein Komma getrennt.</span><span class="sxs-lookup"><span data-stu-id="d0d21-116">Arguments are separated by a comma.</span></span>  <br/> |
| <span data-ttu-id="d0d21-117">...</span><span class="sxs-lookup"><span data-stu-id="d0d21-117">...</span></span>  <br/> | <span data-ttu-id="d0d21-118">Wird nur zur Notation verwendet, nicht in eine Funktion einfügen.</span><span class="sxs-lookup"><span data-stu-id="d0d21-118">Used for notation only; do not include in a function.</span></span>  <br/> |
| <span data-ttu-id="d0d21-119">[ ]</span><span class="sxs-lookup"><span data-stu-id="d0d21-119">[ ]</span></span>  <br/> | <span data-ttu-id="d0d21-p104">Optionales Argument. Wird nur zur Notation verwendet, nicht in eine Funktion einfügen.</span><span class="sxs-lookup"><span data-stu-id="d0d21-p104">Optional argument. Used for notation only; do not include in a function.</span></span>  <br/> |
| |  <br/> | <span data-ttu-id="d0d21-122">Eine Auswahl; Sie können _argumentA oder_ argument _enthalten._</span><span class="sxs-lookup"><span data-stu-id="d0d21-122">A choice; you can include  _argumentA_ or  _argument_.</span></span> <span data-ttu-id="d0d21-123">Wird nur zur Notation verwendet, nicht in eine Funktion einfügen.</span><span class="sxs-lookup"><span data-stu-id="d0d21-123">Used for notation only; do not include in a function.</span></span>  <br/> |
   
<span data-ttu-id="d0d21-p106">Viele Funktionen, die Sie in Formeln verwenden können, ähneln denen, die Sie bereits in Tabellenkalkulationsprogrammen gesehen haben: mathematische Funktionen wie SUM oder SQRT; trigonometrische Funktionen wie SIN oder COS oder logische Funktionen wie IF oder NOT. Viele andere Funktionen stehen nur in Microsoft Office Visio zur Verfügung, z. B. GUARD, GRAVITY und RUNADDON.</span><span class="sxs-lookup"><span data-stu-id="d0d21-p106">Many functions that you can use in formulas resemble those you have seen in spreadsheet programs: mathematical, such as SUM or SQRT; trigonometric, such as SIN or COS; or logical, such as IF or NOT. Many other functions are unique to Microsoft Office Visio, such as GUARD, GRAVITY, and RUNADDON.</span></span>
  
<span data-ttu-id="d0d21-126">Weitere Informationen zu bestimmten Funktionen finden Sie in dieser ShapeSheet-Referenz.</span><span class="sxs-lookup"><span data-stu-id="d0d21-126">For more information on specific functions, see this ShapeSheet Reference.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="d0d21-127">Bestimmte Funktionen werden in von Visio generierten Formeln angezeigt, werden jedoch nicht im Dialogfeld Formel bearbeiten angezeigt oder in diesem Verweis beschrieben, da sie für die interne Verwendung reserviert sind und nicht in anderen Formeln verwendet werden sollten. </span><span class="sxs-lookup"><span data-stu-id="d0d21-127">Certain functions appear in formulas generated by Visio, but are not shown in the **Edit Formula** dialog box or described in this reference because they are reserved for internal use and should not be used in other formulas.</span></span> <span data-ttu-id="d0d21-128">Dazu gehören beispielsweise die folgenden Formeln: ELLIPSE_THETA, _ELLIPSE_ECC, _UCON_C1 und _SHAPEMIN.</span><span class="sxs-lookup"><span data-stu-id="d0d21-128">Following are examples: ELLIPSE_THETA, _ELLIPSE_ECC, _UCON_C1, and _SHAPEMIN.</span></span> 
  

