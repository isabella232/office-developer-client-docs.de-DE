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
ms.openlocfilehash: a8bfc045559a2c2904ae4a97c489248fb6c446c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796816"
---
# <a name="default-cell-hyperlinks-section"></a>Default Cell (Hyperlinks Section)

Legt den Standardhyperlink für ein Shape oder eine Seite fest. Setzen Sie den Wert dieser Zelle auf WAHR, um einen Hyperlink als Standardeinstellung festzulegen.
  
## <a name="remarks"></a>Bemerkungen

Sie können den Standardhyperlink auch festlegen, indem Sie ein Shape auswählen, auf der Registerkarte **Einfügen** auf **Hyperlink** klicken, einen Hyperlink auswählen und anschließend auf **Standard** klicken. Der Standardhyperlink wird fett angezeigt.
  
Wenn Sie einen Verweis auf die Zelle Default aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Hyperlink. *Name* . Standard, in dem Hyperlink. *Name* ist der Zeilenname  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Default aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionHyperlink** <br/> |
|Zeilenindex:  <br/> |**visRow1stHyperlink** +  *i* wobei *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visHLinkDefault** <br/> |
   

