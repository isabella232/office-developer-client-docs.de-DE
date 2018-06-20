---
title: Inhalt von Tabellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7b8efb4e-b5be-41b8-81bb-9aa1da421433
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0dd79d9630837b5ec8a709d386ccc0db987dfb5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791435"
---
# <a name="contents-tables"></a>Inhalt von Tabellen

  
  
**Betrifft**: Outlook 
  
Eine Inhaltstabelle enthält Informationen zu Objekten in einem MAPI-Container. Von adressbuchanbietern implementierte implementieren Sie Inhalt Tabellen für jeden ihrer Container und Nachrichtenspeicher und remote-Transport-Anbieter Inhalt Tabellen für ihre Ordner. Die Inhaltstabelle ein Adressbuchcontainer enthält Informationen zu den messaging Listenobjekten Benutzer- und Verteilung, während der Inhalt eines Ordners Informationen zu eigenen Nachrichten in der Tabelle ist. Inhalt Tabellen werden hauptsächlich von Clientanwendungen verwendet. 
  
Es gibt zwei Arten von Ordner Inhalt Tabellen:
  
- Standard-Inhalt Tabellen enthalten standard Nachrichten – Nachrichten, die übertragen und für einen Benutzer sichtbar gemacht werden können. 
    
- Zugehörige Inhalt Tabellen enthalten ausgeblendet, Übertragungseinehit Informationen, die von einem Client wie, eine Alternative Darstellung einer standard-Nachricht speichern für einen bestimmten Zweck, erstellt. Zugehörige Informationen wird erstellt, indem Sie das MAPI_ASSOCIATED-Flag für den Aufruf der [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) übergeben. 
    
Die Inhalte, die keine für Tabellen mit den meisten Address Book Containern und viele Ordner Unterstützung kategorisiert sortieren. 
  
Eine Inhaltstabelle kann durch Aufrufen von zugegriffen werden:
  
- [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).
    
    - Oder -
    
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md) mit **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) oder **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) (nur Ordner) als Eigenschafts-Tag und IID angegeben _IMAPITable als Schnittstellenbezeichner.
    
Nachrichtenspeicher und Address Book Anbieter müssen beide Verfahren zum Abrufen von Eigenschaften der Tabelle unterstützen. Es ist nicht zulässig für Anbieter unterstützt nur eine Möglichkeit für den Zugriff auf diese Tabellen, da Clients erwarten, dass die Option haben. 
  
 **GetContentsTable** , die als Eingabe akzeptiert mehrere Flags, die Voreinstellungen angeben. Das Flag MAPI_ASSOCIATED bei Festlegung einer zugeordneten Inhaltstabelle abgerufen werden. Da einige Ordner zugeordneten Inhalt nicht unterstützt, und es keine Möglichkeit für Clients gibt, die diese vorausschauendes Bestimmung, gibt **GetContentsTable** manchmal den Fehler MAPI_E_NO_SUPPORT zurück, wenn einer zugeordneten Inhaltstabelle angefordert wird. 
  
Das Flag MAPI_DEFERRED_ERRORS gibt an, das die Implementierung von der Tabelle, die während des Anrufs aufgetretenen nicht bis zu einem späteren Zeitpunkt gemeldet werden müssen. 
  
