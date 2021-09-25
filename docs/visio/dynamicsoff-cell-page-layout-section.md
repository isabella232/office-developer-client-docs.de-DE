---
title: Zelle "DynamicsOff" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251641
ms.localizationpriority: medium
ms.assetid: 055764aa-9681-ffb0-83ce-fdd612fe37af
description: Legt fest, ob platzierbare Shapes verschoben und ob Verbinder um andere Shapes und Verbinder auf dem Zeichenblatt herum umgeleitet werden können.
ms.openlocfilehash: 8579e350379df5798c29ac12436ff6d4edcb1926
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590240"
---
# <a name="dynamicsoff-cell-page-layout-section"></a>Zelle "DynamicsOff" (Abschnitt "Page Layout")

Legt fest, ob platzierbare Shapes verschoben und ob Verbinder um andere Shapes und Verbinder auf dem Zeichenblatt herum umgeleitet werden können.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Dynamik deaktivieren.  <br/> |
| FALSE  <br/> | Dynamik aktivieren.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Sie können die Dynamik deaktivieren, um die Leistung Ihrer Lösung zu steigern. Wenn Ihre Lösung beispielsweise Shape-Platzierungen in eine Zeichnung einfügt, Sie aber nicht möchten, dass die Anwendung Verbinder umleitet und Shapes neu platziert, sobald Sie ein Shape hinzufügen, können Sie die Dynamik deaktivieren. Aktivieren Sie die Dynamik wieder, nachdem Ihre Lösung die Shapes hinzugefügt hat.
  
Verwenden Sie Folgendes, um einen Verweis auf die Zelle "DynamicsOff" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | DynamicsOff  <br/> |
   
Um einen Verweis auf die Zelle DynamicsOff anhand des Indexes aus einem Programm abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
| Zellenindex:  <br/> |**visPLODynamicsOff** <br/> |
   

