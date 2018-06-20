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
ms.openlocfilehash: 0509b9b6a708924b5aeb69f16f3f4cd99573cc0c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798218"
---
# <a name="subaddress-cell-hyperlinks-section"></a>SubAddress Cell (Hyperlinks Section)

Gibt eine Position im Zieldokument an, mit der eine Verknüpfung hergestellt werden kann.
  
## <a name="remarks"></a>Bemerkungen

Angenommen, wenn die Zelle Address "Drawing1.vsdx" ist, kann die Zelle SubAddress ein Seitenname wie "Seite 3" angeben. Wenn die Zelle Address der Microsoft Excel-Datei "Samples.xlsx" ist, kann der Wert dieser Zelle ein Arbeitsblatt oder einen Bereich in einem Arbeitsblatt, z. B. "Microsoft Excel-Arbeitsblattfunktionen" oder "Sheet1! sein A1: D10 ". Wenn die Zelle Address "http://www.microsoft.com/office/", kann der Wert dieser Zelle einen benannten Anker innerhalb des Dokuments, z. B. "Solutions" sein.
  
Sie können den Wert dieser Zelle auch im Dialogfeld **Hyperlinks** festlegen (klicken Sie in der Gruppe **Hyperlinks** auf der Registerkarte **Einfügen** auf **Hyperlink**).
  
Wenn Sie einen Verweis auf die Zelle SubAddress nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Hyperlink.  *Name* . SubAddress, in dem Hyperlink *.name* der Zeilenname ist  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **SubAddress** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionHyperlink** <br/> |
| Zeilenindex:  <br/> |**visRow1stHyperlink** +  *i* wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visHLinkSubAddress** <br/> |
   

