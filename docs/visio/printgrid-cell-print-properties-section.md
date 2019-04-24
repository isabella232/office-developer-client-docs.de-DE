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
ms.openlocfilehash: 9b98999cd02fa6a47ec8564bbd7337ecf8637306
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315190"
---
# <a name="printgrid-cell-print-properties-section"></a>Zelle "PrintGrid" (Abschnitt "Print Properties")

Gibt an, ob beim Drucken einer Dokumentseite das Gitternetz gedruckt werden soll.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Beim Drucken der Seite wird das Gitternetz gedruckt.  <br/> |
|FALSE  <br/> |Das Gitternetz wird beim Drucken der Seite nicht gedruckt (Standard).  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Dieser Wert entspricht der Einstellung für das Kontrollkästchen **Gitterlinien** auf der Registerkarte **Druckeinrichtung** im Dialogfeld **Seite einrichten** (klicken Sie auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**). Mit Ausnahme der Farbe (die Druckversion ist grau) ist das gedruckte Gitternetz identisch mit dem im Microsoft Visio-Zeichenfenster. 
  
Sie können für einzelne Seiten festlegen, ob das Gitternetz gedruckt werden soll. Die Art des Rasters kann auch auf Seitenbasis im Dialogfeld **** ** &amp; Lineal-Raster** definiert werden (Klicken Sie auf der Registerkarte **Ansicht** auf den Pfeil nach unten), wenn eine Seite aktiv ist. 
  
Wenn Sie einen Verweis auf die Zelle PrintGrid aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |PrintGrid  <br/> |
   
Wenn Sie einen Verweis auf die Zelle PrintGrid aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPrintProperties** <br/> |
|Zellenindex:  <br/> |**visPrintPropertiesPrintGrid** <br/> |
   

