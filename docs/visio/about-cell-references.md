---
title: Informationen zu Zellbezügen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251827
localization_priority: Normal
ms.assetid: e6a9aceb-90d7-fb53-eaf4-416a1ae2a98b
description: Sie können gegenseitige Abhängigkeiten zwischen Formeln mithilfe von ShapeSheet-Zellbezügen erstellen. Zellbezüge ermöglichen es Ihnen, einen Wert für eine Zelle zu berechnen, der auf dem Wert einer anderen Zelle basiert. Die Zelle Width eines Shapes kann beispielsweise eine Formel enthalten, die die Breite des Shapes berechnet, indem sie auf den Wert seiner Zelle Height verweist, sodass die Breite des Shapes proportional unverändert bleibt, wenn ein Benutzer die vertikale Größe des Shapes ändert.
ms.openlocfilehash: 54c7fd69e2ddaa9350996e2d8c921958a04e34ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796364"
---
# <a name="about-cell-references"></a>Informationen zu Zellbezügen

Sie können gegenseitige Abhängigkeiten zwischen Formeln mithilfe von ShapeSheet-Zellbezügen erstellen. Zellbezüge ermöglichen es Ihnen, einen Wert für eine Zelle zu berechnen, der auf dem Wert einer anderen Zelle basiert. Die Zelle Width eines Shapes kann beispielsweise eine Formel enthalten, die die Breite des Shapes berechnet, indem sie auf den Wert seiner Zelle Height verweist, sodass die Breite des Shapes proportional unverändert bleibt, wenn ein Benutzer die vertikale Größe des Shapes ändert.
  
In der Formel einer Zelle können Sie auf eine Zelle in demselben Shape oder in einem anderen Objekt (z. B. Dokument oder Zeichenblatt) verweisen, damit Microsoft Visio einen Wert für eine Zelle anhand des Werts einer anderen Zelle berechnet.
  
## <a name="what-cell-references-can-include"></a>Mögliche Inhalte von Zellbezügen

Zellbezüge können Shape binären IDs oder Namen enthalten. Sie können jederzeit auf jedes beliebige Shape auf der Seite, anhand dessen ID verweisen, ob das Shape oder nicht benannt wird. Wenn ein Shape noch nicht benannt wurde, ist der Standardname Blatt. *i* , wobei *i* die Shape-ID ist Die ID wird zugewiesen, wenn das Shape erstellt und nicht geändert werden, wird es sei denn, Sie Shapes in einer anderen Seite oder einem Dokument verschieben. Wenn mehr als eine Form auf einer Seite, den denselben Namen hat, müssen Sie die zugewiesene ID einbeziehen. 
  
## <a name="cell-reference-syntax-and-examples"></a>Syntax und Beispiele für Zellbezüge

Die von Ihnen verwendete Syntax und die Möglichkeit, anhand eines Namens auf ein Shape verweisen zu können, hängt von der Beziehung zwischen den beiden Objekten ab. Es gelten die folgenden allgemeinen Regeln:
  
- Wenn ein Shape mit dem gerade von Ihnen bearbeiteten Shapes gleichrangig ist, können Sie auf das gleichrangige Shape anhand des Namens verweisen. Wenn das gleichrangige Shape eine Gruppe ist, können Sie anhand eines Namens auf die Gruppe, jedoch nicht auf deren Mitglieder verweisen. Darüber hinaus können Sie auch nicht anhand eines Namens auf das übergeordnete Objekt eines Shapes oder die gleichrangigen Shapes des übergeordneten Objekts verweisen.
    
- Sie können die Syntax Blatt.ID verwenden, um auf jedes beliebige Shape auf dem Zeichenblatt zu verweisen, unabhängig davon, ob sich das Shape in einer Gruppe befindet oder ob es sich dabei um ein übergeordnetes Objekt eines Shapes handelt.
    
- Namen, die nicht standardmäßige Zeichen enthalten, müssen in einfache Anführungszeichen eingeschlossen werden. Einfachen Anführungszeichen in einem nicht standardmäßigen Namen muss ein einfaches Anführungszeichen vorangestellt werden.
    
|**Um auf eine Zelle zu verweisen**|**Verwenden Sie diese syntax**|**Beispiel**|
|:-----|:-----|:-----|
|
                
                
                Dasselbe Shape
  <br/> | Abrufen CellName  <br/> | Breite  <br/> |
| 
                
                
                Ein Shape, eine Gruppe oder Führungslinie
  <br/> | Shapename! Abrufen CellName  <br/> | 
                
                
                Stern!Winkel
  <br/> |
| 
                
                
                Ein Shape, eine Gruppe oder Führungslinie, in denen mehrere Shapes auf derselben Ebene denselben Namen aufweisen
  <br/> | Shapename.ID! Abrufen CellName  <br/> | Executive.2! Höhe  <br/> |
| 
                
                
                Eine Spalte mit Namen mit indizierten Zeilen
  <br/> | Section.Column[index]  <br/> | Char.Font[3]  <br/> |
| 
                
                
                Eine Spalte ohne Namen mit indizierten Zeilen
  <br/> | Section.ColumnIndex  <br/> | Scratch.A5  <br/> |
| 
                
                
                Jedes beliebige Shape, jedes Zeichenblatt, jedes Master-Shape oder jede Formatvorlage
  <br/> | Blatt.ID! Abrufen CellName  <br/> | Sheet.8! FillForegnd  <br/> |
| 
                
                
                Ein Master-Shape
  <br/> | Masters [MasterName]! Arbeitsblattname! Zellbezug  <br/> | Master [Zahnrad]! Welle! Geometry1.x1  <br/> |
| 
                
                
                Die Zeichenblatt oder Master-Shape, auf dem sich das Objekt befindet
  <br/> | ThePage! Zellbezug  <br/> | ThePage! User.Vanishing_Point  <br/> |
| 
                
                
                Ein anderes Zeichenblatt im Dokument
  <br/> | Seiten [PageName]! Arbeitsblattname! Zellbezug  <br/> | Seiten [Seite 3]! Sheet4! BeginX  <br/> |
| 
                
                
                Eine Formatvorlage
  <br/> | Formatvorlagen! Arbeitsblattname! Zellbezug  <br/> | Formatvorlagen! Manager! LineColor  <br/> |
| 
                
                
                Das Dokument
  <br/> | TheDoc! Zellbezug  <br/> | TheDoc! PreviewQuality  <br/> |
| 
                
                
                Ein Shape, ein Zeichenblatt, ein Master-Shape, ein Dokument oder eine Formatvorlage mit einem nicht standardmäßigen Namen.
  <br/> | "Arbeitsblattname!" Abrufen CellName  <br/> | "1-D'! LineColor  <br/> |
   

