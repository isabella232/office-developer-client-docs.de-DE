---
title: Inhaltstabellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7b8efb4e-b5be-41b8-81bb-9aa1da421433
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 491381c771cae65e682acc8033b6558523847d3d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435586"
---
# <a name="contents-tables"></a>Inhaltstabellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Inhaltstabelle enthält Informationen zu Objekten in einem MAPI-Container. Adressbuchanbieter implementieren Inhaltstabellen für jeden container, und Nachrichtenspeicher- und Remotetransportanbieter implementieren Inhaltstabellen für ihre Ordner. Das Inhaltsverzeichnis eines Adressbuchcontainers listet Informationen zu den Nachrichtenbenutzer- und Verteilerlistenobjekten auf, während das Inhaltsverzeichnis eines Ordners Informationen zu seinen Nachrichten auflistet. Inhaltstabellen werden hauptsächlich von Clientanwendungen verwendet. 
  
Es gibt zwei Arten von Ordnerinhaltstabellen:
  
- Standardinhaltstabellen enthalten Standardnachrichten – Nachrichten, die übertragen und für einen Benutzer sichtbar gemacht werden können. 
    
- Verknüpfte Inhaltstabellen enthalten ausgeblendete, nicht durchsetzbare Informationen, die von einem Client für einen bestimmten Zweck erstellt wurden, z. B. zum Speichern einer alternativen Darstellung einer Standardnachricht. Zugeordnete Informationen werden erstellt, indem das MAPI_ASSOCIATED an den [IMAPIFolder::CreateMessage-Aufruf übergeben](imapifolder-createmessage.md) wird. 
    
Die Inhaltstabellen der meisten Adressbuchcontainer und vieler Ordner unterstützen keine kategorisierte Sortierung. 
  
Auf eine Inhaltstabelle kann über folgenden Aufruf zugegriffen werden:
  
- [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).
    
    - Oder -
    
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md) mit **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) oder **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) (nur Ordner), die als Eigenschaftstag und IID_IMAPITable als Schnittstellenbezeichner angegeben sind.
    
Nachrichtenspeicher- und Adressbuchanbieter müssen beide Techniken zum Abrufen von Tabelleneigenschaften unterstützen. Es ist nicht hinnehmbar, dass Anbieter nur eine Möglichkeit für den Zugriff auf diese Tabellen unterstützen, da Clients erwarten, dass sie die Wahl haben. 
  
 **GetContentsTable** akzeptiert als Eingabe mehrere Flags, die Einstellungen angeben. Wenn festgelegt, ruft MAPI_ASSOCIATED-Flag eine zugeordnete Inhaltstabelle ab. Da einige Ordner zugeordnete Inhalte nicht unterstützen und Clients dies nicht im Voraus ermitteln können, gibt **GetContentsTable** manchmal den Fehler MAPI_E_NO_SUPPORT, wenn eine zugeordnete Inhaltstabelle angefordert wird. 
  
Das MAPI_DEFERRED_ERRORS gibt dem Implementier der Tabelle an, dass fehler, die während des Aufrufs auftreten, erst zu einem späteren Zeitpunkt gemeldet werden müssen. 
  
Der Aufruf von **IMAPIProp::OpenProperty** umfasst den Zugriff auf eine Inhaltstabelle durch Öffnen der entsprechenden Eigenschaft,  **PR_CONTAINER_CONTENTS** für Adressbuchinhaltstabellen und Standardordnerinhaltstabellen und PR_FOLDER_ASSOCIATED_CONTENTS für zugeordnete Inhaltstabellen. Obwohl keine oder diese Eigenschaften über die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) eines Ordners oder Containers abgerufen werden können, sind sie im Eigenschaftentagarray enthalten, das von der [IMAPIProp::GetPropList-Methode](imapiprop-getproplist.md) zurückgegeben wird. 
  
 **PR_CONTAINER_CONTENTS** kann auch zum Ein- oder Ausschließen einer Inhaltstabelle aus einem Kopiervorgang verwendet werden. Wenn ein Client PR_CONTAINER_CONTENTS im *lpExcludeProps-Parameter* für **IMAPIProp::CopyTo** in einem Kopiervorgang angibt, unterstützt der neue Ordner oder Container das Inhaltsverzeichnis des ursprünglichen **Ordners** oder Containers nicht. 
  
Adressbuchcontainer- und Ordnerinhaltstabellen verfügen über eine lange Liste der erforderlichen Spalten – Spalten, die Clients erwarten können, nachdem sie die Tabelle aus **GetContentsTable** oder **OpenProperty abgerufen haben.** Anbieter können diesen erforderlichen Satz bei Bedarf hinzufügen, und Clients können über die **SetColumns-Methode** auch Änderungen anfordern. 
  
