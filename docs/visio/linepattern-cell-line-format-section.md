---
title: Zelle "LinePattern" (Abschnitt "Line Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm560
localization_priority: Normal
ms.assetid: a416762b-7294-c99f-d9f1-332c3ed35dff
description: Definiert das Linienmuster eines Shapes. Der in die Zelle LinePattern eingegebene Wert ist eine Zahl, die einen Index für eine Linienmustersammlung darstellt.
ms.openlocfilehash: eec5bed18777f7822f9544d59dce7722f2f732bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416755"
---
# <a name="linepattern-cell-line-format-section"></a>Zelle "LinePattern" (Abschnitt "Line Format")

Definiert das Linienmuster eines Shapes. Der in die Zelle LinePattern eingegebene Wert ist eine Zahl, die einen Index für eine Linienmustersammlung darstellt.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Kein Linienmuster  <br/> |
|1  <br/> |Einfarbig  <br/> |
|2 - 23  <br/> |Verschiedene Linienmuster  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können sich die Linienmustersammlung auch im Dialogfeld **Linie** ansehen (klicken Sie dazu auf der Registerkarte **Start** in der Gruppe **Shape** auf **Linie**, zeigen Sie auf **Strichlinien**, und klicken Sie dann auf **Weitere Linien**).
  
Um ein benutzerdefiniertes Linienmuster anzugeben, verwenden Sie die Funktion VERWENDUNG in dieser Zelle.
  
Wenn Sie einen Verweis auf die Zelle "LinePattern aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |"LinePattern  <br/> |
   
Wenn Sie einen Verweis auf die Zelle "LinePattern aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowLine** <br/> |
|Zellenindex:  <br/> |**visLinePattern** <br/> |
   

