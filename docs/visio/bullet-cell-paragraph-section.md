---
title: Zelle "Bullet" (Abschnitt "Paragraph")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm130
localization_priority: Normal
ms.assetid: 124a5ee1-6dd1-d17d-6f0e-dbaa5d95d9cd
description: Bestimmt das Aufzählungszeichenformat.
ms.openlocfilehash: 03b7d046cd42458b614313c19b2100259730539c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422768"
---
# <a name="bullet-cell-paragraph-section"></a>Zelle "Bullet" (Abschnitt "Paragraph")

Bestimmt das Aufzählungszeichenformat.
  
|**Wert**|**Formatvorlage für Aufzählungszeichen**|
|:-----|:-----|
|0  <br/> |None  <br/> |
|1  <br/> |![](media/IC_Bullet1_ZA07645847.gif)           <br/> |
|2  <br/> |![](media/IC_Bullet2_ZA07645848.gif)           <br/> |
|3  <br/> |![](media/IC_Bullet3_ZA07645849.gif)           <br/> |
|4   <br/> |![](media/IC_Bullet4_ZA07645851.gif)           <br/> |
|5   <br/> |![](media/IC_Bullet5_ZA07645852.gif)           <br/> |
|6   <br/> |![](media/IC_Bullet6_ZA07645853.gif)           <br/> |
|7   <br/> |![](media/IC_Bullet7_ZA07645854.gif)           <br/> |
   
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionParagraph** <br/> |
|Zeilenindex:  <br/> |**visRowParagraph**  +   *i* where *i* = 0, 1, 2, ...  <br/> |
|Zellenindex:  <br/> |**visBulletIndex** <br/> |
   
## <a name="remarks"></a>Hinweise

Sie können den Wert für diese Zelle auch festlegen, indem Sie mit der rechten Maustaste auf ein Shape klicken, auf **Format** zeigen, auf **Text** klicken und dann die Registerkarte **Aufzählungszeichen** auswählen. 
  
Verwenden Sie zum Erhalten eines Verweises auf die Zelle Bullet anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Para.Bullet[ *i*  ] where  *i*  = <1>, 2, 3, ...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Bullet nach Index aus einem Programm zu erhalten: 
  

