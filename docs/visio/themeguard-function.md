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
# <a name="themeguard-function"></a>THEMEGUARD Function

Schützt die Formatierungszellen eines Shapes, um sicherzustellen, dass Sie die entsprechenden Aspekte des aktuellen Designs verwenden.
  
## <a name="syntax"></a>Syntax

THEMEGUARD ()
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie die THEMEGUARD-Funktion auf eine Zelle anwenden, wird die manuelle Formatierung nicht auf die gleiche Weise geschützt wie bei der Anwendung der GUARD-Funktion. Wenn Sie die Form auf der Benutzeroberfläche oder programmgesteuert mithilfe der Automatisierung formatieren, wird die THEMEGUARD-Formel außer Kraft gesetzt, es sei denn, Sie schließen die SETATREFEXPR-Funktion in die Formel ein, um den manuellen Formatierungswert zu speichern. 
  
## <a name="example"></a>Beispiel

```vb
Shape.FillForegnd = THEMEGUARD(THEME("AccentColor2")
```

Gibt an, dass das Shape die Farbe "Akzent 2" aus dem aktuellen Design anstelle der Füllfarbe des Hauptdesigns verwendet.
  

