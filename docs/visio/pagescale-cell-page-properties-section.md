---
title: Zelle "PageScale" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm775
ms.localizationpriority: medium
ms.assetid: e1da84b3-fd15-12b9-9342-0412e818b3b9
description: Bestimmt den Wert der Seiteneinheit im aktuellen Zeichnungsmaßstab. Der Zeichnungsmaßstab für die Seite ist das Verhältnis der in der Zelle PageScale angezeigten Seiteneinheit zur in der Zelle DrawingScale angezeigten Zeichnungseinheit.
ms.openlocfilehash: 32d596b7b7e2b7e9810f0bc168072eefa534b045
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554222"
---
# <a name="pagescale-cell-page-properties-section"></a>Zelle "PageScale" (Abschnitt "Page Properties")

Bestimmt den Wert der Seiteneinheit im aktuellen Zeichnungsmaßstab. Der Zeichnungsmaßstab für die Seite ist das Verhältnis der in der Zelle PageScale angezeigten Seiteneinheit zur in der Zelle DrawingScale angezeigten Zeichnungseinheit.
  
## <a name="remarks"></a>HinwBemerkungeneise

Sie können auch den Wert der Zelle PageScale auf der Registerkarte Zeichnungsmaßstab im Dialogfeld Seite **einrichten** festlegen (klicken Sie auf der Registerkarte Entwurf auf den Pfeil neben dem Pfeil neben  Seite **einrichten).**  Der Wert der Zelle ist die erste der beiden Zahlen im **vordefinierten Skalierungsfeld** oder **benutzerdefinierten Skalierungsfeld,** abhängig von der unter Zeichnungsmaßstab ausgewählten Einstellung für den Zeichnungsmaßstab.  Wenn Sie beispielsweise einen Architekturmaßstab für ihre Zeichnung auswählen, ist der Zeichnungsmaßstab für das Zeichenblatt 3/32" = 1'0". Der Wert in der Zelle "PageScale" ist 0,0938 Zoll. (oder 3/32") und der Wert in der Zelle DrawingScale ist 1 Fuß.
  
Um einen Verweis auf die Zelle "PageScale" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |PageScale  <br/> |
   
Um einen Verweis auf die Zelle "PageScale" anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPage** <br/> |
|Zellenindex:  <br/> |**visPageScale** <br/> |
   

