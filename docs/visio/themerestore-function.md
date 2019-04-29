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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404288"
---
# <a name="themerestore-function"></a><span data-ttu-id="f2ebc-103">THEMERESTORE Function</span><span class="sxs-lookup"><span data-stu-id="f2ebc-103">THEMERESTORE Function</span></span>

<span data-ttu-id="f2ebc-104">Speichert den lokalen Formatierungswert eines Shapes, wenn Sie ein Design anwenden, sodass Sie die lokale Formatierung wiederherstellen können, wenn der Benutzer das Design anschließend entfernt.</span><span class="sxs-lookup"><span data-stu-id="f2ebc-104">Stores the local formatting value of a shape when you apply a theme so that you can restore the local formatting if the user subsequently removes the theme.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="f2ebc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2ebc-105">Syntax</span></span>

<span data-ttu-id="f2ebc-106">THEMERESTORE ()</span><span class="sxs-lookup"><span data-stu-id="f2ebc-106">THEMERESTORE()</span></span>
  
## <a name="example"></a><span data-ttu-id="f2ebc-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f2ebc-107">Example</span></span>

```vb
Shape.FillForegnd = THEME("FillColor") + THEMERESTORE(RGB(255,102,0)
```

<span data-ttu-id="f2ebc-108">Wenn das aktuelle Design entfernt wird, stellt diese Funktion die lokale Füllfarbenformatierung wieder her, die zuvor auf ein Shape angewendet worden war.</span><span class="sxs-lookup"><span data-stu-id="f2ebc-108">Restores local fill color formatting previously applied to a shape when the current theme is removed.</span></span>
  

