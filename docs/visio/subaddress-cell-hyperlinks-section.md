---
title: Zelle "SubAddress" (Abschnitt "Hyperlinks")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm985
localization_priority: Normal
ms.assetid: 949448fd-0f85-b56a-945e-1da0e48609e8
description: Gibt eine Position im Zieldokument an, mit der eine Verknüpfung hergestellt werden kann.
ms.openlocfilehash: 092a53bd7c9d5adb77ed35f3e2ef53888bd6ebea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349322"
---
# <a name="subaddress-cell-hyperlinks-section"></a>Zelle "SubAddress" (Abschnitt "Hyperlinks")

Gibt eine Position im Zieldokument an, mit der eine Verknüpfung hergestellt werden kann.
  
## <a name="remarks"></a>Hinweise

Wenn die Zelle Address beispielsweise "Drawing1.vsdx" ist, kann die Zelle SubAddress einen Seitennamen wie "Page-3" angeben. Wenn die Zelle Address die Microsoft Excel "Samples.xlsx" ist, kann der Wert dieser Zelle ein Arbeitsblatt oder ein Bereich innerhalb eines Arbeitsblatts sein, z. B. "Worksheet Functions" oder "Sheet1! A1:D10". Wenn die Zelle Address den Wert " hat, kann der Wert dieser Zelle ein benannter Anker im Dokument sein, z. B. https://www.microsoft.com/office/ "lösungen".
  
Sie können den Wert dieser Zelle auch im Dialogfeld **Hyperlinks** festlegen (klicken Sie dazu auf der Registerkarte **Einfügen** in der Gruppe **Hyperlinks** auf **Hyperlink**).
  
Verwenden Sie zum Erhalten eines Verweises auf die Zelle SubAddress anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Hyperlink.  *Name*  . SubAddress, wobei Hyperlink  *.name*  der Zeilenname ist  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **Zelle SubAddress** nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionHyperlink** <br/> |
| Zeilenindex:  <br/> |**visRow1stHyperlink**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visHLinkSubAddress** <br/> |
   

