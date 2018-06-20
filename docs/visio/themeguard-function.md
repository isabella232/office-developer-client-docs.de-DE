---
title: THEMEGUARD-Funktion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a556eadc-9ee6-7a29-ca05-6250b612790c
description: Schützt die Formatierungen Zellen eines Shapes, um sicherzustellen, dass sie entsprechende Aspekte des aktuellen Designs verwenden.
ms.openlocfilehash: 10a7772995b9cc22e53ff577b2f663d7c97d0816
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798265"
---
# <a name="themeguard-function"></a><span data-ttu-id="fd87e-103">THEMEGUARD Function</span><span class="sxs-lookup"><span data-stu-id="fd87e-103">THEMEGUARD Function</span></span>

<span data-ttu-id="fd87e-104">Schützt die Formatierungen Zellen eines Shapes, um sicherzustellen, dass sie entsprechende Aspekte des aktuellen Designs verwenden.</span><span class="sxs-lookup"><span data-stu-id="fd87e-104">Guards the formatting cells of a shape to ensure that they use appropriate aspects of the current theme.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="fd87e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd87e-105">Syntax</span></span>

<span data-ttu-id="fd87e-106">THEMEGUARD()</span><span class="sxs-lookup"><span data-stu-id="fd87e-106">THEMEGUARD()</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fd87e-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd87e-107">Remarks</span></span>

<span data-ttu-id="fd87e-108">Anwenden der THEMEGUARD-Funktion auf eine Zelle ist nicht für die manuelle Formatierung auf die gleiche Weise, die die GUARD anwenden Funktion schützen.</span><span class="sxs-lookup"><span data-stu-id="fd87e-108">Applying the THEMEGUARD function to a cell does not guard against manual formatting in the same way that applying the GUARD function does.</span></span> <span data-ttu-id="fd87e-109">Wenn Sie die Formatierung auf die Form in der Benutzeroberfläche oder programmgesteuert mittels Automatisierung anwenden, wird die Formel THEMEGUARD überschrieben, sofern Sie nicht die SETATREFEXPR-Funktion in der Formel, um die manuelle Formatierung Wert zu speichern.</span><span class="sxs-lookup"><span data-stu-id="fd87e-109">If you apply formatting to the shape in the user interface or programmatically, by means of Automation, the THEMEGUARD formula is overridden, unless you include the SETATREFEXPR function in the formula to store the manual formatting value.</span></span> 
  
## <a name="example"></a><span data-ttu-id="fd87e-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="fd87e-110">Example</span></span>

```vb
Shape.FillForegnd = THEMEGUARD(THEME("AccentColor2")
```

<span data-ttu-id="fd87e-111">Gibt an, dass das Shape die Farbe "Akzent 2" aus dem aktuellen Design anstelle der Füllfarbe des Hauptdesigns verwendet.</span><span class="sxs-lookup"><span data-stu-id="fd87e-111">Specifies that the shape take the Accent 2 color from the current theme, rather than the main theme fill color.</span></span>
  

