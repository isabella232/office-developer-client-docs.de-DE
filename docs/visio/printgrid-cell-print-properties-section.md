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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433206"
---
# <a name="printgrid-cell-print-properties-section"></a>Zelle "PrintGrid" (Abschnitt "Print Properties")

Gibt an, ob beim Drucken einer Dokumentseite das Gitternetz gedruckt werden soll.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Beim Drucken der Seite wird das Gitternetz gedruckt.  <br/> |
|FALSE  <br/> |Das Gitternetz wird beim Drucken der Seite nicht gedruckt (Standard).  <br/> |
   
## <a name="remarks"></a>Hinweise

Dieser Wert entspricht der Einstellung für das Kontrollkästchen **Gitterlinien** auf der Registerkarte **Druckeinrichtung** im Dialogfeld **Seite einrichten** (klicken Sie auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**). Mit Ausnahme der Farbe (die Druckversion ist grau) ist das gedruckte Gitternetz identisch mit dem im Microsoft Visio-Zeichenfenster. 
  
Sie können für einzelne Seiten festlegen, ob das Gitternetz gedruckt werden soll. Die Rasterart kann auch seiteweise im Dialogfeld Linealraster definiert werden  (klicken Sie  auf der Registerkarte Ansicht auf den Pfeil anzeigen), wenn eine Seite aktiv ist. **&amp;** 
  
Um einen Verweis auf die Zelle PrintGrid anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |PrintGrid  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle PrintGrid nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPrintProperties** <br/> |
|Zellenindex:  <br/> |**visPrintPropertiesPrintGrid** <br/> |
   

