---
title: Zelle "LockTextEdit" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm665
localization_priority: Normal
ms.assetid: d8de5fa4-826b-e869-4d9f-997361d05fd8
description: Sperrt den Text eines Shapes, damit dieser nicht bearbeitet werden kann.
ms.openlocfilehash: f6e5176e3ab654b76c0641b8f642abcf6b1050dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404498"
---
# <a name="locktextedit-cell-protection-section"></a>Zelle "LockTextEdit" (Abschnitt "Protection")

Sperrt den Text eines Shapes, damit dieser nicht bearbeitet werden kann.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Text kann nicht bearbeitet werden.  <br/> |
| FALSE  <br/> | Text kann bearbeitet werden.  <br/> |
   
## <a name="remarks"></a>Hinweise

Sie können weiterhin Text formatieren, indem Sie eine Formatvorlage aus dem Dialogfeld **Text** anwenden (klicken Sie dazu auf der Registerkarte **Start** auf den Pfeil neben **Schriftart**). 
  
Um einen Verweis auf die Zelle LockTextEdit anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LockTextEdit  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die LockTextEdit-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLock** <br/> |
| Zellenindex:  <br/> |**visLockTextEdit** <br/> |
   

