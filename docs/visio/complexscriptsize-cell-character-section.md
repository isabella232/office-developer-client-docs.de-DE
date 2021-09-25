---
title: Zelle "ComplexScriptSize" (Abschnitt "Character")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033768
ms.localizationpriority: medium
ms.assetid: f58687d7-2ba4-ff77-0bcc-3106867d89de
description: Der Schriftgrad zum Formatieren von Text mit komplexen Schriftzeichen.
ms.openlocfilehash: 8d810cecb7f9bd1d80895892a362d808f8adc3f7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608473"
---
# <a name="complexscriptsize-cell-character-section"></a>Zelle "ComplexScriptSize" (Abschnitt "Character")

Der Schriftgrad zum Formatieren von Text mit komplexen Schriftzeichen. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Komplexe Schriftgraden sind auf der Registerkarte **"Schriftart"** im Dialogfeld **"Text"** aufgeführt (klicken Sie auf der Registerkarte **"Start"** in der Gruppe **"Schriftart"** auf den Pfeil). Diese Liste wird nur angezeigt, wenn Sie im Dialogfeld Microsoft Office **Spracheinstellungen** eine Sprache hinzugefügt haben, die asiatische oder komplexe Skriptzeichen enthält. (Klicken Sie auf **"Start",** auf **"Alle Programme",** auf **Microsoft Office,** auf **Microsoft Office "Extras"** und dann auf **Microsoft Office "Spracheinstellungen".**
  
Sie können diesen Wert als explizite Größe in Punkt oder als Prozentsatz angeben. Wenn Sie einen Prozentsatz angeben, basiert der Wert auf dem Wert in der Zelle Größe. Der Standardwert von 0 (Null) bedeutet 100 %. 
  
Um einen Verweis auf die Zelle "ComplexScriptSize" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Char.ComplexScriptSize[ *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle ComplexScriptSize anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionCharacter** <br/> |
|Zeilenindex:  <br/> |**visRowCharacter**  +   *i* where *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visCharacterComplexScriptSize** <br/> |
   

