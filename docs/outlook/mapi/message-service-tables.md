---
title: Nachrichtendiensttabellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b93ab837-3918-4427-b013-bedc6f5276e4
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c644e89511033234aa45c5f82738e4c471ef646d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422495"
---
# <a name="message-service-tables"></a>Nachrichtendiensttabellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Nachrichtendiensttabelle enthält Informationen zu den Nachrichtendiensten im aktuellen Profil. Es gibt eine Nachrichtendiensttabelle für jede MAPI-Sitzung, die von MAPI implementiert und von speziellen Clientanwendungen verwendet wird, die Konfigurationsunterstützung bereitstellen. 
  
Die Nachrichtendiensttabelle ist eine statische Tabelle.
  
Clients greifen auf die Nachrichtendiensttabelle zu, indem sie die [IMsgServiceAdmin::GetMsgServiceTable-Methode](imsgserviceadmin-getmsgservicetable.md) aufrufen. 
  
Die folgenden Eigenschaften stellen die erforderliche Spalte in der Nachrichtendiensttabelle zusammen:
  
|||
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))  <br/> |
|**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md))  <br/> |**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))  <br/> |
|**PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md))  <br/> |**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))  <br/> |
   
 **PR_DISPLAY_NAME** ist der anzeigebare Name für den Nachrichtendienst und die Standardspalte des Sortierschlüssels. 
  
 **PR_INSTANCE_KEY** dient als Indexspalte für die Tabelle, die eine Zeile eindeutig identifiziert. 
  
 **PR_RESOURCE_FLAGS** beschreibt die Funktionen des Nachrichtendiensts. 
  
 **PR_SERVICE_DLL_NAME** ist der Name der DLL, die die Nachrichtendienstimplementierung enthält. 
  
 **PR_SERVICE_ENTRY_NAME** ist der Name der Einstiegspunktfunktion des Nachrichtendiensts, die dem [MSGSERVICEENTRY-Prototyp entspricht.](msgserviceentry.md) 
  
 **PR_SERVICE_NAME** ist ein erforderlicher Eintrag im **Abschnitt [Dienste]** in MAPISVC.INF. Der Wert für diese Eigenschaft wird nie geändert oder lokalisiert. **PR_SERVICE_NAME** kann zum programmgesteuerten Identifizieren des Nachrichtendiensts verwendet werden. 
  
 **PR_SERVICE_SUPPORT_FILES** ist eine Liste der Dateien, die mit dem Nachrichtendienst installiert werden müssen. 
  
 **PR_SERVICE_UID** ist ein eindeutiger Bezeichner für den Nachrichtendienst. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

