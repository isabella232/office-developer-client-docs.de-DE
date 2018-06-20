---
title: Nachricht Servicetabellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b93ab837-3918-4427-b013-bedc6f5276e4
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 81772115fcd4f081718dd560759f6ab93dc7c11c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793275"
---
# <a name="message-service-tables"></a>Nachricht Servicetabellen

  
  
**Betrifft**: Outlook 
  
Die Nachricht Service-Tabelle enthält Informationen zu den Diensten Nachricht im aktuellen Profil. Es wird eine Meldung-Service-Tabelle für jede MAPI-Sitzung, MAPI Implementierung und Verwendung von speziellen-Clientanwendungen, die Konfiguration unterstützen. 
  
Die Nachricht Service-Tabelle ist eine statische Tabelle.
  
Clientzugriff durch Aufrufen der Methode [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) die Tabelle der Dienste. 
  
Die folgenden Eigenschaften bilden die erforderliche Spalte in der Tabelle der Dienste festgelegt:
  
|||
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))  <br/> |
|**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md))  <br/> |**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))  <br/> |
|**PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md))  <br/> |**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))  <br/> |
   
 **PR_DISPLAY_NAME** ist der Anzeigename für den Dienst und die Schlüsselspalte der standardmäßigen sortieren. 
  
 **PR_INSTANCE_KEY** dient als Index-Spalte für die Tabelle, die eine Zeile eindeutig identifiziert. 
  
 **PR_RESOURCE_FLAGS** wird die Nachricht Service-Funktionen beschrieben. 
  
 **PR_SERVICE_DLL_NAME** ist der Name der DLL, die die Implementierung der Service Nachricht enthält. 
  
 **PR_SERVICE_ENTRY_NAME** ist der Name der Messagingdiensts Eintrag Point-Funktion, die den [MSGSERVICEENTRY](msgserviceentry.md) Prototyp entspricht. 
  
 **PR_SERVICE_NAME** ist eine erforderliche Eintrag im Abschnitt **[Services]** in MAPISVC.INF. Der Wert für diese Eigenschaft wird nie geändert oder lokalisiert werden. **PR_SERVICE_NAME** kann verwendet werden, um den Dienst programmgesteuert zu identifizieren. 
  
 **PR_SERVICE_SUPPORT_FILES** ist eine Liste von Dateien, die mit dem Nachrichtendienst installiert werden muss. 
  
 **PR_SERVICE_UID** ist ein eindeutiger Bezeichner für den Dienst. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

