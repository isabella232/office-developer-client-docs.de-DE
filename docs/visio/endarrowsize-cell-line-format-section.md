---
title: Zelle "EndArrowSize" (Abschnitt "Line Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251630
localization_priority: Normal
ms.assetid: e2ecf7c0-a0e9-951f-676a-8e5857bb6544
description: Bestimmt die Pfeilspitzengröße am Linienende.
ms.openlocfilehash: 768a2b2adb05248049377eaee07194cdb89ed810
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438078"
---
# <a name="endarrowsize-cell-line-format-section"></a>Zelle "EndArrowSize" (Abschnitt "Line Format")

Bestimmt die Pfeilspitzengröße am Linienende.
  
|**Wert**|**Größe**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Sehr klein  <br/> |**visArrowSizeVerySmall** <br/> |
|1  <br/> |Small  <br/> |**visArrowSizeSmall** <br/> |
|2  <br/> |Mittel  <br/> |**visArrowSizeMedium** <br/> |
|3  <br/> |Large  <br/> |**visArrowSizeLarge** <br/> |
|4   <br/> |Sehr groß  <br/> |**visArrowSizeVeryLarge** <br/> |
|5   <br/> |Jumbo  <br/> |**visArrowSizeJumbo** <br/> |
|6   <br/> |Colossal  <br/> |**visArrowSizeColossal** <br/> |
   
## <a name="remarks"></a>Hinweise

Sie können diesen Wert auch im Dialogfeld **Linie** festlegen (klicken Sie dazu auf der Registerkarte **Start** in der Gruppe **Shape** auf **Linie**, zeigen Sie auf **Pfeile**, und klicken Sie dann auf **Weitere Pfeile**).
  
Um einen Verweis auf die Zelle EndArrowSize anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |EndArrowSize  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die EndArrowSize-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowLine** <br/> |
|Zellenindex:  <br/> |**visLineEndArrowSize** <br/> |
   

