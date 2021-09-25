---
title: Inhaltstabellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 7b8efb4e-b5be-41b8-81bb-9aa1da421433
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8114190a263ffbcc72344cd3a051a427238ecb0f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556826"
---
# <a name="contents-tables"></a>Inhaltstabellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Inhaltsverzeichnis enthält Informationen zu Objekten in einem MAPI-Container. Adressbuchanbieter implementieren Inhaltstabellen für jeden container, und Nachrichtenspeicher und Remote-Transportanbieter implementieren Inhaltstabellen für ihre Ordner. Das Inhaltsverzeichnis eines Adressbuchcontainers listet Informationen zu seinen Nachrichtenbenutzer- und Verteilerlistenobjekten auf, während im Inhaltsverzeichnis eines Ordners Informationen zu seinen Nachrichten aufgeführt sind. Inhaltstabellen werden in erster Linie von Clientanwendungen verwendet. 
  
Es gibt zwei Typen von Ordnerinhaltstabellen:
  
- Standardinhaltsverzeichnisse enthalten Standardnachrichten – Nachrichten, die übertragen und für einen Benutzer sichtbar gemacht werden können. 
    
- Zugeordnete Inhaltsverzeichnisse enthalten ausgeblendete, nicht übertragbare Informationen, die von einem Client für einen bestimmten Zweck erstellt werden, z. B. zum Speichern einer alternativen Darstellung einer Standardnachricht. Zugeordnete Informationen werden erstellt, indem das MAPI_ASSOCIATED-Flag an den [IMAPIFolder::CreateMessage-Aufruf](imapifolder-createmessage.md) übergeben wird. 
    
Die Inhaltsverzeichnisse der meisten Adressbuchcontainer und viele Ordner unterstützen keine kategorisierte Sortierung. 
  
Auf ein Inhaltsverzeichnis kann durch Aufrufen von Folgendem zugegriffen werden:
  
- [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).
    
    - Oder -
    
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md) with **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) or **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) (folders only) specified as the property tag and IID_IMAPITable as the interface identifier.
    
Nachrichtenspeicher- und Adressbuchanbieter müssen beide Techniken zum Abrufen von Tabelleneigenschaften unterstützen. Es ist inakzeptabel, dass Anbieter nur eine Möglichkeit für den Zugriff auf diese Tabellen unterstützen, da Clients davon ausgehen, dass sie die Wahl haben. 
  
 **GetContentsTable** akzeptiert als Eingabe mehrere Flags, die Einstellungen angeben. Bei Festlegung ruft das flag MAPI_ASSOCIATED ein zugeordnetes Inhaltsverzeichnis ab. Da einige Ordner zugeordnete Inhalte nicht unterstützen und Clients dies nicht im Voraus ermitteln können, gibt **GetContentsTable** manchmal den Fehler MAPI_E_NO_SUPPORT zurück, wenn ein zugeordnetes Inhaltsverzeichnis angefordert wird. 
  
Das flag MAPI_DEFERRED_ERRORS gibt dem Implementierer der Tabelle an, dass während des Aufrufs aufgetretene Fehler erst zu einem späteren Zeitpunkt gemeldet werden müssen. 
  
Der Aufruf von **IMAPIProp::OpenProperty** umfasst den Zugriff auf ein Inhaltsverzeichnis durch Öffnen der entsprechenden Eigenschaft, **PR_CONTAINER_CONTENTS** für Adressbuchinhaltsverzeichnisse und Standardordnerinhaltstabellen und **PR_FOLDER_ASSOCIATED_CONTENTS** für zugeordnete Inhaltstabellen. Obwohl keine oder diese Eigenschaften über die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) eines Ordners oder Containers abgerufen werden können, sind sie im Eigenschaftentagarray enthalten, das von der [IMAPIProp::GetPropList-Methode](imapiprop-getproplist.md) zurückgegeben wird. 
  
 **PR_CONTAINER_CONTENTS** können auch verwendet werden, um ein Inhaltsverzeichnis in einen Kopiervorgang einzuschließen oder auszuschließen. Wenn ein Client **PR_CONTAINER_CONTENTS** im  *LpExcludeProps-Parameter*  für **IMAPIProp::CopyTo** in einem Kopiervorgang angibt, unterstützt der neue Ordner oder Container das Inhaltsverzeichnis des ursprünglichen Ordners oder Containers nicht. 
  
