---
title: Zelle "Relationships" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80005
localization_priority: Normal
ms.assetid: 4168cd98-9674-1233-254f-0afe81b7245b
description: Speichert die Beziehungen zwischen Containern, Listen, Beschriftungen und Shapes.
ms.openlocfilehash: b270366fe1045aea3d628150c82e7fd798fa21df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406409"
---
# <a name="relationships-cell-shape-layout-section"></a>Zelle "Relationships" (Abschnitt "Shape Layout")

Speichert die Beziehungen zwischen Containern, Listen, Beschriftungen und Shapes. 
  
## <a name="remarks"></a>Hinweise

 Microsoft Visio verwendet die Zelle Beziehungen, um die Beziehungen zu speichern, die dieses Shape betreffen. Zum Darstellen der Beziehungen zu diesem Shape wird eine Reihe von DEPENDSON-Funktionen mit den angegebenen Parametern verwendet, wie in der nachstehenden Tabelle dargestellt. 
  
|**Erster Parameter**|**Zusätzliche Parameter**|
|:-----|:-----|
|1  <br/> |Shapes, die Elemente dieses Containers sind  <br/> |
|2  <br/> |Shapes, die Elemente dieser Liste sind  <br/> |
|3  <br/> |Beschriftungen, die mit diesem Shape verknüpft sind  <br/> |
|4   <br/> |Container, zu deren Elementen dieses Shape gehört  <br/> |
|5   <br/> |Listen, zu denen dieses Listenelement gehört  <br/> |
|6   <br/> |Shape, das mit dieser Beschriftung verknüpft ist  <br/> |
|7   <br/> |Container an der linken Begrenzungskante, an der sich dieses Shape befindet  <br/> |
|8   <br/> |Container an der rechten Begrenzungskante, an der sich dieses Shape befindet  <br/> |
|9   <br/> |Container an der oberen Begrenzungskante, an der sich dieses Shape befindet  <br/> |
|10  <br/> |Container an der unteren Begrenzungskante, an der sich dieses Shape befindet  <br/> |
|11  <br/> |Liste, die von dieser Liste überlappt wird  <br/> |
   
Verwenden Sie zum Erhalten eines Verweises auf die Zelle Beziehungen anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Beziehungen  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Beziehungen nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
|Zellenindex:  <br/> |**visSLORelationships** <br/> |
   

