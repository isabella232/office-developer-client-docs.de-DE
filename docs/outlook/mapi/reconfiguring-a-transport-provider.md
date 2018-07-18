---
title: Neukonfigurieren eines Transportanbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d466bde-b70d-44b6-ba03-6ad8353ec759
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ec5a431d04799e3f19c23dd0437aeac13fbf0968
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795351"
---
# <a name="reconfiguring-a-transport-provider"></a>Neukonfigurieren eines Transportanbieters

  
  
**Betrifft**: Outlook 
  
Status-Objekt eines Transportdienstes können Sie einige der Eigenschaften des Anbieters ändern. Bereich von Eigenschaften, die geändert werden kann, hängt von der Eigenschaften, die mit dem Anbieter Eigenschaftenfenster und wie diese Eigenschaften definiert sind, enthalten sind. 
  
 **So konfigurieren Sie eine aktive Transportdienst neu**
  
1. Rufen Sie [IMAPISession::GetStatusTable](imapisession-getstatustable.md) Zugriff auf die Statustabelle. 
    
2. Suchen Sie die Zeile für den Transportdienst neu konfiguriert werden, indem Sie eine eigenschaftseinschränkung, die entspricht **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) erstellen, mit dem Namen des Zielanbieters. 
    
3. Rufen Sie [IMAPITable](imapitable-findrow.md) zum Abrufen der entsprechenden Zeile. 
    
4. Überprüfen Sie, dass die Flags STATUS_SETTINGS_DIALOG und STATUS_VALIDATE_STATE in der Adressbuchhierarchie Ziel **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))-Eigenschaft festgelegt werden. Wenn STATUS_SETTINGS_DIALOG nicht festgelegt ist, wird der Adressbuchhierarchie ein Eigenschaftenblatts Konfiguration nicht angezeigt. Wenn STATUS_VALIDATE_STATE nicht festgelegt ist, nicht Dr möglich.
    
5. Wenn STATUS_SETTINGS_DIALOG festgelegt ist, rufen Sie [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) zum Anzeigen der Adressbuchhierarchie Eigenschaftenfenster und ermöglicht es dem Benutzer, um Änderungen vorzunehmen. 
    
6. Nachdem der Benutzer mit der Neukonfiguration abgeschlossen wurde, rufen Sie [IMAPIStatus::ValidateState](imapistatus-validatestate.md) Wenn STATUS_VALIDATE_STATE übergeben CONFIG_CHANGED festgelegt ist. 
    

