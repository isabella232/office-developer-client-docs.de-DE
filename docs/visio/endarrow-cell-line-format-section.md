---
title: Zelle "EndArrow" (Abschnitt "Line Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm320
localization_priority: Normal
ms.assetid: 2f9c11ba-a316-bc34-60d4-0a41b2af486f
description: Zeigt an, ob eine Linie eine Pfeilspitze oder eine andere Linienendformatierung an ihrem letzten Scheitelpunkt hat.
ms.openlocfilehash: 54ef11125a8774914a60897850fb75cd4ab949a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434683"
---
# <a name="endarrow-cell-line-format-section"></a>Zelle "EndArrow" (Abschnitt "Line Format")

Zeigt an, ob eine Linie eine Pfeilspitze oder eine andere Linienendformatierung an ihrem letzten Scheitelpunkt hat.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Keine Pfeilspitze  <br/> |
|1 - 45  <br/> |Verschiedene Pfeilspitzenformatvorlagen, die den indizierten Einträgen im Dialogfeld **Linie** entsprechen.  <br/> |
   
## <a name="remarks"></a>Hinweise

Sie können diesen Wert auch im Dialogfeld **Linie** festlegen (klicken Sie dazu auf der Registerkarte **Start** in der Gruppe **Shape** auf **Linie**, zeigen Sie auf **Pfeile**, und klicken Sie dann auf **Weitere Pfeile**). Die Größe der Pfeilspitze wird in der Zelle EndArrowSize festgelegt.
  
Sie können ein benutzerdefiniertes Linienende über die Funktion VERWENDUNG in dieser Zelle angeben. 
  
Verwenden Sie zum Erhalten eines Verweises auf die Zelle EndArrow anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |EndArrow  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die EndArrow-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowLine** <br/> |
|Zellenindex:  <br/> |**visLineEndArrow** <br/> |
   

