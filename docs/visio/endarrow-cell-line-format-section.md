---
title: Zelle "EndArrow" (Abschnitt "Line Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm320
ms.localizationpriority: medium
ms.assetid: 2f9c11ba-a316-bc34-60d4-0a41b2af486f
description: Zeigt an, ob eine Linie eine Pfeilspitze oder eine andere Linienendformatierung an ihrem letzten Scheitelpunkt hat.
ms.openlocfilehash: 186c16762103aab59b3162f5706b0ca31ecfe9b4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559899"
---
# <a name="endarrow-cell-line-format-section"></a>Zelle "EndArrow" (Abschnitt "Line Format")

Zeigt an, ob eine Linie eine Pfeilspitze oder eine andere Linienendformatierung an ihrem letzten Scheitelpunkt hat.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Keine Pfeilspitze  <br/> |
|1 - 45  <br/> |Verschiedene Pfeilspitzenformatvorlagen, die den indizierten Einträgen im Dialogfeld **Linie** entsprechen.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Sie können diesen Wert auch im Dialogfeld **Linie** festlegen (klicken Sie dazu auf der Registerkarte **Start** in der Gruppe **Shape** auf **Linie**, zeigen Sie auf **Pfeile**, und klicken Sie dann auf **Weitere Pfeile**). Die Größe der Pfeilspitze wird in der Zelle EndArrowSize festgelegt.
  
Sie können ein benutzerdefiniertes Linienende über die Funktion VERWENDUNG in dieser Zelle angeben. 
  
Um einen Verweis auf die Zelle "EndArrow" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |EndArrow  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle EndArrow anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowLine** <br/> |
|Zellenindex:  <br/> |**visLineEndArrow** <br/> |
   

