---
title: Zelle "SubAddress" (Abschnitt "Hyperlinks")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm985
ms.localizationpriority: medium
ms.assetid: 949448fd-0f85-b56a-945e-1da0e48609e8
description: Gibt eine Position im Zieldokument an, mit der eine Verknüpfung hergestellt werden kann.
ms.openlocfilehash: cd3c69e932c393c463b9aa4ee1a0ebff1817d45e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569923"
---
# <a name="subaddress-cell-hyperlinks-section"></a>Zelle "SubAddress" (Abschnitt "Hyperlinks")

Gibt eine Position im Zieldokument an, mit der eine Verknüpfung hergestellt werden kann.
  
## <a name="remarks"></a>HinwBemerkungeneise

Wenn die Zelle Address z. B. Drawing1.vsdx lautet, kann die Zelle SubAddress einen Seitennamen wie z. B. Page-3 angeben. Wenn die Zelle Address die Microsoft Excel Datei Samples.xlsx ist, kann der Wert dieser Zelle ein Arbeitsblatt oder ein Bereich innerhalb eines Arbeitsblatts sein, z. B. "Worksheet Functions" oder "Sheet1! A1:D10". Wenn die Zelle https://www.microsoft.com/office/ Address den Wert "" aufweist, kann der Wert dieser Zelle ein benannter Anker innerhalb des Dokuments sein, z. B. "Lösungen".
  
Sie können den Wert dieser Zelle auch im Dialogfeld **Hyperlinks** festlegen (klicken Sie dazu auf der Registerkarte **Einfügen** in der Gruppe **Hyperlinks** auf **Hyperlink**).
  
Um einen Verweis auf die Zelle "SubAddress" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Hyperlink.  *Name*  . SubAddress, wobei Hyperlink  *.name*  der Zeilenname ist  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle **SubAddress** anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionHyperlink** <br/> |
| Zeilenindex:  <br/> |**visRow1stHyperlink**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visHLinkSubAddress** <br/> |
   

