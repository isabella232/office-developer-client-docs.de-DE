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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359606"
---
# <a name="lockcustprop-cell-protection-section"></a>Zelle "LockCustProp" (Abschnitt "Protection")

Bestimmt, ob der Benutzer im Dialogfeld **Shape-Daten definieren** oder im Kontextmenü für das Fenster **Shape-Daten** Shape-Daten auf der Benutzeroberfläche hinzufügen, löschen oder ändern darf. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Der Befehl **Shape-Daten definieren** im Kontextmenü des Fensters **Shape-Daten** ist deaktiviert.  <br/> |
|FALSE  <br/> |Der Befehl **Shape-Daten definieren** im Kontextmenü des Fensters **Shape-Daten** ist aktiviert (Standardeinstellung).  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Wert TRUE verhindert nicht, dass der Wert eines Shape-Datenelements oder der Abschnitt Shape Data im ShapeSheet-Fenster geändert werden kann. 
  
Wenn Sie einen Verweis auf die Zelle Zelle LockCustProp aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Zelle LockCustProp  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle LockCustProp aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowLock** <br/> |
|Zellenindex:  <br/> |**visLockCustProp** <br/> |
   

