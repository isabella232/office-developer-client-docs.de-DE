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
# <a name="themerestore-function"></a><span data-ttu-id="b037c-103">THEMERESTORE-Funktion</span><span class="sxs-lookup"><span data-stu-id="b037c-103">THEMERESTORE Function</span></span>

<span data-ttu-id="b037c-104">Speichert den Wert der lokalen Formatierungen eines Shapes anwenden eines Designs, damit Sie die lokale Formatierung wiederherstellen können, wenn der Benutzer anschließend das Design entfernt.</span><span class="sxs-lookup"><span data-stu-id="b037c-104">Stores the local formatting value of a shape when you apply a theme so that you can restore the local formatting if the user subsequently removes the theme.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="b037c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b037c-105">Syntax</span></span>

<span data-ttu-id="b037c-106">THEMERESTORE()</span><span class="sxs-lookup"><span data-stu-id="b037c-106">THEMERESTORE()</span></span>
  
## <a name="example"></a><span data-ttu-id="b037c-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b037c-107">Example</span></span>

```vb
Shape.FillForegnd = THEME("FillColor") + THEMERESTORE(RGB(255,102,0)
```

<span data-ttu-id="b037c-108">Wenn das aktuelle Design entfernt wird, stellt diese Funktion die lokale Füllfarbenformatierung wieder her, die zuvor auf ein Shape angewendet worden war.</span><span class="sxs-lookup"><span data-stu-id="b037c-108">Restores local fill color formatting previously applied to a shape when the current theme is removed.</span></span>
  

