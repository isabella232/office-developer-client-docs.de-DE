---
title: Zelle "LockCustProp" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60055
localization_priority: Normal
ms.assetid: d1c23f1d-485d-a897-594d-15d6e8d0fb3c
description: Bestimmt, ob der Benutzer im Dialogfeld Shape-Daten definieren oder im Kontextmenü für das Fenster Shape-Daten Shape-Daten auf der Benutzeroberfläche hinzufügen, löschen oder ändern darf.
ms.openlocfilehash: 001123f3bd08d35f6f8e4874e20f2ee073835494
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422523"
---
# <a name="lockcustprop-cell-protection-section"></a>Zelle "LockCustProp" (Abschnitt "Protection")

Bestimmt, ob der Benutzer im Dialogfeld **Shape-Daten definieren** oder im Kontextmenü für das Fenster **Shape-Daten** Shape-Daten auf der Benutzeroberfläche hinzufügen, löschen oder ändern darf. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Der Befehl **Shape-Daten definieren** im Kontextmenü des Fensters **Shape-Daten** ist deaktiviert.  <br/> |
|FALSE  <br/> |Der Befehl **Shape-Daten definieren** im Kontextmenü des Fensters **Shape-Daten** ist aktiviert (Standardeinstellung).  <br/> |
   
## <a name="remarks"></a>Hinweise

Der Wert TRUE verhindert nicht, dass der Wert eines Shape-Datenelements oder der Abschnitt Shape Data im ShapeSheet-Fenster geändert werden kann. 
  
Verwenden Sie zum Erhalten eines Verweises auf die Zelle LockCustProp anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |LockCustProp  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die LockCustProp-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowLock** <br/> |
|Zellenindex:  <br/> |**visLockCustProp** <br/> |
   

