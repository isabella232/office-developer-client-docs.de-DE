---
title: Zelle "FillPattern" (Abschnitt "Fill Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm375
ms.localizationpriority: medium
ms.assetid: dac82a4f-4508-541a-e118-7d79df987232
description: Legt das Füllmuster für das Shape fest. Verwenden Sie die USE-Funktion in dieser Zelle, um ein benutzerdefiniertes Füllmuster anzugeben.
ms.openlocfilehash: 3a8a07add43f980f124ff532e2b04939f2324284
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570679"
---
# <a name="fillpattern-cell-fill-format-section"></a>Zelle "FillPattern" (Abschnitt "Fill Format")

Legt das Füllmuster für das Shape fest. Verwenden Sie die USE-Funktion in dieser Zelle, um ein benutzerdefiniertes Füllmuster anzugeben.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Keine (transparente Füllung).  <br/> |
|1  <br/> |Einfarbige Vordergrundfarbe.  <br/> |
|2 - 40  <br/> |Verschiedene Füllmuster, die den indizierten Einträgen im Dialogfeld **Füllbereich** entsprechen.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Sie können diesen Wert auch über das Dialogfeld **Füllbereich** festlegen (klicken Sie dazu auf der Registerkarte **Start** in der Gruppe **Shape** auf **Füllbereich**, und klicken Sie dann auf **Füllbereichsoptionen**).
  
Um einen Verweis auf die Zelle "FillPattern" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |FillPattern  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle FillPattern anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowFill** <br/> |
|Zellenindex:  <br/> |**visFillPattern** <br/> |
   

