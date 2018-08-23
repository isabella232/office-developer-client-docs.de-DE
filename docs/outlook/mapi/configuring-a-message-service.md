---
title: Konfigurieren eines Nachrichtendiensts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d68892e3-7c87-4b3a-a691-bff92f83ed00
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2b170037bc51a7848154c12acbfe700a0142ef8f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564108"
---
# <a name="configuring-a-message-service"></a>Konfigurieren eines Nachrichtendiensts

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
 **So konfigurieren Sie die-Dienstanbieter in einem Message-Dienst**
  
- Rufen Sie [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md). Wenn alle Daten für die Konfiguration notwendig sind programmgesteuert verfügbar, können Sie, ob eine Benutzeroberfläche angezeigt werden soll oder nicht. Wenn ein Teil der Informationen für einen oder mehrere Anbieter nicht verfügbar ist, stellen Sie jedoch sicher, dass Sie die Kennzeichen SERVICE_UI_ALLOWED oder SERVICE_UI_ALWAYS festgelegt. Unterdrücken eine Benutzeroberfläche beim erforderlichen Konfigurationsdaten nicht verfügbar Ergebnisse in einem Nachrichtendienst nicht konfiguriert ist.
    
 **So konfigurieren Sie einen einzelnen-Dienstanbieter in einem Message-Dienst**
  
1. Rufen Sie [IMAPISession::GetStatusTable](imapisession-getstatustable.md) Zugriff auf den Dienstanbieter Status-Objekt. 
    
2. Rufen Sie [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) , um den Dienstanbieter Eigenschaftenfenster anzuzeigen. 
    
Weitere Informationen zum Status Objekte verwenden finden Sie unter [Statustabelle und Status-Objekte](status-table-and-status-objects.md).
  

