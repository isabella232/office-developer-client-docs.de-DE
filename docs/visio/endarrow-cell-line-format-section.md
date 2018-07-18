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
ms.openlocfilehash: fa37e4896fdab0f2e8fee6d94aa38c72519a7e6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796930"
---
# <a name="endarrow-cell-line-format-section"></a>EndArrow Cell (Line Format Section)

Zeigt an, ob eine Linie eine Pfeilspitze oder eine andere Linienendformatierung an ihrem letzten Scheitelpunkt hat.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Keine Pfeilspitze  <br/> |
|1 – 45  <br/> |Verschiedene Pfeilspitzenformatvorlagen, die den indizierten Einträgen im Dialogfeld **Linie** entsprechen.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können diesen Wert auch im Dialogfeld **Linie** festlegen (klicken Sie dazu auf der Registerkarte **Start** in der Gruppe **Shape** auf **Linie**, zeigen Sie auf **Pfeile**, und klicken Sie dann auf **Weitere Pfeile**). Die Größe der Pfeilspitze wird in die Zelle EndArrowSize festgelegt.
  
Sie können ein benutzerdefiniertes Linienende über die Funktion VERWENDUNG in dieser Zelle angeben. 
  
Wenn Sie einen Verweis auf die Zelle EndArrow aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |EndArrow  <br/> |
   
Wenn Sie einen Verweis auf die Zelle EndArrow aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowLine** <br/> |
|Zellenindex:  <br/> |**visLineEndArrow** <br/> |
   

