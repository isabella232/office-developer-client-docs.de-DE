---
title: Zelle "LockCustProp" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60055
ms.localizationpriority: medium
ms.assetid: d1c23f1d-485d-a897-594d-15d6e8d0fb3c
description: Bestimmt, ob der Benutzer im Dialogfeld Shape-Daten definieren oder im Kontextmenü für das Fenster Shape-Daten Shape-Daten auf der Benutzeroberfläche hinzufügen, löschen oder ändern darf.
ms.openlocfilehash: bf8730523b007f8d7e0f4b936d94c8779d160a63
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603634"
---
# <a name="lockcustprop-cell-protection-section"></a>Zelle "LockCustProp" (Abschnitt "Protection")

Bestimmt, ob der Benutzer im Dialogfeld **Shape-Daten definieren** oder im Kontextmenü für das Fenster **Shape-Daten** Shape-Daten auf der Benutzeroberfläche hinzufügen, löschen oder ändern darf. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Der Befehl **Shape-Daten definieren** im Kontextmenü des Fensters **Shape-Daten** ist deaktiviert.  <br/> |
|FALSE  <br/> |Der Befehl **Shape-Daten definieren** im Kontextmenü des Fensters **Shape-Daten** ist aktiviert (Standardeinstellung).  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Der Wert TRUE verhindert nicht, dass der Wert eines Shape-Datenelements oder der Abschnitt Shape Data im ShapeSheet-Fenster geändert werden kann. 
  
Verwenden Sie zum Abrufen eines Verweises auf die Zelle "LockCustProp" anhand des Namens einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |LockCustProp  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle LockCustProp anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowLock** <br/> |
|Zellenindex:  <br/> |**visLockCustProp** <br/> |
   

