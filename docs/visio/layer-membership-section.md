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
ms.openlocfilehash: e7e07ba14147abc8cdfd8b8544e4ee8f34b2be06
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432247"
---
# <a name="layer-membership-section"></a>Abschnitt "Layer Membership"

Enthält eine Zeile, in der alle Layer aufgeführt werden, denen das Shape zugewiesen ist.
  
## <a name="remarks"></a>Bemerkungen

Die Layerzuweisung wird als Index zu der Liste der Layer auf dem Zeichenblatt angezeigt. Der Layerindex entspricht der Reihenfolge der Layer im Dialogfeld **Layereigenschaften** (klicken Sie auf der Registerkarte **Start** in der Gruppe **Bearbeiten** auf **Layer**, und klicken Sie dann auf **Layereigenschaften**). Der erste Name in dem Dialogfeld ist Layer 0, der zweite ist Layer 1 und so weiter.
  
Wenn ein Shape mehreren Layern zugewiesen ist, werden die einzelnen Layerindizes in der Zelle Layer Membership durch ein Semikolon getrennt angezeigt.
  
Wenn Sie auf den Wert der Layer-Mitgliedschafts Zelle in einer Formel verweisen möchten, verwenden Sie den Namen **LayerMember**.
  

