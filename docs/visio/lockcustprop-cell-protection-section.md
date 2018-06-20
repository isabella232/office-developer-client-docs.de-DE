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
description: Bestimmt, ob der Benutzer hinzufügen, löschen oder Ändern von Shape-Daten in der Benutzeroberfläche (UI) über das Dialogfeld Shape-Daten definieren oder im Kontextmenü für das Fenster Shape-Daten kann.
ms.openlocfilehash: a88da9e4973f819b398b5bdeda434ede14640797
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797375"
---
# <a name="lockcustprop-cell-protection-section"></a>Zelle "LockCustProp" (Abschnitt "Protection")

Bestimmt, ob der Benutzer hinzufügen, löschen oder Ändern von Shape-Daten in der Benutzeroberfläche (UI) über das Dialogfeld **Shape-Daten definieren** oder im Kontextmenü für das Fenster **Shape-Daten** kann. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Der Befehl **Shape-Daten definieren** im Kontextmenü im Fenster **Shape-Daten** ist deaktiviert.  <br/> |
|FALSE  <br/> |Der Befehl **Shape-Daten definieren** im Kontextmenü im Fenster **Shape-Daten** ist aktiviert (Standardeinstellung).  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Wert TRUE verhindert nicht, dass der Wert eines Shape-Datenelements oder der Abschnitt Shape Data im ShapeSheet-Fenster geändert werden kann. 
  
Wenn Sie einen Verweis auf die Zelle LockCustProp nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |LockCustProp  <br/> |
   
Wenn Sie einen Verweis auf die Zelle LockCustProp aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowLock** <br/> |
|Zellenindex:  <br/> |**visLockCustProp** <br/> |
   

