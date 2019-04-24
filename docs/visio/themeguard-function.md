---
title: THEMEGUARD-Funktion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a556eadc-9ee6-7a29-ca05-6250b612790c
description: Schützt die Formatierungszellen eines Shapes, um sicherzustellen, dass Sie die entsprechenden Aspekte des aktuellen Designs verwenden.
ms.openlocfilehash: c20d43f9d03296a3c529a6c8f59cf27489dcdc51
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326754"
---
# <a name="themeguard-function"></a><span data-ttu-id="ca192-103">THEMEGUARD Function</span><span class="sxs-lookup"><span data-stu-id="ca192-103">THEMEGUARD Function</span></span>

<span data-ttu-id="ca192-104">Schützt die Formatierungszellen eines Shapes, um sicherzustellen, dass Sie die entsprechenden Aspekte des aktuellen Designs verwenden.</span><span class="sxs-lookup"><span data-stu-id="ca192-104">Guards the formatting cells of a shape to ensure that they use appropriate aspects of the current theme.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="ca192-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca192-105">Syntax</span></span>

<span data-ttu-id="ca192-106">THEMEGUARD ()</span><span class="sxs-lookup"><span data-stu-id="ca192-106">THEMEGUARD()</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ca192-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ca192-107">Remarks</span></span>

<span data-ttu-id="ca192-108">Wenn Sie die THEMEGUARD-Funktion auf eine Zelle anwenden, wird die manuelle Formatierung nicht auf die gleiche Weise geschützt wie bei der Anwendung der GUARD-Funktion.</span><span class="sxs-lookup"><span data-stu-id="ca192-108">Applying the THEMEGUARD function to a cell does not guard against manual formatting in the same way that applying the GUARD function does.</span></span> <span data-ttu-id="ca192-109">Wenn Sie die Form auf der Benutzeroberfläche oder programmgesteuert mithilfe der Automatisierung formatieren, wird die THEMEGUARD-Formel außer Kraft gesetzt, es sei denn, Sie schließen die SETATREFEXPR-Funktion in die Formel ein, um den manuellen Formatierungswert zu speichern.</span><span class="sxs-lookup"><span data-stu-id="ca192-109">If you apply formatting to the shape in the user interface or programmatically, by means of Automation, the THEMEGUARD formula is overridden, unless you include the SETATREFEXPR function in the formula to store the manual formatting value.</span></span> 
  
## <a name="example"></a><span data-ttu-id="ca192-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ca192-110">Example</span></span>

```vb
Shape.FillForegnd = THEMEGUARD(THEME("AccentColor2")
```

<span data-ttu-id="ca192-111">Gibt an, dass das Shape die Farbe "Akzent 2" aus dem aktuellen Design anstelle der Füllfarbe des Hauptdesigns verwendet.</span><span class="sxs-lookup"><span data-stu-id="ca192-111">Specifies that the shape take the Accent 2 color from the current theme, rather than the main theme fill color.</span></span>
  

