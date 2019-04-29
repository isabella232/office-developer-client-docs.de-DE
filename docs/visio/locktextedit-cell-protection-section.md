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
   
## <a name="remarks"></a>Bemerkungen

Sie können weiterhin Text formatieren, indem Sie eine Formatvorlage aus dem Dialogfeld **Text** anwenden (klicken Sie dazu auf der Registerkarte **Start** auf den Pfeil neben **Schriftart**). 
  
Wenn Sie einen Verweis auf die Zelle Zelle LockTextEdit aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Zelle LockTextEdit  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle LockTextEdit aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLock** <br/> |
| Zellenindex:  <br/> |**visLockTextEdit** <br/> |
   

