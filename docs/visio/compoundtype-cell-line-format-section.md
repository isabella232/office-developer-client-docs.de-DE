---
title: Zusammengesetzte Zelle (Abschnitt "Linien Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3e2a88ad-d92c-4550-8da3-fa7fdd032e73
description: Bestimmt den zusammengesetzten Typ der Form.
ms.openlocfilehash: 120975e419656234266cb8151b2fa37ef19602e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407172"
---
# <a name="compoundtype-cell-line-format-section"></a>Zusammengesetzte Zelle (Abschnitt "Linien Format")

Bestimmt den zusammengesetzten Typ der Form. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Einfach  <br/> |
|1  <br/> |Gleitkommawert mit doppelter Genauigkeit  <br/> |
|2  <br/> |Dünn  <br/> |
|3  <br/> |Dünn  <br/> |
|4  <br/> |Triple  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die **** Zelle compoundtype aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Compoundtype  <br/> |
   
Wenn Sie einen Verweis auf die **** Zelle compoundtype nach Index aus einem Programm erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLine** <br/> |
| Zellenindex:  <br/> |**visCompoundType** <br/> |
   

