---
title: Zelle "LineWeight" (Abschnitt "Line Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm585
localization_priority: Normal
ms.assetid: 16b0e293-eeef-34b4-aeb0-4472815dd543
description: Legt die Linienbreite eines Shapes fest. Definieren Sie die Linienbreite, indem Sie eine Zahl mit einer gültigen Maßeinheit eingeben.
ms.openlocfilehash: 654a93f939226bedab2e40ab591dad0e3f872267
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341811"
---
# <a name="lineweight-cell-line-format-section"></a>Zelle "LineWeight" (Abschnitt "Line Format")

Legt die Linienbreite eines Shapes fest. Definieren Sie die Linienbreite, indem Sie eine Zahl mit einer gültigen Maßeinheit eingeben.
  
## <a name="remarks"></a>Bemerkungen

Sie können den Wert von LineWeight auch im Dialogfeld **Linie** festlegen (Klicken Sie dazu auf der Registerkarte **Start** in der Gruppe **Shape** auf **Linie**, zeigen Sie auf **Gewicht**, und klicken Sie dann auf **Weitere Linien**).
  
Wenn die Maßeinheit nicht eingegeben wird, wird die im Dialogfeld **Visio-Optionen** angegebene Maßeinheit für Text verwendet (Klicken Sie auf die Registerkarte **Datei** , und klicken Sie dann auf **Optionen**). Die Linienbreite ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung maßstäblich ist, bleibt die Linienbreite unverändert. 
  
Wenn Sie einen Verweis auf die Zelle LineWeight aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LineWeight  <br/> |
   
Wenn Sie einen Verweis auf die Zelle LineWeight aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLine** <br/> |
| Zellenindex:  <br/> |**visLineWeight** <br/> |
   

