---
title: Zelle "DynamicsOff" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251641
localization_priority: Normal
ms.assetid: 055764aa-9681-ffb0-83ce-fdd612fe37af
description: Legt fest, ob platzierbare Shapes verschoben und ob Verbinder um andere Shapes und Verbinder auf dem Zeichenblatt herum umgeleitet werden können.
ms.openlocfilehash: d1075ab1b0512d5db1c7b7a5f2895305318dae7d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437476"
---
# <a name="dynamicsoff-cell-page-layout-section"></a>Zelle "DynamicsOff" (Abschnitt "Page Layout")

Legt fest, ob platzierbare Shapes verschoben und ob Verbinder um andere Shapes und Verbinder auf dem Zeichenblatt herum umgeleitet werden können.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Dynamik deaktivieren.  <br/> |
| FALSE  <br/> | Dynamik aktivieren.  <br/> |
   
## <a name="remarks"></a>Hinweise

Sie können die Dynamik deaktivieren, um die Leistung Ihrer Lösung zu steigern. Wenn Ihre Lösung beispielsweise Shape-Platzierungen in eine Zeichnung einfügt, Sie aber nicht möchten, dass die Anwendung Verbinder umleitet und Shapes neu platziert, sobald Sie ein Shape hinzufügen, können Sie die Dynamik deaktivieren. Aktivieren Sie die Dynamik wieder, nachdem Ihre Lösung die Shapes hinzugefügt hat.
  
Um einen Verweis auf die DynamicsOff-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | DynamicsOff  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die DynamicsOff-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
| Zellenindex:  <br/> |**visPLODynamicsOff** <br/> |
   

