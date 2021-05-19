---
title: PidTagAdditionalRenEntryIdsEx (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 57ab68d4c53693c769a4aadf8737f57ef5e73fcd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335203"
---
# <a name="pidtagadditionalrenentryidsex-canonical-property"></a>PidTagAdditionalRenEntryIdsEx (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält spezielle Ordnereintrags-IDs für ein Store-Objekt. Jeder Eintrag in dieser mehrwertigen Eigenschaft kann einem oder mehreren Eintrags-IDs zugeordnet werden, d. h. es besteht eine 1:n-Beziehung zwischen einem Eintrag und den zugehörigen Eintrags-IDs.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ADDITIONAL_REN_ENTRYIDS_EX  <br/> |
|Kennung:  <br/> |0x36D9  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Outlook-Anwendung  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn diese Eigenschaft verwendet wird, enthält sie ein Array von Blöcken, das die Eintrags-IDs für die Ordner angibt. Die Blöcke folgen dem in den folgenden vier Tabellen angegebenen Format.
  
**PersistData-Block**

|**Name**|**Typ**|**Größe**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
|**PersistID** <br/> |WORD  <br/> |2  <br/> |Typbezeichnerwert für diesen **PersistData-Eintrag.** Die Liste der gültigen Werte finden Sie in der Tabelle "PersistBlockType Values".  <br/> |
|**DataElementsSize** <br/> |WORD  <br/> |2  <br/> |Größe des **DataElements-Felds** in Bytes.  <br/> |
|**DataElements** <br/> |Array von **PersistElement-Blöcken**  <br/> |Variable  <br/> |Gibt an, wie viele **PersistElement-Einträge** für den Speicher vorhanden sind. Das Format dieser Struktur finden Sie in der Tabelle "PersistElement Block".  <br/> |
   
**PersistBlockType-Werte**

|**Name**|**Wert**|**Beschreibung**|
|:-----|:-----|:-----|
|PERSIST_SENTINEL  <br/> |0x0000  <br/> |Gibt an, dass keine **weiteren PersistData-Blöcke** verarbeitet werden.  <br/> |
|RSF_PID_RSS_SUBSCRIPTION  <br/> |0x8001  <br/> |Gibt an, dass dieser Block Daten für den Ordner RSS-Abonnements enthält.  <br/> |
|RSF_PID_SEND_AND_TRACK  <br/> |0x8002  <br/> |Gibt an, dass dieser Block Daten für den Ordner "E-Mail-Verarbeitung nachverfolgt" enthält.  <br/> |
|RSF_PID_TODO_SEARCH  <br/> |0x8004  <br/> |Gibt an, dass dieser Block Daten für den Suchordner To-Do enthält.  <br/> |
|RSF_PID_CONV_ACTIONS  <br/> |0x8006  <br/> |Gibt an, dass dieser Block Daten für den Ordner Unterhaltungsaktion Einstellungen enthält.  <br/> |
|RSF_PID_COMBINED_ACTIONS  <br/> |0x8007  <br/> |Dieser Wert ist reserviert.  <br/> |
|RSF_PID_SUGGESTED_CONTACTS  <br/> |0x8008  <br/> |Gibt an, dass dieser Block Daten für den Ordner Vorgeschlagene Kontakte enthält.  <br/> |
|RSF_PID_CONTACT_SEARCH  <br/> |0x8009  <br/> |Gibt an, dass dieser Block Daten für den Ordner "Kontaktesuche" enthält.  <br/> Wird nur von Outlook.  <br/> |
|RSF_PID_BUDDYLIST_PDLS  <br/> |0x800A  <br/> |Gibt an, dass dieser Block Daten für den Ordner Instant Messaging (Instant Messaging) Contact Lists enthält. Der referenzierte Ordner enthält persönliche Verteilerlisten (PDLs), die jede Gruppe innerhalb der Kontaktliste für Im-Minuten-Kontakt darstellen.  <br/> Wird sowohl von Outlook als auch von Exchange.  <br/> |
|RSF_PID_BUDDYLIST_CONTACTS  <br/> |0x800B  <br/> |Gibt an, dass dieser Block Daten für den Ordner "Im-Im-Kontakt"-Ordner enthält. Der referenzierte Ordner enthält die einzelnen Kontakte, auf die von den Kontaktlistengruppen im Im-Im-In-Kontakt verwiesen wird.  <br/> Wird sowohl von Outlook als auch von Exchange.  <br/> |
   
Wenn der **PersistBlockType-Wert** nicht einer der hier definierten ist, wird der **PersistData-Block** ignoriert, und die Verarbeitung wird fortgesetzt, bis entweder eine PERSIST_SENTINEL **PersistID** verarbeitet wird oder das Ende des Datenstroms erreicht ist. 
  
**PersistElementBlock**

|**Name**|**Typ**|**Größe**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
|**ElementID** <br/> |WORD  <br/> |2  <br/> |Gibt den Typbezeichnerwert für diesen **PersistElement-Block** an. Eine Liste der gültigen Werte finden Sie in der Tabelle "PersistElementType Values".  <br/> |
|**ElementDataSize** <br/> |WORD  <br/> |2  <br/> |Gibt die Größe des Felds **ElementData** in Bytes an.  <br/> |
|**ElementData** <br/> |Array von Binärdaten  <br/> |Variable  <br/> |Enthält die Daten für dieses PersistID-ElementID-Paar.  +    <br/> |
   
**PersistElementType-Werte**

|**Name**|**Wert**|**Wert von ElementDataSize**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
|RSF_ELID_HEADER  <br/> |0x0002  <br/> |0x0004  <br/> |Gibt an, dass das **ElementData-Feld** dieses Blocks einen DWORD-Headerwert enthält. Wie dieser Wert interpretiert wird, hängt vom **PersistID-Typ des Blocks** ab.  <br/> Für alle in [[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb.aspx)angegebenen **PersistID-Typen** ist dieser Wert null.  <br/> |
|RSF_ELID_ENTRYID  <br/> |0x0001  <br/> |Variable  <br/> |Gibt an, dass dieser Block die **EntryID** des durch **PersistID angegebenen Ordners enthält.**  <br/> |
|ELEMENT_SENTINEL  <br/> |0x0000  <br/> |0x0000  <br/> |Gibt an, dass keine **weiteren PersistElement-Blöcke** verarbeitet werden.  <br/> |
   
Wenn der **PersistElementType-Wert** nicht einer der hier definierten ist, wird der **PersistElement-Block** ignoriert, und die Verarbeitung wird fortgesetzt, bis entweder eine **ELEMENT_SENTINEL-ElementID** verarbeitet wird oder das Ende des Datenstroms erreicht ist. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Ermöglicht die Behandlung von Zulässig-/Sperrlisten und die Ermittlung von Junk-E-Mail-Nachrichten.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge zum Erstellen und Suchen der speziellen Ordner in einem Postfach an.
    
[[MS-OXPHISH]](https://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)
  
> Identifiziert und markiert E-Mail-Nachrichten, die Empfänger dazu verwengen sollen, vertrauliche Informationen (z. B. Kennwörter und andere persönliche Informationen) an eine nicht vertrauenswürdige Quelle zu verschicken.
    
### <a name="header-files"></a>Headerdateien

Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.
    
Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

