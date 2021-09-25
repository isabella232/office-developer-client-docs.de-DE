---
title: Zelle "DrawingSizeType" (Abschnitt "Zeichenblatteigenschaften")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm275
ms.localizationpriority: medium
ms.assetid: 7fe270e8-0dff-bf1f-dfc0-c0608af79f59
description: Legt die Zeichnungsgröße fest.
ms.openlocfilehash: eab36fc223c21cc8b943cabb5005649f4b090f05
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570736"
---
# <a name="drawingsizetype-cell-page-properties-section"></a>Zelle "DrawingSizeType" (Abschnitt "Zeichenblatteigenschaften")

Legt die Zeichnungsgröße fest.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Druckereinstellungen übernehmen  <br/> |**visPrintSetup** <br/> |
|1  <br/> |Blatt an Zeichnungsgröße anpassen  <br/> |**visTight** <br/> |
|2  <br/> |Standard  <br/> |**visStandard** <br/> |
|3  <br/> |Benutzerdefiniert  <br/> |**visCustom** <br/> |
|4   <br/> |Benutzerdefinierte Skalierung  <br/> |**visLogical** <br/> |
|5  <br/> |Metrisch (ISO)  <br/> |**visDSMetric** <br/> |
|6   <br/> |ANSI-Konstruktion  <br/> |**visDSEngr** <br/> |
|7   <br/> |ANSI-Architektur  <br/> |**visDSArch** <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie das Dialogfeld **Seite einrichten**, um die Zeichnungsgröße festzulegen (klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**), oder passen Sie die Größe der Seite manuell mit der Maus an. 
  
Verwenden Sie Folgendes, um einen Verweis auf die Zelle DrawingSizeType anhand des Namens einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |DrawingSizeType  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle DrawingSizeType anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPage** <br/> |
|Zellenindex:  <br/> |**visPageDrawSizeType** <br/> |
   

