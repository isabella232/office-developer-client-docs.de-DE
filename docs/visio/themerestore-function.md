---
title: THEMERESTORE-Funktion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: ca7e6621-f39b-64dd-3594-41d74da21a94
description: Speichert den lokalen Formatierungswert eines Shapes, wenn Sie ein Design anwenden, sodass Sie die lokale Formatierung wiederherstellen können, wenn der Benutzer das Design anschließend entfernt.
ms.openlocfilehash: 708dcf51a7a01c0f58dab435dd710208b5cb2ff1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597856"
---
# <a name="themerestore-function"></a>THEMERESTORE Function

Speichert den lokalen Formatierungswert eines Shapes, wenn Sie ein Design anwenden, sodass Sie die lokale Formatierung wiederherstellen können, wenn der Benutzer das Design anschließend entfernt.
  
## <a name="syntax"></a>Syntax

THEMERESTORE()
  
## <a name="example"></a>Beispiel

```vb
Shape.FillForegnd = THEME("FillColor") + THEMERESTORE(RGB(255,102,0)
```

Wenn das aktuelle Design entfernt wird, stellt diese Funktion die lokale Füllfarbenformatierung wieder her, die zuvor auf ein Shape angewendet worden war.
  

