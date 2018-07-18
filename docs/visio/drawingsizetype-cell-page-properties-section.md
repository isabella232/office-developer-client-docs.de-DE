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
ms.openlocfilehash: a87f37ac79d00aeb064072389db432421b33d2d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796896"
---
# <a name="drawingsizetype-cell-page-properties-section"></a>DrawingSizeType Cell (Page Properties Section)

Legt die Zeichnungsgröße fest.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Druckereinstellungen übernehmen  <br/> |**visPrintSetup** <br/> |
|1  <br/> |Blatt an Zeichnungsgröße anpassen  <br/> |**visTight** <br/> |
|2  <br/> |Standard  <br/> |**visStandard** <br/> |
|3  <br/> |Benutzerdefiniert  <br/> |**visCustom** <br/> |
|4  <br/> |Benutzerdefinierte Skalierung  <br/> |**visLogical** <br/> |
|5  <br/> |Metrisch (ISO)  <br/> |**visDSMetric** <br/> |
|6  <br/> |ANSI-Konstruktion  <br/> |**visDSEngr** <br/> |
|7  <br/> |ANSI-Architektur  <br/> |**visDSArch** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Verwenden Sie das Dialogfeld **Seite einrichten**, um die Zeichnungsgröße festzulegen (klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**), oder passen Sie die Größe der Seite manuell mit der Maus an. 
  
Wenn Sie eine Referenz auf die Zelle DrawingSizeType nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |DrawingSizeType  <br/> |
   
Wenn Sie eine Referenz auf die Zelle DrawingSizeType aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPage** <br/> |
|Zellenindex:  <br/> |**visPageDrawSizeType** <br/> |
   