Der Aufruf von **IMAPIProp::OpenProperty** umfasst den Zugriff auf eine Inhaltstabelle durch Öffnen der entsprechenden Eigenschaft **PR_CONTAINER_CONTENTS** für Address Book Inhalt Tabellen und Standardordner Inhalt Tabellen und **PR_FOLDER_ASSOCIATED_ Inhalt** für verknüpfte Tabellen Inhalt. Jedoch weder oder diese Eigenschaften können über einen Ordner oder für den Container [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode abgerufen werden, sie sind in der von der [IMAPIProp::GetPropList](imapiprop-getproplist.md) -Methode zurückgegebene Array Eigenschaft Tag enthalten. 
  
 **PR_CONTAINER_CONTENTS** kann auch ein-oder Ausschließen einer Inhaltstabelle aus einem Kopiervorgang verwendet werden. Wenn ein Client **PR_CONTAINER_CONTENTS** im *LpExcludeProps* -Parameter für **IMAPIProp::CopyTo** in einen Kopiervorgang angibt, wird der neuen Ordner oder im Container nicht der Inhaltstabelle des ursprünglichen Ordner oder des Containers unterstützt. 
  
Address Book Container und Ordner Inhalt Tabellen haben eine lange Liste von erforderlichen Spalten – Spalten, die Clients zur Verfügung, nachdem sie die Tabelle aus **GetContentsTable** oder **OpenProperty**abrufen erwarten können. Anbieter können auf diesen Satz von erforderlichen hinzufügen, wenn Bedarf und Clients, mit der **SetColumns** -Methode auch Änderungen angefordert werden können. 
  
Die erforderlichen Spalten für die einzelnen Arten von Inhalt Tabellen sind:
  
|**Erforderliche Spalte**|**Typ der Inhaltstabelle**|
|:-----|:-----|
|**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |Address Book Container Tabellen  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Address Book Container Tabellen  <br/> |
|**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> |Nachricht Store Ordner Tabellen  <br/> |
|**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |Alle Ordner Inhalt Tabellen  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Address Book Container Tabellen  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Alle Inhalte Tabellen  <br/> |
|**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))  <br/> |Alle Ordner Inhalt Tabellen  <br/> |
|**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |Alle Inhalte Tabellen  <br/> |
|**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |Nachricht Store Ordner Tabellen  <br/> |
|**PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md))  <br/> |Nachricht Store Ordner Tabellen  <br/> |
|**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |Alle Ordner Inhalt Tabellen  <br/> |
|**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |Remote-Transport Ordner Tabellen  <br/> |
|**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |Alle Ordner Inhalt Tabellen  <br/> |
|**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |Alle Ordner Inhalt Tabellen  <br/> |
|**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))  <br/> |Alle Ordner Inhalt Tabellen  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Alle Inhalte Tabellen  <br/> |
|**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))  <br/> |Nachricht Store Ordner Tabellen  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Speichern von Adressbuchcontainer und Nachricht Ordner Tabellen  <br/> |
|**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |Remote-Transport Ordner Tabellen  <br/> |
|**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |Nachricht Store Ordner Tabellen  <br/> |
|**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |Nachricht Store Ordner Tabellen  <br/> |
   
Verfügbar mit jeder Zeile die Eintrags-ID kann entweder eine kurz- oder langfristig Eintrags-ID, je nach der Implementierung der Tabelle sein. Kurzfristige-Eintragsbezeichner werden normalerweise in Situationen verwendet, in dem Leistung von Belang ist. Beide Arten von Eintrags-ID kann verwendet werden, auf das entsprechende Objekt zugreifen. 
  
Inhalt Tabellen haben auch eine Reihe von Spalten, die optional, wird jedoch von Dienstanbietern in ihre Implementierungen häufig enthalten sind. Diese optionalen Spalten sind:
  
|**Optionale Spalte**|**Typ der Inhaltstabelle**|
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |Nachricht Store Ordner Tabellen  <br/> |
|**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> |Standardordner Inhalt Tabellen  <br/> |
|**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))  <br/> |Standardordner Inhalt Tabellen  <br/> |
|**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))  <br/> |Nachricht Store Ordner Tabellen  <br/> |
|**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |Address Book Container Tabellen  <br/> |
|**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))  <br/> |Alle Ordner Inhalt Tabellen  <br/> |
|**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |Alle Ordner Inhalt Tabellen  <br/> |
|**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))  <br/> |Alle Ordner Inhalt Tabellen  <br/> |
|**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |Alle Ordner Inhalt Tabellen  <br/> |
|**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |Address Book Container Tabellen  <br/> |
|**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md))  <br/> |Address Book Container Tabellen  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |Alle Ordner Inhalt Tabellen  <br/> |
|**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))  <br/> |Alle Ordner Inhalt Tabellen  <br/> |
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |Alle Ordner Inhalt Tabellen  <br/> |
|**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))  <br/> |Address Book Container Tabellen  <br/> |
   
Nachricht-Anbieter müssen auch **PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) Suchergebnis Ordner Inhalt nur für Tabellen enthalten.
  
Benannte Eigenschaften können auf die Spalte einer Tabelle der Ordner-Inhalt hinzugefügt werden, nur, wenn alle Nachrichten in den Ordner die gleiche Zuordnung Signatur, d. h., der Zuordnung von Eigenschaftennamen Eigenschaftenbezeichner haben. Wenn sie die Erstellung von beliebigen Nachrichten im Ordner unterstützen, sollte Ordner Inhalt Tabellen hinzufügen Nachrichtenklasse spezifische Eigenschaften auf die Spalte festzulegen, unterstützen.
  
Clients können die Standard-Sortierreihenfolge für einen Ordner Inhaltstabelle speichern, dessen [IMAPIFolder::SaveContentsSort](imapifolder-savecontentssort.md) -Methode aufrufen. Wenn das Flag RECURSIVE_SORT dem Gespräch angegeben wird, kann die Sortierreihenfolge vorgenommen werden, auf alle Unterordner innerhalb des Ordners anwenden. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

