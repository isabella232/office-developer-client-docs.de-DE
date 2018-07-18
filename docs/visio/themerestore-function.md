---
title: THEMERESTORE-Funktion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ca7e6621-f39b-64dd-3594-41d74da21a94
description: Speichert den Wert der lokalen Formatierungen eines Shapes anwenden eines Designs, damit Sie die lokale Formatierung wiederherstellen können, wenn der Benutzer anschließend das Design entfernt.
ms.openlocfilehash: f22f603cad1d310adc59d19e9b3e3882bd797fce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798278"
---
# <a name="themerestore-function"></a>THEMERESTORE Function

Speichert den Wert der lokalen Formatierungen eines Shapes anwenden eines Designs, damit Sie die lokale Formatierung wiederherstellen können, wenn der Benutzer anschließend das Design entfernt.
  
## <a name="syntax"></a>Syntax

THEMERESTORE()
  
## <a name="example"></a>Beispiel

```vb
Shape.FillForegnd = THEME("FillColor") + THEMERESTORE(RGB(255,102,0)
```

Wenn das aktuelle Design entfernt wird, stellt diese Funktion die lokale Füllfarbenformatierung wieder her, die zuvor auf ein Shape angewendet worden war.
  

