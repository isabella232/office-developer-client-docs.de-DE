---
title: Zelle "BeginArrow" (Abschnitt "Line Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm51105
localization_priority: Normal
ms.assetid: 0ab4044e-2d77-1fbe-ef20-5d029bc064ba
description: Zeigt an, ob eine Linie eine Pfeilspitze oder eine andere Linienendformatierung an ihrem ersten Scheitelpunkt hat. Geben Sie eine Zahl zwischen 0 und 45 oder die USE-Funktion zusammen mit dem Namen des benutzerdefinierten Linienendes ein, oder verwenden Sie das Dialogfeld Linie.
ms.openlocfilehash: cf5a512dabd0e6296b83fa7bfd2a2a6134143d50
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346235"
---
# <a name="beginarrow-cell-line-format-section"></a>Zelle "BeginArrow" (Abschnitt "Line Format")

Zeigt an, ob eine Linie eine Pfeilspitze oder eine andere Linienendformatierung an ihrem ersten Scheitelpunkt hat. Geben Sie eine Zahl zwischen 0 und 45 oder die USE-Funktion zusammen mit dem Namen des benutzerdefinierten Linienendes ein, oder verwenden Sie das Dialogfeld **Linie**. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| 0  <br/> | Keine Pfeilspitze  <br/> |
| 1 - 45  <br/> | Verschiedene Pfeilspitzenformatvorlagen, die den indizierten Einträgen im Dialogfeld **Linie** entsprechen.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die Größe der Pfeilspitze wird in der Zelle PfeilBeginnGröße angegeben.
  
Wenn Sie einen Verweis auf die Zelle beginArrow aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Zelle BeginArrow  <br/> |
   
Wenn Sie einen Verweis auf die Zelle beginArrow aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLine** <br/> |
| Zellenindex:  <br/> |**visLineBeginArrow** <br/> |
   

