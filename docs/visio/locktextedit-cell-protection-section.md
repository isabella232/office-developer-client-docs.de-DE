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
ms.openlocfilehash: 7f8800f0b260e808a46ec123d27784f3dd92e847
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797399"
---
# <a name="locktextedit-cell-protection-section"></a>Zelle "LockTextEdit" (Abschnitt "Protection")

Sperrt den Text eines Shapes, damit dieser nicht bearbeitet werden kann.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Text kann nicht bearbeitet werden.  <br/> |
| FALSE  <br/> | Text kann bearbeitet werden.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können weiterhin Text formatieren, indem Sie eine Formatvorlage im Dialogfeld **Text** anwenden (klicken Sie auf der Registerkarte **Start** auf den Pfeil neben **Schriftart** ). 
  
Wenn Sie einen Verweis auf die Zelle LockTextEdit nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LockTextEdit  <br/> |
   
Wenn Sie einen Verweis auf die Zelle LockTextEdit aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLock** <br/> |
| Zellenindex:  <br/> |**visLockTextEdit** <br/> |
   

