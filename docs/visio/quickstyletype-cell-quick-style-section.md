---
title: Zelle "QuickStyleType" (Abschnitt "Quick Style")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7470417-0d70-433e-9496-604ca2eafee6
description: Bestimmt den Typ der Schnellformatvorlage (2-dimensional, 1-dimensional oder Verbinder), den die Form erbt.
ms.openlocfilehash: 95aced62c6397fc3229de29b98d3f18e5f69d05b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410504"
---
# <a name="quickstyletype-cell-quick-style-section"></a>Zelle "QuickStyleType" (Abschnitt "Quick Style")

Bestimmt den Typ der Schnellformatvorlage (2-dimensional, 1-dimensional oder Verbinder), den die Form erbt. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Visio automatisch auswählen  <br/> |
|1  <br/> |1-dimensional  <br/> |
|2  <br/> |2-dimensional  <br/> |
|3  <br/> |Connector  <br/> |
   
## <a name="remarks"></a>Hinweise

Verwenden Sie zum Erhalten eines Verweises auf die **Zelle QuickStyleType** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | QuickStyleType  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **QuickStyleType-Zelle** nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowQuickStyleProperties** <br/> |
| Zellenindex:  <br/> |**visQuickStyleType** <br/> |
   

