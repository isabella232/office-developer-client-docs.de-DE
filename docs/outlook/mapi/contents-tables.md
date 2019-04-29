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
  
Eine Contents-Tabelle enthält Informationen zu Objekten in einem MAPI-Container. Adressbuchanbieter implementieren Inhaltstabellen für jeden ihrer Container, und Nachrichtenspeicher-und Remote Transportanbieter implementieren Inhaltstabellen für Ihre Ordner. In der Tabelle Contents eines Adressbuch Containers werden Informationen zu den zugehörigen Messaging-Benutzer-und Verteilerlisten Objekten aufgelistet, während in der Inhaltstabelle eines Ordners Informationen zu den Nachrichten aufgelistet werden. Inhaltstabellen werden hauptsächlich von Clientanwendungen verwendet. 
  
Es gibt zwei Arten von Ordnerinhaltstabellen:
  
- Standardinhalts Tabellen enthalten Standardnachrichten – Nachrichten, die für einen Benutzer übertragen und sichtbar gemacht werden können. 
    
- Verknüpfte Inhaltstabellen enthalten ausgeblendete, nicht übertragbare Informationen, die von einem Client für einen bestimmten Zweck erstellt wurden, beispielsweise zum Speichern einer alternativen Darstellung einer Standardnachricht. Zugeordnete Informationen werden erstellt, indem das MAPI_ASSOCIATED-Flag an den [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) -Aufruf übergeben wird. 
    
Die Inhaltstabellen der meisten Adressbuchcontainer und viele Ordner unterstützen keine kategorisierte Sortierung. 
  
Auf eine Inhaltstabelle kann durch Aufrufen zugegriffen werden:
  
- [IMAPIContainer::](imapicontainer-getcontentstable.md)getcontentable.
    
    - Oder
    
