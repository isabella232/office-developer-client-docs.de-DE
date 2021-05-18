---
title: Neukonfigurieren eines Transportanbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d466bde-b70d-44b6-ba03-6ad8353ec759
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b35ca2bb52439cf2ba1750c6fad2883730c4c3f8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408410"
---
# <a name="reconfiguring-a-transport-provider"></a>Neukonfigurieren eines Transportanbieters

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Sie können das Statusobjekt eines Transportanbieters verwenden, um einige der Eigenschaften des Anbieters zu ändern. Der Bereich der Eigenschaften, die geändert werden können, hängt von den Eigenschaften ab, die im Eigenschaftenblatt des Anbieters enthalten sind und wie diese Eigenschaften definiert werden. 
  
 **So konfigurieren Sie einen aktiven Transportanbieter neu**
  
1. Rufen [Sie IMAPISession::GetStatusTable auf,](imapisession-getstatustable.md) um auf die Statustabelle zu zugreifen. 
    
2. Suchen Sie die Zeile für den Transportanbieter, der neu konfiguriert werden soll, indem Sie eine Eigenschaftseinschränkung erstellen, die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) mit dem Namen des Zielanbieters entspricht. 
    
3. Rufen [Sie IMAPITable::FindRow auf,](imapitable-findrow.md) um die entsprechende Zeile abzurufen. 
    
4. Überprüfen Sie, ob STATUS_SETTINGS_DIALOG und STATUS_VALIDATE_STATE in der eigenschaft **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) des Zieltransportanbieters festgelegt sind. Wenn STATUS_SETTINGS_DIALOG nicht festgelegt ist, zeigt der Transportanbieter kein Konfigurationseigenschaftsblatt an. Wenn STATUS_VALIDATE_STATE nicht festgelegt ist, können Sie keine dynamische Neukonfiguration durchführen.
    
5. Wenn STATUS_SETTINGS_DIALOG festgelegt ist, rufen Sie [IMAPIStatus::SettingsDialog auf,](imapistatus-settingsdialog.md) um das Eigenschaftenblatt des Transportanbieters anzeigen und dem Benutzer das Vornehmen von Änderungen zu ermöglichen. 
    
6. Nachdem der Benutzer die Neukonfiguration abgeschlossen hat, rufen Sie [IMAPIStatus::ValidateState](imapistatus-validatestate.md) auf, wenn STATUS_VALIDATE_STATE festgelegt ist, und übergeben CONFIG_CHANGED. 
    

