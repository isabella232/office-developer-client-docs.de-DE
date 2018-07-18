---
title: Zelle "PrintGrid" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033794
localization_priority: Normal
ms.assetid: 0504ff7f-2274-7ae3-1f4b-a3d890dbd79a
description: Gibt an, ob beim Drucken einer Dokumentseite das Gitternetz gedruckt werden soll.
ms.openlocfilehash: 76e5b5b4e82c39cbbffbecc710f05a77dbaa6332
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797748"
---
# <a name="printgrid-cell-print-properties-section"></a>PrintGrid Cell (Print Properties Section)

Gibt an, ob beim Drucken einer Dokumentseite das Gitternetz gedruckt werden soll.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|WAHR  <br/> |Beim Drucken der Seite wird das Gitternetz gedruckt.  <br/> |
|FALSCH  <br/> |Das Gitternetz wird beim Drucken der Seite nicht gedruckt (Standard).  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Dieser Wert entspricht der Einstellung für das Kontrollkästchen **Gitterlinien** auf der Registerkarte **Druckeinrichtung** im Dialogfeld **Seite einrichten** (klicken Sie auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**). Mit Ausnahme der Farbe (die Druckversion ist grau) ist das gedruckte Gitternetz identisch mit dem im Microsoft Visio-Zeichenfenster. 
  
Sie können auswählen, ob das Gitternetz auf Basis von Seite gedruckt. Das Format des Rasters kann auch definiert werden, auf Basis von Seite in der **Lineal &amp; Raster** im Dialogfeld (klicken Sie auf der Registerkarte **Ansicht** auf den Pfeil neben **Anzeigen** ) Wenn die Seite aktiv ist. 
  
Wenn Sie einen Verweis auf die Zelle PrintGrid aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |PrintGrid  <br/> |
   
Wenn Sie einen Verweis auf die Zelle PrintGrid aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPrintProperties** <br/> |
|Zellenindex:  <br/> |**visPrintPropertiesPrintGrid** <br/> |
   

