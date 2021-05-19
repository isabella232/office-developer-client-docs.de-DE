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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434354"
---
# <a name="default-cell-hyperlinks-section"></a>Zelle "Default" (Abschnitt "Hyperlinks")

Legt den Standardhyperlink für ein Shape oder eine Seite fest. Setzen Sie den Wert dieser Zelle auf WAHR, um einen Hyperlink als Standardeinstellung festzulegen.
  
## <a name="remarks"></a>Hinweise

Sie können den Standardhyperlink auch festlegen, indem Sie ein Shape auswählen, auf der Registerkarte **Einfügen** auf **Hyperlink** klicken, einen Hyperlink auswählen und anschließend auf **Standard** klicken. Der Standardhyperlink wird fett angezeigt.
  
Um einen Verweis auf die Standardzelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Hyperlink. *Name*  . Standard, wobei Hyperlink. *Name*  ist der Zeilenname  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Standardzelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionHyperlink** <br/> |
|Zeilenindex:  <br/> |**visRow1stHyperlink**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visHLinkDefault** <br/> |
   

