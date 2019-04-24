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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315719"
---
# <a name="dynamicsoff-cell-page-layout-section"></a>Zelle "DynamicsOff" (Abschnitt "Page Layout")

Legt fest, ob platzierbare Shapes verschoben und ob Verbinder um andere Shapes und Verbinder auf dem Zeichenblatt herum umgeleitet werden können.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Dynamik deaktivieren.  <br/> |
| FALSE  <br/> | Dynamik aktivieren.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können die Dynamik deaktivieren, um die Leistung Ihrer Lösung zu steigern. Wenn Ihre Lösung beispielsweise Shape-Platzierungen in eine Zeichnung einfügt, Sie aber nicht möchten, dass die Anwendung Verbinder umleitet und Shapes neu platziert, sobald Sie ein Shape hinzufügen, können Sie die Dynamik deaktivieren. Aktivieren Sie die Dynamik wieder, nachdem Ihre Lösung die Shapes hinzugefügt hat.
  
Wenn Sie einen Verweis auf die Zelle Zelle DynamicsOff aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Zelle DynamicsOff  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle DynamicsOff aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
| Zellenindex:  <br/> |**visPLODynamicsOff** <br/> |
   

