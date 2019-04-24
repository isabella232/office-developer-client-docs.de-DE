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
# <a name="themerestore-function"></a><span data-ttu-id="e90c2-103">THEMERESTORE Function</span><span class="sxs-lookup"><span data-stu-id="e90c2-103">THEMERESTORE Function</span></span>

<span data-ttu-id="e90c2-104">Speichert den lokalen Formatierungswert eines Shapes, wenn Sie ein Design anwenden, sodass Sie die lokale Formatierung wiederherstellen können, wenn der Benutzer das Design anschließend entfernt.</span><span class="sxs-lookup"><span data-stu-id="e90c2-104">Stores the local formatting value of a shape when you apply a theme so that you can restore the local formatting if the user subsequently removes the theme.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e90c2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e90c2-105">Syntax</span></span>

<span data-ttu-id="e90c2-106">THEMERESTORE ()</span><span class="sxs-lookup"><span data-stu-id="e90c2-106">THEMERESTORE()</span></span>
  
## <a name="example"></a><span data-ttu-id="e90c2-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e90c2-107">Example</span></span>

```vb
Shape.FillForegnd = THEME("FillColor") + THEMERESTORE(RGB(255,102,0)
```

<span data-ttu-id="e90c2-108">Wenn das aktuelle Design entfernt wird, stellt diese Funktion die lokale Füllfarbenformatierung wieder her, die zuvor auf ein Shape angewendet worden war.</span><span class="sxs-lookup"><span data-stu-id="e90c2-108">Restores local fill color formatting previously applied to a shape when the current theme is removed.</span></span>
  

