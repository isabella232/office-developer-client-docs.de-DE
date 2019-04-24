---
title: Kanonische Pidtagadditionalrenentryidsex (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAdditionalRenEntryIdsEx
api_type:
- HeaderDef
ms.assetid: b5e896e7-c0c6-4ad1-bf91-9daba3a1e4d4
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 57ab68d4c53693c769a4aadf8737f57ef5e73fcd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335203"
---
# <a name="pidtagadditionalrenentryidsex-canonical-property"></a>Kanonische Pidtagadditionalrenentryidsex (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält spezielle Ordnereintrags-IDs für ein Store-Objekt. Jeder Eintrag in dieser mehrwertigen Eigenschaft kann einer oder mehreren Eintrags-IDs zugeordnet werden, das heißt, es gibt eine 1: n-Beziehung zwischen einem Eintrag und den zugehörigen Eintrags-IDs.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ADDITIONAL_REN_ENTRYIDS_EX  <br/> |
|Kennung:  <br/> |0x36D9  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Outlook-Anwendung  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn diese Eigenschaft verwendet wird, enthält Sie ein Array von Blöcken, die die Eintrags-IDs für die Ordner angeben. Die Blöcke entsprechen dem in den folgenden vier Tabellen angegebenen Format.
  
**PersistData-Block**

|**Name**|**Typ**|**Size**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
|**Persistenz** <br/> |WORD  <br/> |2  <br/> |Typ-ID-Wert für diesen **PersistData** -Eintrag. Die Liste gültiger Werte finden Sie in der Tabelle "PersistBlockType-Werte".  <br/> |
|**DataElementsSize** <br/> |WORD  <br/> |2  <br/> |Die Größe des dataElements- **** Felds in Byte.  <br/> |
|**DataElements** <br/> |Array von **persistelement** -Blöcken  <br/> |Variable  <br/> |Gibt an, **** wie viele persistelement-Einträge für den Speicher vorhanden sind. Weitere Informationen finden Sie in der Tabelle "Persistelement-Block" für das Format dieser Struktur.  <br/> |
   
**PersistBlockType-Werte**

|**Name**|**Wert**|**Beschreibung**|
|:-----|:-----|:-----|
|PERSIST_SENTINEL  <br/> |0x0000  <br/> |Gibt an, dass keine weiteren **PersistData** -Blöcke verarbeitet werden.  <br/> |
|RSF_PID_RSS_SUBSCRIPTION  <br/> |0x8001  <br/> |Gibt an, dass dieser Blockdaten für den RSS-Abonnements Ordner enthält.  <br/> |
|RSF_PID_SEND_AND_TRACK  <br/> |0x8002  <br/> |Gibt an, dass dieser Blockdaten für den verFolgten e-Mail-Verarbeitungs Ordner enthält.  <br/> |
|RSF_PID_TODO_SEARCH  <br/> |0x8004  <br/> |Gibt an, dass dieser Blockdaten für den Aufgaben Suchordner enthält.  <br/> |
|RSF_PID_CONV_ACTIONS  <br/> |0x8006  <br/> |Gibt an, dass dieser Blockdaten für den Unterhaltungs Aktions Ordner enthält.  <br/> |
|RSF_PID_COMBINED_ACTIONS  <br/> |0x8007  <br/> |Dieser Wert ist reserviert.  <br/> |
|RSF_PID_SUGGESTED_CONTACTS  <br/> |0x8008  <br/> |Gibt an, dass dieser Blockdaten für den vorgeschlagenen Ordner Kontakte enthält.  <br/> |
|RSF_PID_CONTACT_SEARCH  <br/> |0x8009  <br/> |Gibt an, dass dieser Blockdaten für den Suchordner Kontakte enthält.  <br/> Wird nur von Outlook verwendet.  <br/> |
|RSF_PID_BUDDYLIST_PDLS  <br/> |0x800A  <br/> |Gibt an, dass dieser Blockdaten für den Instant Messaging-Kontaktlistenordner (Chat) enthält. Der referenzierte Ordner enthält persönliche Verteilerlisten (PDLs), die jede Gruppe in der Chatkontaktliste darstellen.  <br/> Wird sowohl von Outlook als auch von Exchange verwendet.  <br/> |
|RSF_PID_BUDDYLIST_CONTACTS  <br/> |0x800B  <br/> |Gibt an, dass dieser Blockdaten für den IM-Kontakteordner enthält. Der referenzierte Ordner enthält die einzelnen Kontakte, auf die von den Kontaktlisten Gruppen der Sofortnachrichten verwiesen wird.  <br/> Wird sowohl von Outlook als auch von Exchange verwendet.  <br/> |
   
Wenn der **PersistBlockType** -Wert nicht einer der hier definierten ist, wird der **PersistData** -Block ignoriert, und die Verarbeitung wird fortgesetzt, bis eine PERSIST_SENTINEL- **Persistenz** -oder das Ende des Streams erreicht ist. 
  
**PersistElementBlock**

|**Name**|**Typ**|**Size**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
|**ElementID** <br/> |WORD  <br/> |2  <br/> |Gibt den Typ-Bezeichnerwert für **** diesen persistelement-Block an. In der Tabelle "PersistElementType-Werte" finden Sie eine Liste gültiger Werte.  <br/> |
|**ElementDataSize** <br/> |WORD  <br/> |2  <br/> |Gibt die Größe des **ElementData** -Felds in Byte an.  <br/> |
|**ElementData** <br/> |Array von Binärdaten  <br/> |Variable  <br/> |Enthält die Daten für dieses Element-Paar des **Persist** + -**Elements** .  <br/> |
   
**PersistElementType-Werte**

|**Name**|**Wert**|**Wert von ElementDataSize**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
|RSF_ELID_HEADER  <br/> |0x0002  <br/> |0x0004  <br/> |Gibt an, dass das **ElementData** -Feld dieses Blocks einen DWORD-Header Wert enthält. Wie dieser Wert interpretiert wird, hängt vom **Persist** -Typ des Blocks ab.  <br/> Für alle **** in [[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb.aspx)angegebenen persistenztypen ist dieser Wert 0 (null).  <br/> |
|RSF_ELID_ENTRYID  <br/> |0x0001  <br/> |Variable  <br/> |Gibt an, dass dieser Block **** die Eintrags-Nr. des **** durch Persistable angegebenen Ordners enthält.  <br/> |
|ELEMENT_SENTINEL  <br/> |0x0000  <br/> |0x0000  <br/> |Gibt an, dass **** keine weiteren persistelement-Blöcke verarbeitet werden.  <br/> |
   
Wenn der **PersistElementType** -Wert nicht einer der hier definierten ist, wird der **persistelement** -Block ignoriert, und die Verarbeitung wird fortgesetzt, bis eine ELEMENT_SENTINEL- **Element** -Nr verarbeitet oder das Ende des Streams erreicht ist. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Ermöglicht die Behandlung von Allow/Block-Listen und die Bestimmung von Junk-e-Mails.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge zum Erstellen und suchen der speziellen Ordner in einem Postfach an.
    
[[MS-OXPHISH]](https://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)
  
> Identifiziert und markiert e-Mail-Nachrichten, die dazu dienen, Empfänger dazu zu verleiten, vertrauliche Informationen (wie Kennwörter und andere persönliche Informationen) an eine nicht vertrauenswürdige Quelle weiterzugeben.
    
### <a name="header-files"></a>Header Dateien

Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

