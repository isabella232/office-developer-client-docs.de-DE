---
title: Zelle "DrawingSizeType" (Abschnitt "Zeichenblatteigenschaften")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm275
localization_priority: Normal
ms.assetid: 7fe270e8-0dff-bf1f-dfc0-c0608af79f59
description: Legt die Zeichnungsgröße fest.
ms.openlocfilehash: 33c85b6c2f0587654038eaec1a9490ca8bd8301b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425449"
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
|5   <br/> |Metrisch (ISO)  <br/> |**visDSMetric** <br/> |
|6   <br/> |ANSI-Konstruktion  <br/> |**visDSEngr** <br/> |
|7   <br/> |ANSI-Architektur  <br/> |**visDSArch** <br/> |
   
## <a name="remarks"></a>Hinweise

Verwenden Sie das Dialogfeld **Seite einrichten**, um die Zeichnungsgröße festzulegen (klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**), oder passen Sie die Größe der Seite manuell mit der Maus an. 
  
Um einen Verweis auf die Zelle DrawingSizeType anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |DrawingSizeType  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die DrawingSizeType-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPage** <br/> |
|Zellenindex:  <br/> |**visPageDrawSizeType** <br/> |
   

