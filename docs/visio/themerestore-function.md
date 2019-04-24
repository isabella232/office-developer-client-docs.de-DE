---
title: THEMERESTORE-Funktion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ca7e6621-f39b-64dd-3594-41d74da21a94
description: Speichert den lokalen Formatierungswert eines Shapes, wenn Sie ein Design anwenden, sodass Sie die lokale Formatierung wiederherstellen können, wenn der Benutzer das Design anschließend entfernt.
ms.openlocfilehash: 628e246f91172f136dd1a70807fca2abc1ff5bdd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332214"
---
# <a name="themerestore-function"></a>THEMERESTORE Function

Speichert den lokalen Formatierungswert eines Shapes, wenn Sie ein Design anwenden, sodass Sie die lokale Formatierung wiederherstellen können, wenn der Benutzer das Design anschließend entfernt.
  
## <a name="syntax"></a>Syntax

THEMERESTORE ()
  
## <a name="example"></a>Beispiel

```vb
Shape.FillForegnd = THEME("FillColor") + THEMERESTORE(RGB(255,102,0)
```

Wenn das aktuelle Design entfernt wird, stellt diese Funktion die lokale Füllfarbenformatierung wieder her, die zuvor auf ein Shape angewendet worden war.
  

