---
title: Zelle "PrintGrid" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033794
ms.localizationpriority: medium
ms.assetid: 0504ff7f-2274-7ae3-1f4b-a3d890dbd79a
description: Gibt an, ob beim Drucken einer Dokumentseite das Gitternetz gedruckt werden soll.
ms.openlocfilehash: e290e28920f3ece4f9493b52b223e85dc3888949
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559759"
---
# <a name="printgrid-cell-print-properties-section"></a>Zelle "PrintGrid" (Abschnitt "Print Properties")

Gibt an, ob beim Drucken einer Dokumentseite das Gitternetz gedruckt werden soll.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Beim Drucken der Seite wird das Gitternetz gedruckt.  <br/> |
|FALSE  <br/> |Das Gitternetz wird beim Drucken der Seite nicht gedruckt (Standard).  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Dieser Wert entspricht der Einstellung für das Kontrollkästchen **Gitterlinien** auf der Registerkarte **Druckeinrichtung** im Dialogfeld **Seite einrichten** (klicken Sie auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**). Mit Ausnahme der Farbe (die Druckversion ist grau) ist das gedruckte Gitternetz identisch mit dem im Microsoft Visio-Zeichenfenster. 
  
Sie können für einzelne Seiten festlegen, ob das Gitternetz gedruckt werden soll. Das Rasterformat kann auch seitenweise im Dialogfeld **&amp; Linealraster** definiert werden (klicken Sie auf **der** Registerkarte Ansicht auf den Pfeil **anzeigen),** wenn eine Seite aktiv ist. 
  
Um einen Verweis auf die Zelle "PrintGrid" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |PrintGrid  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle PrintGrid anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPrintProperties** <br/> |
|Zellenindex:  <br/> |**visPrintPropertiesPrintGrid** <br/> |
   

