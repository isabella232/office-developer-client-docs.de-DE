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
ms.openlocfilehash: a5207607d90ef6a79dcb3acc191521b73e2cdf54
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797339"
---
# <a name="lineweight-cell-line-format-section"></a>LineWeight Cell (Line Format Section)

Legt die Linienbreite eines Shapes fest. Definieren Sie die Linienbreite, indem Sie eine Zahl mit einer gültigen Maßeinheit eingeben.
  
## <a name="remarks"></a>Bemerkungen

Sie können den Wert von LineWeight auch im Dialogfeld Linie definieren (klicken Sie auf der Registerkarte Start in der Gruppe Shape auf Linie, zeigen Sie auf Linienbreite, und klicken Sie dann auf Weitere Linien).
  
Wenn die Einheit nicht eingegeben wird, wird die Maßeinheit für den Text im Dialogfeld **Visio-Optionen** (klicken Sie auf der Registerkarte **Datei** , und klicken Sie dann auf **Optionen**). Linienbreite ist unabhängig von der Skalierung der Zeichnung. Wenn die Zeichnung skaliert wird, bleibt die Linienstärke unverändert. 
  
Wenn Sie einen Bezug auf die Zelle Name aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LineWeight  <br/> |
   
Wenn Sie einen Bezug auf die Zelle LineWeight aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLine** <br/> |
| Zellenindex:  <br/> |**visLineWeight** <br/> |
   

