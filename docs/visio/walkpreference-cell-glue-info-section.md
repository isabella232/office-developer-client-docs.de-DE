---
title: Zelle "WalkPreference" (Abschnitt "Glue Info")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1115
ms.localizationpriority: medium
ms.assetid: 08165195-7e4e-f3ab-fa76-fbcacb0a9c9c
description: Bestimmt, ob ein Endpunkt eines 1D-Shapes zu einem horizontalen oder vertikalen Verbindungspunkt auf dem Shape, mit dem er dynamisch verbunden ist, verschoben wird, wenn das Shape an eine mehrdeutige Position verschoben wird. Standardmäßig werden beide Endpunkte des 1D-Shapes zu horizontalen Verbindungspunkten verschoben.
ms.openlocfilehash: bd3b582ca00c8c4f9ef9018f219b0fdd9dafe07d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627114"
---
# <a name="walkpreference-cell-glue-info-section"></a>Zelle "WalkPreference" (Abschnitt "Glue Info")

Bestimmt, ob ein Endpunkt eines 1D-Shapes zu einem horizontalen oder vertikalen Verbindungspunkt auf dem Shape, mit dem er dynamisch verbunden ist, verschoben wird, wenn das Shape an eine mehrdeutige Position verschoben wird. Standardmäßig werden beide Endpunkte des 1D-Shapes zu horizontalen Verbindungspunkten verschoben.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 1  <br/> | Der Anfangspunkt des 1D-Shapes wird zu einem vertikalen Verbindungspunkt verschoben, der Endpunkt hingegen zu einem horizontalen Verbindungspunkt (Verbindungen von oben zur Seite oder von unten zur Seite).  <br/> |**visOirPrefBegNS** <br/> |
| 2  <br/> | Der Anfangspunkt des 1D-Shapes wird zu einem horizontalen Verbindungspunkt verschoben, der Endpunkt hingegen zu einem vertikalen Verbindungspunkt (Verbindungen von der Seite nach oben oder von der Seite nach unten).  <br/> |**visOirPrefEndNS** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Zelle hat keine Auswirkungen auf dynamische Verbinder. Das Verhalten eines dynamischen Verbinders wird von dessen Routingformat bestimmt. Das standardmäßige Routingformat für dynamische Verbinder auf einem Zeichenblatt finden Sie in der Zelle AnordnungFormat. Das Routingformat für einen spezifischen dynamischen Verbinder finden Sie hingegen in der Zelle ShapeAnordnungFormat.
  
Um einen Verweis auf die Zelle "WalkPreference" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | WalkPreference  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle WalkPreference anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowMisc** <br/> |
| Zellenindex:  <br/> |**visOirPref** <br/> |
   

