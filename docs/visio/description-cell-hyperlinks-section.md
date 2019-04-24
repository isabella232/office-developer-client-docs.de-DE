---
title: Zelle "Description" (Abschnitt "Hyperlinks")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm230
localization_priority: Normal
ms.assetid: 2f571c65-6b7a-5a3a-c075-3c52d3ab989b
description: Stellt eine beschreibende Textzeichenfolge für einen Hyperlink dar.
ms.openlocfilehash: b58e6dc3ec2fc3b64db00e0f19e0718fe897aaa3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360242"
---
# <a name="description-cell-hyperlinks-section"></a>Zelle "Description" (Abschnitt "Hyperlinks")

Stellt eine beschreibende Textzeichenfolge für einen Hyperlink dar. 
  
## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Zelle, um Kommentare zum Hyperlink zu speichern. Beispiel: "Link zu unserer Preis-Website".
  
Sie können den Wert dieser Zelle auch im Dialogfeld **Hyperlinks** festlegen (klicken Sie dazu auf der Registerkarte **Einfügen** auf **Hyperlink**). 
  
Wenn Sie einen Verweis auf die Zelle Description aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Hyperlink.  *Name* . Beschreibung des Hyperlinks.  *Name* ist der Name der Hyperlink-Zeile.  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Description aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionHyperlink** <br/> |
| Zeilenindex:  <br/> |**visRow1stHyperlink** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visHLinkDescription** <br/> |
   

