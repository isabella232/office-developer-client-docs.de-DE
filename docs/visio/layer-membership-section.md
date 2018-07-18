---
title: Abschnitt "Layer Membership"
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm2080
localization_priority: Normal
ms.assetid: 7fb1d8a1-8892-f489-2f58-0008b5b750f5
description: Enthält eine Zeile, in der alle Layer aufgeführt werden, denen das Shape zugewiesen ist.
ms.openlocfilehash: 5f522e31916ad276e15ac23e5149407dd67eb9cf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797305"
---
# <a name="layer-membership-section"></a>Layer Membership Section

Enthält eine Zeile, in der alle Layer aufgeführt werden, denen das Shape zugewiesen ist.
  
## <a name="remarks"></a>Bemerkungen

Die Layerzuweisung wird als Index zu der Liste der Layer auf dem Zeichenblatt angezeigt. Der Layerindex entspricht der Reihenfolge der Layer im Dialogfeld **Layereigenschaften** (klicken Sie auf der Registerkarte **Start** in der Gruppe **Bearbeiten** auf **Layer**, und klicken Sie dann auf **Layereigenschaften**). Der erste Name in dem Dialogfeld ist Layer 0, der zweite ist Layer 1 und so weiter.
  
Wenn ein Shape mehreren Layern zugewiesen ist, werden die einzelnen Layerindizes in der Zelle Layer Membership durch ein Semikolon getrennt angezeigt.
  
Wenn Sie auf den Wert der Zelle Layer Membership in einer Formel verweisen möchten, verwenden Sie den Namen **LayerMember**.
  

