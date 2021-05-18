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
ms.openlocfilehash: 05f7ded3f7336dc2f8598e8d1e9edc501b511546
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408607"
---
# <a name="walkpreference-cell-glue-info-section"></a>Zelle "WalkPreference" (Abschnitt "Glue Info")

Bestimmt, ob ein Endpunkt eines 1D-Shapes zu einem horizontalen oder vertikalen Verbindungspunkt auf dem Shape, mit dem er dynamisch verbunden ist, verschoben wird, wenn das Shape an eine mehrdeutige Position verschoben wird. Standardmäßig werden beide Endpunkte des 1D-Shapes zu horizontalen Verbindungspunkten verschoben.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 1  <br/> | Der Anfangspunkt des 1D-Shapes wird zu einem vertikalen Verbindungspunkt verschoben, der Endpunkt hingegen zu einem horizontalen Verbindungspunkt (Verbindungen von oben zur Seite oder von unten zur Seite).  <br/> |**visWalkPrefBegNS** <br/> |
| 2  <br/> | Der Anfangspunkt des 1D-Shapes wird zu einem horizontalen Verbindungspunkt verschoben, der Endpunkt hingegen zu einem vertikalen Verbindungspunkt (Verbindungen von der Seite nach oben oder von der Seite nach unten).  <br/> |**visWalkPrefEndNS** <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Zelle hat keine Auswirkungen auf dynamische Verbinder. Das Verhalten eines dynamischen Verbinders wird von dessen Routingformat bestimmt. Das standardmäßige Routingformat für dynamische Verbinder auf einem Zeichenblatt finden Sie in der Zelle AnordnungFormat. Das Routingformat für einen spezifischen dynamischen Verbinder finden Sie hingegen in der Zelle ShapeAnordnungFormat.
  
Um einen Verweis auf die WalkPreference-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | WalkPreference  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die WalkPreference-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowMisc** <br/> |
| Zellenindex:  <br/> |**visWalkPref** <br/> |
   

