---
title: Zelle "LineCap" (Abschnitt "Line Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251231
localization_priority: Normal
ms.assetid: 3519216b-b6cf-2e8c-e20f-adfa373c9028
description: Gibt an, ob eine Linie abgerundete, viereckige oder erweiterte Enden hat.
ms.openlocfilehash: 44de4bff87fd3d121dfce9eec934ec39bc61065a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359318"
---
# <a name="linecap-cell-line-format-section"></a>Zelle "LineCap" (Abschnitt "Line Format")

Gibt an, ob eine Linie abgerundete, viereckige oder erweiterte Enden hat.
  
|**Wert**|**Formatvorlage für das Linienende**|
|:-----|:-----|
|0  <br/> |Gerundet  <br/> |
|1  <br/> |Square  <br/> |
|2  <br/> |Erweitert  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können den Wert dieser Zelle auch im Dialogfeld **Linie** festlegen (klicken Sie dazu auf der Registerkarte **Start** in der Gruppe **Shape** auf **Linie**, zeigen Sie auf **Pfeile**, und klicken Sie dann auf **Weitere Pfeile**).
  
Wenn Sie einen Verweis auf die Zelle "LineCap aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |"LineCap  <br/> |
   
Wenn Sie einen Verweis auf die Zelle "LineCap aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowLine** <br/> |
|Zellenindex:  <br/> |**visLineEndCap** <br/> |
   

