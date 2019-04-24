---
title: Zelle "Default" (Abschnitt "Hyperlinks")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251545
localization_priority: Normal
ms.assetid: 0edea0ea-58dd-15da-6d4f-185d40133452
description: Legt den Standardhyperlink für ein Shape oder eine Seite fest. Setzen Sie den Wert dieser Zelle auf WAHR, um einen Hyperlink als Standardeinstellung festzulegen.
ms.openlocfilehash: 9991bd0e241c5dfd4fda65aeff8b6cc203ad3458
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360277"
---
# <a name="default-cell-hyperlinks-section"></a>Zelle "Default" (Abschnitt "Hyperlinks")

Legt den Standardhyperlink für ein Shape oder eine Seite fest. Setzen Sie den Wert dieser Zelle auf WAHR, um einen Hyperlink als Standardeinstellung festzulegen.
  
## <a name="remarks"></a>Bemerkungen

Sie können den Standardhyperlink auch festlegen, indem Sie ein Shape auswählen, auf der Registerkarte **Einfügen** auf **Hyperlink** klicken, einen Hyperlink auswählen und anschließend auf **Standard** klicken. Der Standardhyperlink wird fett angezeigt.
  
Wenn Sie einen Verweis auf die Standardzelle nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Hyperlink. *Name* . Standard, wobei Hyperlink. *Name* ist der Name der Zeile  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Default aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionHyperlink** <br/> |
|Zeilenindex:  <br/> |**visRow1stHyperlink** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visHLinkDefault** <br/> |
   