- [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) mit **PR_CONTAINER_CONTENTS** ([pidtagcontainercontents (](pidtagcontainercontents-canonical-property.md)) oder **PR_FOLDER_ASSOCIATED_CONTENTS** ([pidtagfolderassociatedcontents (](pidtagfolderassociatedcontents-canonical-property.md)) (nur Ordner), die als Property-Tag und IID angegeben sind _IMAPITable als Schnittstellenbezeichner.
    
Nachrichtenspeicher-und Adressbuchanbieter müssen beide Techniken zum Abrufen von Tabelleneigenschaften unterstützen. Es ist nicht akzeptabel, dass Anbieter nur eine Möglichkeit für den Zugriff auf diese Tabellen unterstützen, da Clients erwarten, dass Sie die Wahl haben. 
  
 **** GetContents akzeptiert als Eingabe mehrere Flags, die Einstellungen angeben. Ist diese Einstellung festgelegt, ruft das MAPI_ASSOCIATED-Flag eine zugeordnete Inhaltstabelle ab. Da einige Ordner zugeordnete Inhalte nicht unterstützen und es für Clients keine Möglichkeit gibt, dies vor der Zeit zu bestimmen, **** gibt getcontentable manchmal den Fehler MAPI_E_NO_SUPPORT zurück, wenn eine zugeordnete Inhaltstabelle angefordert wird. 
  
Das MAPI_DEFERRED_ERRORS-Flag gibt dem Implementierer der Tabelle an, dass alle während des Anrufs aufgetretenen Fehler erst später gemeldet werden müssen. 
  
Der Aufruf von **IMAPIProp:: OpenProperty** beinhaltet den Zugriff auf eine Inhaltstabelle durch Öffnen der zugehörigen Eigenschaft, **PR_CONTAINER_CONTENTS** für Adressbuch Inhaltstabellen und Standardordner Inhaltstabellen und **PR_FOLDER_ASSOCIATED_ Inhalte** für verknüpfte Inhaltstabellen. Auch wenn diese Eigenschaften nicht über die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode eines Ordners oder Containers abgerufen werden können, werden Sie in das Eigenschaftentag Array aufgenommen, das von der [IMAPIProp::](imapiprop-getproplist.md) getproplist-Methode zurückgegeben wird. 
  
 **PR_CONTAINER_CONTENTS** kann auch zum einschließen oder Ausschließen einer Inhaltstabelle aus einem Kopiervorgang verwendet werden. Wenn ein Client **PR_CONTAINER_CONTENTS** im *lpExcludeProps* -Parameter für **IMAPIProp:: CopyTo** in einem Kopiervorgang angibt, unterstützt der neue Ordner oder Container die Inhaltstabelle des ursprünglichen Ordners oder Containers nicht. 
  
Tabellen des Adressbuch Containers und des Ordnerinhalts enthalten eine lange Liste der erforderlichen Spalten – Spalten, die Clients erwarten können, nachdem Sie die Tabelle aus **** getcontentable oder **OpenProperty**abgerufen haben. Bei Bedarf können Anbieter zu diesem erforderlichen Satz hinzufügen, und Clients können **** mithilfe der SetColumns-Methode auch Änderungen anfordern. 
  
Die erforderlichen Spalten für die einzelnen Inhaltstypen Tabellen sind:
  
|**Erforderliche Spalte**|**Typ der Inhaltstabelle**|
|:-----|:-----|
|**PR_ADDRTYPE** ([Pidtagaddresstype (](pidtagaddresstype-canonical-property.md))  <br/> |Adressbuch-Container Tabellen  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Adressbuch-Container Tabellen  <br/> |
|**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> |Ordner Tabellen für Nachrichtenspeicher  <br/> |
|**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |Alle Ordnerinhaltstabellen  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Adressbuch-Container Tabellen  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Alle Inhaltstabellen  <br/> |
|**PR_HASATTACH** ([Pidtaghasattachments (](pidtaghasattachments-canonical-property.md))  <br/> |Alle Ordnerinhaltstabellen  <br/> |
|**PR_INSTANCE_KEY** ([Pidtaginstancekey (](pidtaginstancekey-canonical-property.md))  <br/> |Alle Inhaltstabellen  <br/> |
|**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |Ordner Tabellen für Nachrichtenspeicher  <br/> |
|**PR_MAPPING_SIGNATURE** ([Pidtagmappingsignature (](pidtagmappingsignature-canonical-property.md))  <br/> |Ordner Tabellen für Nachrichtenspeicher  <br/> |
|**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |Alle Ordnerinhaltstabellen  <br/> |
|**PR_MESSAGE_DOWNLOAD_TIME** ([Pidtagmessagedownloadtime (](pidtagmessagedownloadtime-canonical-property.md))  <br/> |Ordner Tabellen für Remote Transport  <br/> |
|**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |Alle Ordnerinhaltstabellen  <br/> |
|**PR_MESSAGE_SIZE** ([Pidtagmessagesize (](pidtagmessagesize-canonical-property.md))  <br/> |Alle Ordnerinhaltstabellen  <br/> |
|**PR_MSG_STATUS** ([Pidtagmessagestatus (](pidtagmessagestatus-canonical-property.md))  <br/> |Alle Ordnerinhaltstabellen  <br/> |
|**PR_OBJECT_TYPE** ([Pidtagobjecttype (](pidtagobjecttype-canonical-property.md))  <br/> |Alle Inhaltstabellen  <br/> |
|**PR_PARENT_ENTRYID** ([Pidtagparententryid (](pidtagparententryid-canonical-property.md))  <br/> |Ordner Tabellen für Nachrichtenspeicher  <br/> |
|**PR_RECORD_KEY** ([Pidtagrecordkey (](pidtagrecordkey-canonical-property.md))  <br/> |Adressbuchcontainer-und Nachrichtenspeicher Ordner-Tabellen  <br/> |
|**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |Ordner Tabellen für Remote Transport  <br/> |
|**PR_STORE_ENTRYID** ([Pidtagstoreentryid (](pidtagstoreentryid-canonical-property.md))  <br/> |Ordner Tabellen für Nachrichtenspeicher  <br/> |
|**PR_STORE_RECORD_KEY** ([Pidtagstorerecordkey (](pidtagstorerecordkey-canonical-property.md))  <br/> |Ordner Tabellen für Nachrichtenspeicher  <br/> |
   
Die für jede Zeile verfügbare Eintrags-ID kann je nach Tabellen Implementierung entweder eine kurz-oder langfristige Eintrags-ID sein. Kurzfristige Eintragsbezeichner werden in der Regel in Situationen verwendet, in denen die Leistung ein Problem ist. Für den Zugriff auf das entsprechende Objekt kann ein beliebiger Eintragsbezeichner verwendet werden. 
  
Inhaltstabellen verfügen außerdem über eine Reihe von Spalten, die optional sind, jedoch in der Regel von Dienstanbietern in ihren Implementierungen enthalten sind. Diese optionalen Spalten sind:
  
|**Optionale Spalte**|**Typ der Inhaltstabelle**|
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |Ordner Tabellen für Nachrichtenspeicher  <br/> |
|**PR_CONTENT_COUNT** ([Pidtagcontentcount (](pidtagcontentcount-canonical-property.md))  <br/> |Standard Ordnerinhaltstabellen  <br/> |
|**PR_CONTENT_UNREAD** ([Pidtagcontentunreadcount (](pidtagcontentunreadcount-canonical-property.md))  <br/> |Standard Ordnerinhaltstabellen  <br/> |
|**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))  <br/> |Ordner Tabellen für Nachrichtenspeicher  <br/> |
|**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |Adressbuch-Container Tabellen  <br/> |
|**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))  <br/> |Alle Ordnerinhaltstabellen  <br/> |
|**PR_MESSAGE_DELIVERY_TIME** ([Pidtagmessagedeliverytime (](pidtagmessagedeliverytime-canonical-property.md))  <br/> |Alle Ordnerinhaltstabellen  <br/> |
|**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))  <br/> |Alle Ordnerinhaltstabellen  <br/> |
|**PR_PRIORITY** ([Pidtagpriority (](pidtagpriority-canonical-property.md))  <br/> |Alle Ordnerinhaltstabellen  <br/> |
|**PR_SEARCH_KEY** ([Pidtagsearchkey (](pidtagsearchkey-canonical-property.md))  <br/> |Adressbuch-Container Tabellen  <br/> |
|**PR_SEND_RICH_INFO** ([Pidtagsendrichinfo (](pidtagsendrichinfo-canonical-property.md))  <br/> |Adressbuch-Container Tabellen  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |Alle Ordnerinhaltstabellen  <br/> |
|**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))  <br/> |Alle Ordnerinhaltstabellen  <br/> |
|**PR_Subject** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |Alle Ordnerinhaltstabellen  <br/> |
|**PR_TRANSMITABLE_DISPLAY_NAME** ([Pidtagtransmittabledisplayname (](pidtagtransmittabledisplayname-canonical-property.md))  <br/> |Adressbuch-Container Tabellen  <br/> |
   
Nachrichtenspeicher Anbieter müssen auch **PR_PARENT_DISPLAY** ([pidtagparentdisplay (](pidtagparentdisplay-canonical-property.md)) für Suchergebnisordner-Inhaltstabellen verwenden.
  
Benannte Eigenschaften können dem Spaltensatz einer Ordnerinhaltstabelle nur hinzugefügt werden, wenn alle Nachrichten im Ordner dieselbe Zuordnungs Signatur aufweisen, also dieselbe Zuordnung von Eigenschaftennamen zu Eigenschaftenbezeichnern. Ordnerinhaltstabellen sollten das Hinzufügen von Nachrichtenklassen spezifischen Eigenschaften zum Spaltensatz unterstützen, wenn Sie das Erstellen beliebiger Nachrichten im Ordner unterstützen.
  
Clients können die Standardsortierreihenfolge für eine Ordnerinhaltstabelle speichern, indem Sie die [IMAPIFolder:: SaveContentsSort](imapifolder-savecontentssort.md) -Methode aufrufen. Wenn das RECURSIVE_SORT-Flag für den Aufruf angegeben wird, kann die Sortierreihenfolge für alle Unterordner innerhalb des Ordners angewendet werden. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

