---
title: Konfigurieren eines Nachrichtendiensts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: d68892e3-7c87-4b3a-a691-bff92f83ed00
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 97952952e48542d6d997285de6847791eefebb49
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571969"
---
# <a name="configuring-a-message-service"></a>Konfigurieren eines Nachrichtendiensts

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 **So konfigurieren Sie alle Dienstanbieter in einem Nachrichtendienst**
  
- Rufen [Sie IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)auf. Wenn alle für die Konfiguration erforderlichen Daten programmgesteuert verfügbar sind, können Sie auswählen, ob eine Benutzeroberfläche angezeigt werden soll. Wenn jedoch einige der Informationen für einen oder mehrere Anbieter nicht verfügbar sind, stellen Sie sicher, dass Sie das flag SERVICE_UI_ALLOWED oder SERVICE_UI_ALWAYS festlegen. Das Unterdrücken einer Benutzeroberfläche, wenn erforderliche Konfigurationsdaten nicht verfügbar sind, führt zu einem nicht konfigurierten Nachrichtendienst.
    
 **So konfigurieren Sie einen einzelnen Dienstanbieter in einem Nachrichtendienst**
  
1. Rufen Sie [IMAPISession::GetStatusTable](imapisession-getstatustable.md) auf, um auf das Statusobjekt des Dienstanbieters zuzugreifen. 
    
2. Rufen Sie [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) auf, um das Eigenschaftenblatt des Dienstanbieters anzuzeigen. 
    
Weitere Informationen zur Verwendung von Statusobjekten finden Sie unter [StatusTabelle und Statusobjekte.](status-table-and-status-objects.md)
  

