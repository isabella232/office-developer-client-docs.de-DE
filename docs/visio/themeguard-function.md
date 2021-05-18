---
title: THEMEGUARD-Funktion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a556eadc-9ee6-7a29-ca05-6250b612790c
description: Wacht die Formatierungszellen eines Shapes, um sicherzustellen, dass sie geeignete Aspekte des aktuellen Designs verwenden.
ms.openlocfilehash: c20d43f9d03296a3c529a6c8f59cf27489dcdc51
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404946"
---
# <a name="themeguard-function"></a>THEMEGUARD Function

Wacht die Formatierungszellen eines Shapes, um sicherzustellen, dass sie geeignete Aspekte des aktuellen Designs verwenden.
  
## <a name="syntax"></a>Syntax

THEMEGUARD()
  
## <a name="remarks"></a>Hinweise

Das Anwenden der THEMEGUARD-Funktion auf eine Zelle wehrt sich nicht auf die gleiche Weise vor manueller Formatierung wie die Anwendung der GUARD-Funktion. Wenn Sie die Formatierung auf das Shape auf der Benutzeroberfläche oder programmgesteuert über Automatisierung anwenden, wird die THEMEGUARD-Formel außer Kraft gesetzt, es sei denn, Sie fügen die SETATREFEXPR-Funktion in die Formel ein, um den manuellen Formatierungswert zu speichern. 
  
## <a name="example"></a>Beispiel

```vb
Shape.FillForegnd = THEMEGUARD(THEME("AccentColor2")
```

Gibt an, dass das Shape die Farbe "Akzent 2" aus dem aktuellen Design anstelle der Füllfarbe des Hauptdesigns verwendet.
  

