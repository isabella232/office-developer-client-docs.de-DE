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
ms.openlocfilehash: c3410ad15581ff1704d7a43dd7ed5fa193f668b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797807"
---
# <a name="relationships-cell-shape-layout-section"></a>Relationships Cell (Shape Layout Section)

Speichert die Beziehungen zwischen Containern, Listen, Beschriftungen und Shapes. 
  
## <a name="remarks"></a>Bemerkungen

 Microsoft Visio verwendet die Zelle Relationships die Beziehungen zu speichern, die dieses Shape betreffen. Eine Reihe von DEPENDSON-Funktion, mit den Parametern dargestellt, werden verwendet, um mit diesem Shape Beziehungen darstellen, wie in der folgenden Tabelle dargestellt. 
  
|**Erster parameter**|**Zusätzliche Parameter**|
|:-----|:-----|
|1  <br/> |Shapes, die Elemente dieses Containers sind  <br/> |
|2  <br/> |Shapes, die Elemente dieser Liste sind  <br/> |
|3  <br/> |Beschriftungen, die mit diesem Shape verknüpft sind  <br/> |
|4  <br/> |Container, zu deren Elementen dieses Shape gehört  <br/> |
|5  <br/> |Listen, zu denen dieses Listenelement gehört  <br/> |
|6  <br/> |Shape, das mit dieser Beschriftung verknüpft ist  <br/> |
|7  <br/> |Container an der linken Begrenzungskante, an der sich dieses Shape befindet  <br/> |
|8  <br/> |Container an der rechten Begrenzungskante, an der sich dieses Shape befindet  <br/> |
|9  <br/> |Container an der oberen Begrenzungskante, an der sich dieses Shape befindet  <br/> |
|10  <br/> |Container an der unteren Begrenzungskante, an der sich dieses Shape befindet  <br/> |
|11  <br/> |Liste, die von dieser Liste überlappt wird  <br/> |
   
Zum Abrufen eines Verweises auf die Zelle Relationships nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Relationships  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Relationships aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
|Zellenindex:  <br/> |**visSLORelationships** <br/> |
   

