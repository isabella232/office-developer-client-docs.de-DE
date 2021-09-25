---
title: Nachrichtendiensttabellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: b93ab837-3918-4427-b013-bedc6f5276e4
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ab9bfeca1e86bc8017bd091071a36f968b6dfa34
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551107"
---
# <a name="message-service-tables"></a>Nachrichtendiensttabellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Nachrichtendiensttabelle enthält Informationen zu den Nachrichtendiensten im aktuellen Profil. Es gibt eine Nachrichtendiensttabelle für jede MAPI-Sitzung, die von der MAPI implementiert und von speziellen Clientanwendungen verwendet wird, die Konfigurationsunterstützung bereitstellen. 
  
Die Nachrichtendiensttabelle ist eine statische Tabelle.
  
Clients greifen auf die Nachrichtendiensttabelle zu, indem sie die [IMsgServiceAdmin::GetMsgServiceTable-Methode](imsgserviceadmin-getmsgservicetable.md) aufrufen. 
  
Die folgenden Eigenschaften bilden die erforderliche Spalte, die in der Nachrichtendiensttabelle festgelegt ist:
  
|||
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))  <br/> |
|**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md))  <br/> |**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))  <br/> |
|**PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md))  <br/> |**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))  <br/> |
   
 **PR_DISPLAY_NAME** ist der anzeigebare Name für den Nachrichtendienst und die Standardmäßige Sortierschlüsselspalte. 
  
 **PR_INSTANCE_KEY** dient als Indexspalte für die Tabelle und identifiziert eine Zeile eindeutig. 
  
 **PR_RESOURCE_FLAGS** beschreibt die Funktionen des Nachrichtendiensts. 
  
 **PR_SERVICE_DLL_NAME** ist der Name der DLL, die die Implementierung des Nachrichtendiensts enthält. 
  
 **PR_SERVICE_ENTRY_NAME** ist der Name der Einstiegspunktfunktion des Nachrichtendiensts, die dem [MSGSERVICEENTRY-Prototyp](msgserviceentry.md) entspricht. 
  
 **PR_SERVICE_NAME** ist ein erforderlicher Eintrag im Abschnitt **[Dienste]** in MAPISVC.INF. Der Wert für diese Eigenschaft wird nie geändert oder lokalisiert. **PR_SERVICE_NAME** können verwendet werden, um den Nachrichtendienst programmgesteuert zu identifizieren. 
  
 **PR_SERVICE_SUPPORT_FILES** ist eine Liste der Dateien, die mit dem Nachrichtendienst installiert werden müssen. 
  
 **PR_SERVICE_UID** ist ein eindeutiger Bezeichner für den Nachrichtendienst. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

