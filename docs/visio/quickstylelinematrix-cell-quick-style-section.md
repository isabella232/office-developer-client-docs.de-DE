---
title: QuickStyleLineMatrix Cell (Quick Style section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b10221d-30f8-48f5-81ed-0283fdfc3e5d
description: Bestimmt die Formatvorlage für die Schnellformatvorlage, die von der Form erbt, als ganze Zahl von 0-6.
ms.openlocfilehash: e04fc6328d40b0564364aa8feff971628360d813
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410819"
---
# <a name="quickstylelinematrix-cell-quick-style-section"></a>QuickStyleLineMatrix Cell (Quick Style section)

Bestimmt die Formatvorlage für die Schnellformatvorlage, die von der Form erbt, als ganze Zahl von 0-6. 
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **QuickStyleLineMatrix** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | QuickStyleLineMatrix  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **QuickStyleLineMatrix** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowQuickStyleProperties** <br/> |
| Zellenindex:  <br/> |**visQuickStyleLineMatrix** <br/> |
   

