---
title: Zelle "PaperKind" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60067
localization_priority: Normal
ms.assetid: b2c9616f-a144-eb99-54b6-b53745c7b4d6
description: Gibt den Papiertyp für den Druck der Seite an.
ms.openlocfilehash: 03659553ab32afd20d1a5a40b85a8bbf107dbb08
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797597"
---
# <a name="paperkind-cell-print-properties-section"></a>Zelle "PaperKind" (Abschnitt "Print Properties")

Gibt den Papiertyp für den Druck der Seite an.
  
## <a name="remarks"></a>Bemerkungen

Diese Einstellung entspricht der Einstellung **Papiergröße** im Dialogfeld **Drucker einrichten** (klicken Sie auf der Registerkarte **Entwurf** , klicken Sie auf den Pfeil neben **Seite einrichten** , und klicken Sie dann auf der Registerkarte **Druckeinrichtung** auf die Schaltfläche " **Setup** "). 
  
Die numerischen Werte in dieser Zelle auf Konstanten (mit dem Präfix DMPAPER) in der Microsoft Windows-Datei wingdi.h für die Papierauswahl definiert sind. 
  
Wenn Sie einen Verweis auf die Zelle PaperKind nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |PaperKind  <br/> |
   
Wenn Sie einen Verweis auf die Zelle PaperKind aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPrintProperties** <br/> |
|Zellenindex:  <br/> |**visPrintPropertiesPaperKind** <br/> |
   

