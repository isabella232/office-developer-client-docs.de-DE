---
title: Neukonfiguration eines Transportanbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 3d466bde-b70d-44b6-ba03-6ad8353ec759
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: af5479c5116637f36a14b1157f21e648ed83d474
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599144"
---
# <a name="reconfiguring-a-transport-provider"></a>Neukonfiguration eines Transportanbieters

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Sie können das Statusobjekt eines Transportanbieters verwenden, um einige eigenschaften des Anbieters zu ändern. Der Eigenschaftenbereich, der geändert werden kann, hängt von den Eigenschaften ab, die im Eigenschaftenfenster des Anbieters enthalten sind, und von der Definition dieser Eigenschaften. 
  
 **So konfigurieren Sie einen aktiven Transportanbieter neu**
  
1. Rufen Sie [IMAPISession::GetStatusTable](imapisession-getstatustable.md) auf, um auf die Statustabelle zuzugreifen. 
    
2. Suchen Sie die Zeile für den neu zu konfigurierenden Transportanbieter, indem Sie eine Eigenschaftseinschränkung erstellen, die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) mit dem Namen des Zielanbieters übereinstimmt. 
    
3. Rufen Sie [IMAPITable::FindRow](imapitable-findrow.md) auf, um die entsprechende Zeile abzurufen. 
    
4. Überprüfen Sie, ob die Flags STATUS_SETTINGS_DIALOG und STATUS_VALIDATE_STATE in der **Eigenschaft PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) des Zieltransportanbieters festgelegt sind. Wenn STATUS_SETTINGS_DIALOG nicht festgelegt ist, zeigt der Transportanbieter kein Konfigurationseigenschaftenblatt an. Wenn STATUS_VALIDATE_STATE nicht festgelegt ist, können Sie keine dynamische Neukonfiguration ausführen.
    
5. Wenn STATUS_SETTINGS_DIALOG festgelegt ist, rufen Sie [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) auf, um das Eigenschaftenblatt des Transportanbieters anzuzeigen und dem Benutzer das Vornehmen von Änderungen zu ermöglichen. 
    
6. Nachdem der Benutzer die Neukonfiguration abgeschlossen hat, rufen Sie [IMAPIStatus::ValidateState](imapistatus-validatestate.md) auf, wenn STATUS_VALIDATE_STATE festgelegt ist, und übergeben sie CONFIG_CHANGED. 
    

