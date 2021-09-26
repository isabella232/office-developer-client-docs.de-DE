---
title: THEMEGUARD-Funktion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: a556eadc-9ee6-7a29-ca05-6250b612790c
description: Schützt die Formatierungszellen eines Shapes, um sicherzustellen, dass sie die entsprechenden Aspekte des aktuellen Designs verwenden.
ms.openlocfilehash: e29fdd9c148940e047a7f97a8e6d5b72d685f7cb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603347"
---
# <a name="themeguard-function"></a>THEMEGUARD Function

Schützt die Formatierungszellen eines Shapes, um sicherzustellen, dass sie die entsprechenden Aspekte des aktuellen Designs verwenden.
  
## <a name="syntax"></a>Syntax

THEMEGUARD()
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Anwenden der THEMEGUARD-Funktion auf eine Zelle schützt nicht auf die gleiche Weise vor manueller Formatierung wie das Anwenden der GUARD-Funktion. Wenn Sie die Formatierung auf das Shape auf der Benutzeroberfläche oder programmgesteuert mithilfe der Automatisierung anwenden, wird die THEMEGUARD-Formel außer Kraft gesetzt, es sei denn, Sie fügen die SETATREFEXPR-Funktion in die Formel ein, um den manuellen Formatierungswert zu speichern. 
  
## <a name="example"></a>Beispiel

```vb
Shape.FillForegnd = THEMEGUARD(THEME("AccentColor2")
```

Gibt an, dass das Shape die Farbe "Akzent 2" aus dem aktuellen Design anstelle der Füllfarbe des Hauptdesigns verwendet.
  

