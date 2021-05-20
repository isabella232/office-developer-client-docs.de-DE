---
title: Zelle "ComplexScriptSize" (Abschnitt "Character")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033768
localization_priority: Normal
ms.assetid: f58687d7-2ba4-ff77-0bcc-3106867d89de
description: Der Schriftgrad zum Formatieren von Text mit komplexen Schriftzeichen.
ms.openlocfilehash: 38b01c4a0142c7eca2923ee9b13963eaa1a62830
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428438"
---
# <a name="complexscriptsize-cell-character-section"></a>Zelle "ComplexScriptSize" (Abschnitt "Character")

Der Schriftgrad zum Formatieren von Text mit komplexen Schriftzeichen. 
  
## <a name="remarks"></a>Hinweise

Komplexe Schriftgrößen für Skripts werden auf der Registerkarte **Schriftart** im  Dialogfeld **Text** aufgeführt (klicken Sie auf der Registerkarte **Start** auf den Pfeil in der Gruppe Schriftart). Diese Liste wird nur angezeigt, wenn Sie eine Sprache mit  asiatischen oder komplexen Skriptzeichen im Dialogfeld Spracheinstellungen Microsoft Office hinzugefügt haben. (Klicken **Sie auf Start,** **klicken** Sie auf Alle Programme, **Microsoft Office**, klicken Sie **Microsoft Office Tools,** und klicken Sie **dann auf Microsoft Office Spracheinstellungen**.
  
Sie können diesen Wert als explizite Größe in Punkt oder als Prozentsatz angeben. Wenn Sie einen Prozentsatz angeben, basiert der Wert auf dem Wert in der Zelle Größe. Der Standardwert von 0 (Null) bedeutet 100 %. 
  
Verwenden Sie zum Erhalten eines Verweises auf die Zelle ComplexScriptSize anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Char.ComplexScriptSize[ *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die ComplexScriptSize-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionCharacter** <br/> |
|Zeilenindex:  <br/> |**visRowCharacter**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visCharacterComplexScriptSize** <br/> |
   

