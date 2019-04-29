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
ms.openlocfilehash: 4c3d30c7111e7b26886cbfb069ec2822d2ee0234
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434508"
---
# <a name="configuring-a-message-service"></a>Konfigurieren eines Nachrichtendiensts

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 **So konfigurieren Sie alle Dienstanbieter in einem Nachrichtendienst**
  
- Rufen Sie [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)auf. Wenn alle für die Konfiguration erforderlichen Daten programmgesteuert verfügbar sind, können Sie auswählen, ob eine Benutzeroberfläche angezeigt werden soll. Wenn jedoch einige der Informationen für einen oder mehrere Anbieter nicht verfügbar sind, stellen Sie sicher, dass Sie das SERVICE_UI_ALLOWED-oder SERVICE_UI_ALWAYS-Flag festgelegt haben. Das unterdrücken einer Benutzeroberfläche, wenn erforderliche Konfigurationsdaten nicht verfügbar sind, führt zu einem nicht konfigurierten Nachrichtendienst.
    
 **So konfigurieren Sie einen einzelnen Dienstanbieter in einem Nachrichtendienst**
  
1. Rufen Sie [IMAPISession::](imapisession-getstatustable.md) getstatusable auf, um auf das Statusobjekt des Dienstanbieters zuzugreifen. 
    
2. Rufen Sie [IMAPIStatus:: Settingsdialog](imapistatus-settingsdialog.md) auf, um das Eigenschaftenfenster des Dienstanbieters anzuzeigen. 
    
Weitere Informationen zur Verwendung von Status-Objekten finden Sie unter [Status Table-und Status-Objekte](status-table-and-status-objects.md).
  