Adressbuchcontainer- und Ordnerinhaltstabellen verfügen über eine lange Liste der erforderlichen Spalten – Spalten, von denen Clients erwarten können, dass sie verfügbar sind, nachdem sie die Tabelle aus **GetContentsTable** oder **OpenProperty** abgerufen haben. Anbieter können diesem erforderlichen Satz bei Bedarf hinzufügen, und Clients können über die **SetColumns-Methode** auch Änderungen anfordern. 
  
Die erforderlichen Spalten für die einzelnen Inhaltstabellentypen sind:
  
|**Erforderliche Spalte**|**Inhaltsverzeichnistyp**|
|:-----|:-----|
|**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |Adressbuchcontainertabellen  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Adressbuchcontainertabellen  <br/> |
|**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> |Nachrichtenspeicherordnertabellen  <br/> |
|**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |Alle Ordnerinhaltstabellen  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Adressbuchcontainertabellen  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Alle Inhaltsverzeichnisse  <br/> |
|**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))  <br/> |Alle Ordnerinhaltstabellen  <br/> |
|**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |Alle Inhaltsverzeichnisse  <br/> |
|**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |Nachrichtenspeicherordnertabellen  <br/> |
|**PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md))  <br/> |Nachrichtenspeicherordnertabellen  <br/> |
|**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |Alle Ordnerinhaltstabellen  <br/> |
|**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |Ordnertabellen für Remotetransporte  <br/> |
|**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |Alle Ordnerinhaltstabellen  <br/> |
|**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |Alle Ordnerinhaltstabellen  <br/> |
|**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))  <br/> |Alle Ordnerinhaltstabellen  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Alle Inhaltsverzeichnisse  <br/> |
|**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))  <br/> |Nachrichtenspeicherordnertabellen  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Ordnertabellen für Adressbuchcontainer und Nachrichtenspeicher  <br/> |
|**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |Ordnertabellen für Remotetransporte  <br/> |
|**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |Nachrichtenspeicherordnertabellen  <br/> |
|**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |Nachrichtenspeicherordnertabellen  <br/> |
   
Der eintragsbezeichner, der für jede Zeile verfügbar ist, kann je nach Tabellenimplementierungen ein kurz- oder langfristiger Eintragsbezeichner sein. Kurzfristige Eintragsbezeichner werden in der Regel in Situationen verwendet, in denen die Leistung ein Problem darstellt. Beide Typen von Eintragsbezeichnern können verwendet werden, um auf das entsprechende Objekt zuzugreifen. 
  
Inhaltstabellen verfügen auch über eine Reihe von Spalten, die optional sind, aber häufig von Dienstanbietern in ihre Implementierungen einbezogen werden. Diese optionalen Spalten sind:
  
|**Optionale Spalte**|**Inhaltsverzeichnistyp**|
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |Nachrichtenspeicherordnertabellen  <br/> |
|**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> |Standardordnerinhaltstabellen  <br/> |
|**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))  <br/> |Standardordnerinhaltstabellen  <br/> |
|**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))  <br/> |Nachrichtenspeicherordnertabellen  <br/> |
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
   
Nachrichtenspeicheranbieter müssen auch **PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) nur für Inhaltstabellen von Suchergebnisordnern enthalten.
  
Benannte Eigenschaften können dem Spaltensatz einer Ordnerinhaltstabelle nur dann hinzugefügt werden, wenn alle Nachrichten im Ordner dieselbe Zuordnungssignatur aufweisen, d. h. die gleiche Zuordnung von Eigenschaftennamen zu Eigenschaftsbezeichnern. Ordnerinhaltstabellen sollten das Hinzufügen von nachrichtenklassenspezifischen Eigenschaften zum Spaltensatz unterstützen, wenn sie die Erstellung beliebiger Nachrichten im Ordner unterstützen.
  
Clients können die Standardsortierreihenfolge für ein Ordnerinhaltsverzeichnis speichern, indem sie die [IMAPIFolder::SaveContentsSort-Methode](imapifolder-savecontentssort.md) aufrufen. Wenn das flag RECURSIVE_SORT beim Aufruf angegeben ist, kann die Sortierreihenfolge so festgelegt werden, dass sie auf alle Unterordner innerhalb des Ordners angewendet wird. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

