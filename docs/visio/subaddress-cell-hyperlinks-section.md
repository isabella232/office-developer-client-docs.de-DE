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
  
## <a name="remarks"></a>Bemerkungen

Wenn die Zelle Address beispielsweise "Zeichnung1. vsdx" ist, kann die Zelle unter Adresse einen Seitennamen wie "page-3" angeben. Wenn die Zelle address die Microsoft Excel-Datei Samples. xlsx ist, kann der Wert dieser Zelle ein Arbeitsblatt oder ein Bereich innerhalb eines Arbeitsblatts sein, beispielsweise "Arbeitsblattfunktionen" oder "Sheet1! A1: D10 ". Wenn die Zelle Address "https://www.microsoft.com/office/" ist, kann der Wert dieser Zelle ein benannter Anker innerhalb des Dokuments sein, beispielsweise "Lösungen".
  
Sie können den Wert dieser Zelle auch im Dialogfeld **Hyperlinks** festlegen (klicken Sie dazu auf der Registerkarte **Einfügen** in der Gruppe **Hyperlinks** auf **Hyperlink**).
  
Wenn Sie einen Verweis auf die Zelle subAddress aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Hyperlink.  *Name* . Unter Adresse, bei der Hyperlink *. Name* der Zeilenname ist  <br/> |
   
Wenn Sie einen Verweis auf die **** Zelle SubAddress aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionHyperlink** <br/> |
| Zeilenindex:  <br/> |**visRow1stHyperlink** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visHLinkSubAddress** <br/> |
   

