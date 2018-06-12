---
title: Zelle "WalkPreference" (Abschnitt "Glue Info")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1115
localization_priority: Normal
ms.assetid: 08165195-7e4e-f3ab-fa76-fbcacb0a9c9c
description: Bestimmt, ob ein Endpunkt eines 1D-Shapes zu einem horizontalen oder vertikalen Verbindungspunkt auf dem Shape, mit dem er dynamisch verbunden ist, verschoben wird, wenn das Shape an eine mehrdeutige Position verschoben wird. Standardmäßig werden beide Endpunkte des 1D-Shapes zu horizontalen Verbindungspunkten verschoben.
ms.openlocfilehash: cd64a67de6ec914ad1bde86cdac829f6c12cebe4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798404"
---
# <a name="walkpreference-cell-glue-info-section"></a>WalkPreference Cell (Glue Info Section)

Bestimmt, ob ein Endpunkt eines 1D-Shapes zu einem horizontalen oder vertikalen Verbindungspunkt auf dem Shape, mit dem er dynamisch verbunden ist, verschoben wird, wenn das Shape an eine mehrdeutige Position verschoben wird. Standardmäßig werden beide Endpunkte des 1D-Shapes zu horizontalen Verbindungspunkten verschoben.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 1  <br/> | Der Anfangspunkt des 1D-Shapes wird zu einem vertikalen Verbindungspunkt verschoben, der Endpunkt hingegen zu einem horizontalen Verbindungspunkt (Verbindungen von oben zur Seite oder von unten zur Seite).  <br/> |**visWalkPrefBegNS** <br/> |
| 2  <br/> | Der Anfangspunkt des 1D-Shapes wird zu einem horizontalen Verbindungspunkt verschoben, der Endpunkt hingegen zu einem vertikalen Verbindungspunkt (Verbindungen von der Seite nach oben oder von der Seite nach unten).  <br/> |**visWalkPrefEndNS** <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Zelle hat keine Auswirkungen auf dynamische Verbinder. Das Verhalten eines dynamischen Verbinders wird von dessen Routingformat bestimmt. Das standardmäßige Routingformat für dynamische Verbinder auf einem Zeichenblatt finden Sie in der Zelle AnordnungFormat. Das Routingformat für einen spezifischen dynamischen Verbinder finden Sie hingegen in der Zelle ShapeAnordnungFormat.
  
Wenn Sie einen Verweis auf die Zelle WalkPreference nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | WalkPreference  <br/> |
   
Wenn Sie einen Verweis auf die Zelle WalkPreference aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowMisc** <br/> |
| Zellenindex:  <br/> |**visWalkPref** <br/> |
   