Die erforderlichen Spalten für die einzelnen Inhaltstabellentypen sind:
  
|**Erforderliche Spalte**|**Inhaltsverzeichnistyp**|
|:-----|:-----|
|**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |Adressbuchcontainertabellen  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Adressbuchcontainertabellen  <br/> |
|**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> |Tabellen des Nachrichtenspeicherordners  <br/> |
|**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |Alle Ordnerinhaltstabellen  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Adressbuchcontainertabellen  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Alle Inhaltstabellen  <br/> |
|**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))  <br/> |Alle Ordnerinhaltstabellen  <br/> |
|**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |Alle Inhaltstabellen  <br/> |
|**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |Tabellen des Nachrichtenspeicherordners  <br/> |
|**PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md))  <br/> |Tabellen des Nachrichtenspeicherordners  <br/> |
|**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |Alle Ordnerinhaltstabellen  <br/> |
|**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |Tabellen für Remote-Transport-Ordner  <br/> |
|**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |Alle Ordnerinhaltstabellen  <br/> |
|**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |Alle Ordnerinhaltstabellen  <br/> |
|**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))  <br/> |Alle Ordnerinhaltstabellen  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Alle Inhaltstabellen  <br/> |
|**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))  <br/> |Tabellen des Nachrichtenspeicherordners  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Adressbuchcontainer- und Nachrichtenspeicherordnertabellen  <br/> |
|**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |Tabellen für Remote-Transport-Ordner  <br/> |
|**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |Tabellen des Nachrichtenspeicherordners  <br/> |
|**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |Tabellen des Nachrichtenspeicherordners  <br/> |
   
Die für jede Zeile verfügbare Eintrags-ID kann je nach Tabellenimplementierung eine kurz- oder langfristige Eintrags-ID sein. Kurzfristige Eintragsbezeichner werden in der Regel in Situationen verwendet, in denen die Leistung ein Problem ist. Jeder Eintragsbezeichnertyp kann für den Zugriff auf das entsprechende Objekt verwendet werden. 
  
Inhaltstabellen verfügen auch über eine Reihe von Spalten, die optional sind, aber häufig von Dienstanbietern in ihren Implementierungen enthalten sind. Diese optionalen Spalten sind:
  
|**Optionale Spalte**|**Inhaltsverzeichnistyp**|
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |Tabellen des Nachrichtenspeicherordners  <br/> |
|**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> |Standardordnerinhaltstabellen  <br/> |
|**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))  <br/> |Standardordnerinhaltstabellen  <br/> |
|**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))  <br/> |Tabellen des Nachrichtenspeicherordners  <br/> |
|**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |Adressbuchcontainertabellen  <br/> |
|**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))  <br/> |Alle Ordnerinhaltstabellen  <br/> |
|**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |Alle Ordnerinhaltstabellen  <br/> |
|**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))  <br/> |Alle Ordnerinhaltstabellen  <br/> |
|**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |Alle Ordnerinhaltstabellen  <br/> |
|**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |Adressbuchcontainertabellen  <br/> |
|**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md))  <br/> |Adressbuchcontainertabellen  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |Alle Ordnerinhaltstabellen  <br/> |
|**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))  <br/> |Alle Ordnerinhaltstabellen  <br/> |
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |Alle Ordnerinhaltstabellen  <br/> |
|**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))  <br/> |Adressbuchcontainertabellen  <br/> |
   
Nachrichtenspeicheranbieter müssen auch **PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) nur für Inhaltstabellen für Suchergebnisordner enthalten.
  
Benannte Eigenschaften können dem Spaltensatz einer Ordnerinhaltstabelle nur hinzugefügt werden, wenn alle Nachrichten im Ordner dieselbe Zuordnungssignatur aufweisen, d. h. die gleiche Zuordnung von Eigenschaftennamen zu Eigenschaftenbezeichnern. Ordnerinhaltstabellen sollten das Hinzufügen von nachrichtenklassenspezifischen Eigenschaften zum Spaltensatz unterstützen, wenn sie die Erstellung beliebiger Nachrichten im Ordner unterstützen.
  
Clients können die Standardsortierreihenfolge für eine Ordnerinhaltstabelle speichern, indem sie die [IMAPIFolder::SaveContentsSort-Methode](imapifolder-savecontentssort.md) aufrufen. Wenn das RECURSIVE_SORT für den Anruf angegeben ist, kann die Sortierreihenfolge für alle Unterordner innerhalb des Ordners angewendet werden. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

