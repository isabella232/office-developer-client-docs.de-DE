---
title: Kanonische PidTagAdditionalRenEntryIdsEx-Eigenschaft
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
ms.openlocfilehash: d3a8dc45bb131f5d2e7ff370617a10e3096a99f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794054"
---
# <a name="pidtagadditionalrenentryidsex-canonical-property"></a>Kanonische PidTagAdditionalRenEntryIdsEx-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Ordner mit Sonderfunktion Eintrags-IDs für ein Store-Objekt enthält. Jeder Eintrag in dieser mehrwertige Eigenschaft kann eine oder mehrere EntryIDs zugeordnet werden, d. h., eine 1: n-Beziehung zwischen dem Eintrag und die zugeordneten Eintrags-IDs vorhanden ist.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_ADDITIONAL_REN_ENTRYIDS_EX  <br/> |
|Bezeichner:  <br/> |0x36D9  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Outlook-Anwendung  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn diese Eigenschaft verwendet wird, enthält sie ein Array von Blöcken, die Eintrags-IDs für die Ordner angibt. Die Blöcke führen Sie das Format durch die folgenden vier Tabellen angegeben.
  
**PersistData blockieren**

|**Name**|**Typ**|**Size**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
|**Wobei Sie PersistID** <br/> |WORD  <br/> |2  <br/> |Geben Sie für diesen Eintrag **PersistData** -ID-Wert. Finden Sie in der Tabelle "PersistBlockType Werte" für die Liste der gültigen Werte.  <br/> |
|**DataElementsSize** <br/> |WORD  <br/> |2  <br/> |Größe des Feld **DataElements** in Bytes.  <br/> |
|**DataElements** <br/> |Array **PersistElement** Blöcke  <br/> |Variable  <br/> |Gibt an, wie viele **PersistElement** -Einträge für den Speicher befinden. Finden Sie in der Tabelle "PersistElement blockieren" für das Format der diese Struktur.  <br/> |
   
**PersistBlockType Werte**

|**Name**|**Wert**|**Beschreibung**|
|:-----|:-----|:-----|
|PERSIST_SENTINEL  <br/> |0x0000  <br/> |Gibt an, dass keine weitere **PersistData** Blöcke verarbeitet werden.  <br/> |
|RSF_PID_RSS_SUBSCRIPTION  <br/> |0x8001  <br/> |Gibt an, dass dieser Block für den Ordner RSS-Abonnements Daten enthält.  <br/> |
|RSF_PID_SEND_AND_TRACK  <br/> |0x8002  <br/> |Gibt an, dass dieser Block Daten für die Verarbeitung von Nachrichten durch nachverfolgt Ordner enthält.  <br/> |
|RSF_PID_TODO_SEARCH  <br/> |0x8004  <br/> |Gibt an, dass dieser Block für die Aufgabe Suchordner Daten enthält.  <br/> |
|RSF_PID_CONV_ACTIONS  <br/> |0x8006  <br/> |Gibt an, dass dieser Block Daten für den Ordner für die Unterhaltung Aktion Einstellungen enthält.  <br/> |
|RSF_PID_COMBINED_ACTIONS  <br/> |0x8007  <br/> |Dieser Wert ist reserviert.  <br/> |
|RSF_PID_SUGGESTED_CONTACTS  <br/> |0x8008  <br/> |Gibt an, dass dieser Block Daten für den Ordner vorgeschlagene Kontakte enthält.  <br/> |
|RSF_PID_CONTACT_SEARCH  <br/> |0x8009  <br/> |Gibt an, dass dieser Block Daten für den Ordner Kontakte suchen enthält.  <br/> Nur vom Outlook verwendet.  <br/> |
|RSF_PID_BUDDYLIST_PDLS  <br/> |0x800A  <br/> |Gibt an, dass dieser Block mit Daten für den Ordner Kontaktlisten Instant Messaging (IM) enthält. Der referenzierte Ordner enthält persönlichen Verteilerlisten (persönlichen Verteilerlisten), die jede Gruppe in der Liste im-Kontakt darstellt.  <br/> Wird von Outlook und Exchange verwendet.  <br/> |
|RSF_PID_BUDDYLIST_CONTACTS  <br/> |0x800B  <br/> |Gibt an, dass dieser Block Daten für den Ordner im-Kontakte enthält. Der referenzierte Ordner enthält die einzelnen Kontakte, die durch die Instant Messaging-Kontaktliste Gruppen.  <br/> Wird von Outlook und Exchange verwendet.  <br/> |
   
Wenn der Wert der **PersistBlockType** nicht der hier definiert ist, der **PersistData** -Block wird ignoriert, und Verarbeitung wird fortgesetzt, bis entweder eine PERSIST_SENTINEL **wobei Sie PersistID** verarbeitet oder das Ende des Datenstroms erreicht ist. 
  
**PersistElementBlock**

|**Name**|**Typ**|**Size**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
|**ElementID** <br/> |WORD  <br/> |2  <br/> |Gibt den Wert für diesen Block **PersistElement** Typ-ID an. Finden Sie in der Tabelle "PersistElementType Werte" für eine Liste gültiger Werte.  <br/> |
|**ElementDataSize** <br/> |WORD  <br/> |2  <br/> |Gibt die Größe in Bytes im Feld **ElementData** an.  <br/> |
|**ElementData** <br/> |Array von Binärdaten  <br/> |Variable  <br/> |Enthält die Daten für dieses **wobei Sie PersistID** + **ElementID** -Paar.  <br/> |
   
**PersistElementType Werte**

|**Name**|**Wert**|**Wert der ElementDataSize**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
|RSF_ELID_HEADER  <br/> |0x0002  <br/> |0x0004  <br/> |Gibt an, dass dieser Block **ElementData** Feld einen Header DWORD-Wert enthält. Wie dieser Wert interpretiert wird, hängt von den Block **wobei Sie PersistID** Typ ab.  <br/> Für alle **wobei Sie PersistID** Typen in [[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb.aspx)angegeben beträgt dieser Wert 0 (null).  <br/> |
|RSF_ELID_ENTRYID  <br/> |0x0001  <br/> |Variable  <br/> |Gibt an, dass dieser Block die **EntryID** des Ordners ein, **wobei Sie PersistID**gemäß enthält.  <br/> |
|ELEMENT_SENTINEL  <br/> |0x0000  <br/> |0x0000  <br/> |Gibt an, dass keine weitere **PersistElement** Blöcke verarbeitet werden.  <br/> |
   
Wenn der Wert der **PersistElementType** nicht der hier definiert ist, der **PersistElement** -Block wird ignoriert, und Verarbeitung wird fortgesetzt, bis entweder eine ELEMENT_SENTINEL **ElementID** verarbeitet oder das Ende des Datenstroms erreicht ist. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Ermöglicht die Behandlung von zulassen/blockieren-Listen und die Bestimmung des junk-e-Mail-Nachrichten.
    
[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen für das Erstellen und Ordner mit Sonderfunktion in einem Postfach suchen.
    
[[MS-OXPHISH]](http://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)
  
> Identifiziert und e-Mail-Nachrichten, die an Empfänger Preisgabe von vertraulichen Informationen (wie Kennwörter und andere persönliche Informationen) zu einer nicht vertrauenswürdigen Quelle markiert.
    
### <a name="header-files"></a>Header-Dateien

Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.
    
Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[�bersicht �ber die MAPI-Eigenschaft](mapi-property-overview.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

