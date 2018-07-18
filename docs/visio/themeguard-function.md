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
# <a name="themeguard-function"></a>THEMEGUARD Function

Schützt die Formatierungen Zellen eines Shapes, um sicherzustellen, dass sie entsprechende Aspekte des aktuellen Designs verwenden.
  
## <a name="syntax"></a>Syntax

THEMEGUARD()
  
## <a name="remarks"></a>Bemerkungen

Anwenden der THEMEGUARD-Funktion auf eine Zelle ist nicht für die manuelle Formatierung auf die gleiche Weise, die die GUARD anwenden Funktion schützen. Wenn Sie die Formatierung auf die Form in der Benutzeroberfläche oder programmgesteuert mittels Automatisierung anwenden, wird die Formel THEMEGUARD überschrieben, sofern Sie nicht die SETATREFEXPR-Funktion in der Formel, um die manuelle Formatierung Wert zu speichern. 
  
## <a name="example"></a>Beispiel

```vb
Shape.FillForegnd = THEMEGUARD(THEME("AccentColor2")
```

Gibt an, dass das Shape die Farbe "Akzent 2" aus dem aktuellen Design anstelle der Füllfarbe des Hauptdesigns verwendet.
  

