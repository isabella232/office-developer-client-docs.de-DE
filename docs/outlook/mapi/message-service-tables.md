---
title: Nachrichtendienst Tabellen
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
# <a name="message-service-tables"></a>Nachrichtendienst Tabellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Nachrichtendienst Tabelle enthält Informationen zu den Nachrichtendiensten im aktuellen Profil. Es gibt eine Nachrichtendienst Tabelle für jede MAPI-Sitzung, die von MAPI implementiert und von speziellen Clientanwendungen verwendet wird, die Konfigurationsunterstützung bereitstellen. 
  
Die Nachrichtendienst Tabelle ist eine statische Tabelle.
  
Clients greifen auf die Nachrichtendienst Tabelle zu, indem Sie die [IMsgServiceAdmin:: GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) -Methode aufrufen. 
  
Die folgenden Eigenschaften stellen den erforderlichen Spaltensatz in der Nachrichtendienst Tabelle dar:
  
|||
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([Pidtaginstancekey (](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS** ([Pidtagresourceflags (](pidtagresourceflags-canonical-property.md))  <br/> |**PR_SERVICE_DLL_NAME** ([Pidtagservicedllname (](pidtagservicedllname-canonical-property.md))  <br/> |
|**PR_SERVICE_ENTRY_NAME** ([Pidtagserviceentryname (](pidtagserviceentryname-canonical-property.md))  <br/> |**PR_SERVICE_NAME** ([Pidtagservicename (](pidtagservicename-canonical-property.md))  <br/> |
|**PR_SERVICE_SUPPORT_FILES** ([Pidtagservicesupportfiles (](pidtagservicesupportfiles-canonical-property.md))  <br/> |**PR_SERVICE_UID** ([Pidtagserviceuid (](pidtagserviceuid-canonical-property.md))  <br/> |
   
 **PR_DISPLAY_NAME** ist der Anzeige Name für den Nachrichtendienst und die standardmäßige Sortierschlüsselspalte. 
  
 **PR_INSTANCE_KEY** dient als Indexspalte für die Tabelle, um eine Zeile eindeutig zu identifizieren. 
  
 **PR_RESOURCE_FLAGS** beschreibt die Funktionen des Nachrichtendiensts. 
  
 **PR_SERVICE_DLL_NAME** ist der Name der dll, die die Implementierung des Nachrichtendiensts enthält. 
  
 **PR_SERVICE_ENTRY_NAME** ist der Name der Einstiegspunktfunktion des Nachrichtendiensts, die dem [MSGSERVICEENTRY](msgserviceentry.md) -Prototyp entspricht. 
  
 **PR_SERVICE_NAME** ist ein erforderlicher Eintrag im Abschnitt **[Dienste]** in MAPISVC. inf. Der Wert für diese Eigenschaft wird nie geändert oder lokalisiert. **PR_SERVICE_NAME** kann zum programmgesteuerten Identifizieren des Nachrichtendiensts verwendet werden. 
  
 **PR_SERVICE_SUPPORT_FILES** ist eine Liste der Dateien, die mit dem Nachrichtendienst installiert werden müssen. 
  
 **PR_SERVICE_UID** ist ein eindeutiger Bezeichner für den Nachrichtendienst. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

