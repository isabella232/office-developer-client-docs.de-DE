---
title: Zelle "LinePattern" (Abschnitt "Line Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm560
ms.localizationpriority: medium
ms.assetid: a416762b-7294-c99f-d9f1-332c3ed35dff
description: Definiert das Linienmuster eines Shapes. Der in die Zelle LinePattern eingegebene Wert ist eine Zahl, die einen Index für eine Linienmustersammlung darstellt.
ms.openlocfilehash: e17227418fe358cb66a3ab7983940527510d8c62
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623411"
---
# <a name="linepattern-cell-line-format-section"></a>Zelle "LinePattern" (Abschnitt "Line Format")

Definiert das Linienmuster eines Shapes. Der in die Zelle LinePattern eingegebene Wert ist eine Zahl, die einen Index für eine Linienmustersammlung darstellt.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Kein Linienmuster  <br/> |
|1  <br/> |Einfarbig  <br/> |
|2 - 23  <br/> |Verschiedene Linienmuster  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können sich die Linienmustersammlung auch im Dialogfeld **Linie** ansehen (klicken Sie dazu auf der Registerkarte **Start** in der Gruppe **Shape** auf **Linie**, zeigen Sie auf **Strichlinien**, und klicken Sie dann auf **Weitere Linien**).
  
Um ein benutzerdefiniertes Linienmuster anzugeben, verwenden Sie die Funktion VERWENDUNG in dieser Zelle.
  
Um einen Verweis auf die Zelle "LinePattern" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |LinePattern  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle LinePattern anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowLine** <br/> |
|Zellenindex:  <br/> |**visLinePattern** <br/> |
   

