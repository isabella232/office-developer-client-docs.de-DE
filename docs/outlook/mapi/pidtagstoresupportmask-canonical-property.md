---
title: Kanonische PidTagStoreSupportMask-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreSupportMask
api_type:
- COM
ms.assetid: ada5694a-b5b1-471f-be33-906fc052681a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 143e7f0d2cd89cd4e7956cdda05d1bd512db4027
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340971"
---
# <a name="pidtagstoresupportmask-canonical-property"></a>Kanonische PidTagStoreSupportMask-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Bitmaske von Flags, die von Clientanwendungen abgefragt werden, um die Merkmale eines Nachrichtenspeichers zu bestimmen. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_STORE_SUPPORT_MASK  <br/> |
|Kennung:  <br/> |0x340D  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Sonstiges  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft offenbart die Funktionen eines Nachrichtenspeichers für Clientanwendungen, die eine Nachricht senden möchten. Die Flags können Entscheidungen eines Clients oder eines anderen Speichers unterstützen, beispielsweise ob **PR_BODY** ([pidtagbody (](pidtagbody-canonical-property.md)) oder nur **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) gesendet werden soll. Ein Client sollte **PR_STORE_SUPPORT_MASK**nie festlegen; bei dem Versuch, dieses Flag festzulegen, wird MAPI_E_COMPUTED zurückgegeben. 
  
Eine oder mehrere der folgenden Flags können für die **PR_STORE_SUPPORT_MASK** -Bitmaske festgelegt werden: 
  
STORE_ANSI_OK
  
> (131072, 0x00020000) Der Nachrichtenspeicher unterstützt Eigenschaften, die ANSI-Zeichen (8-Bit) enthalten.
    
STORE_ATTACH_OK 
  
> (32, 0x00000020) Der Nachrichtenspeicher unterstützt Anlagen (OLE oder nicht-OLE) für Nachrichten. 
    
STORE_CATEGORIZE_OK 
  
> (1024, 0x00000400) Der Nachrichtenspeicher unterstützt kategorisierte Ansichten von Tabellen. 
    
STORE_CREATE_OK 
  
> (16, 0x00000010) Der Nachrichtenspeicher unterstützt das Erstellen neuer Nachrichten. 
    
STORE_ENTRYID_UNIQUE 
  
> (1, 0x00000001) Eintragsbezeichner für die Objekte im Nachrichtenspeicher sind eindeutig, also nie wieder verwendet während der Lebensdauer des Speichers. 
    
STORE_HTML_OK 
  
> (65536, 0x00010000) Der Nachrichtenspeicher unterstützt HTML-Nachrichten, die in der **PR_BODY_HTML** ([pidtagbodyhtml (](pidtagbodyhtml-canonical-property.md))-Eigenschaft gespeichert werden. Wenn in der Entwicklungsumgebung ein MAPIDEFS verwendet wird. H die Datei, die nicht STORE_HTML_OK enthält, verwenden Sie stattdessen den Wert 0x00010000. 
    
STORE_ITEMPROC
  
> (2097152, 0x00200000) Gibt in einem umbrochenen PST-Speicher an, dass beim Eintreffen einer neuen Nachricht im Speicher der speicherregeln und die Spamfilter Verarbeitung für die Nachricht separat ausführt. Der Store ruft [IMAPISupport:: notify](imapisupport-notify.md)auf, legt **Uleventmaskfnevnewmail** in der [Benachrichtigungs](notification.md) Struktur fest, die als Parameter übergeben wird, und übergibt dann die Details der neuen Nachricht an den überwachenden Client. Wenn der überwachende Client die Nachricht erhält, wendet er keine Regeln darauf an. 
    
STORE_LOCALSTORE
  
> (524288, 0x00080000) Dieses Flag ist reserviert und sollte nicht verwendet werden.
    
STORE_MODIFY_OK 
  
> (8, 0x00000008) Der Nachrichtenspeicher unterstützt die Änderung der vorhandenen Nachrichten. 
    
STORE_MV_PROPS_OK 
  
> (512, 0x00000200) Der Nachrichtenspeicher unterstützt mehrwertige Eigenschaften, garantiert die Stabilität der Wertreihenfolge in einer mehrwertigen Eigenschaft während eines Speichervorgangs und unterstützt die Instanziierung von mehrwertigen Eigenschaften in Tabellen. 
    
STORE_NOTIFY_OK 
  
> (256, 0x00000100) Der Nachrichtenspeicher unterstützt Benachrichtigungen. 
    
STORE_OLE_OK 
  
> (64, 0x00000040) Der Nachrichtenspeicher unterstützt OLE-Anlagen. Auf die OLE-Daten kann über eine **IStorage** -Schnittstelle zugegriffen werden, wie Sie über die **PR_ATTACH_DATA_OBJ** ([pidtagattachdataobject (](pidtagattachdataobject-canonical-property.md))-Eigenschaft verfügbar ist. 
    
STORE_PUBLIC_FOLDERS 
  
> (16384, 0x00004000) Die Ordner in diesem Speicher sind öffentlich (mehr Benutzer) und nicht privat (möglicherweise mehrere Instanzen, jedoch nicht mehrere Benutzer). 
    
STORE_PUSHER_OK
  
> (8388608, 0x00800000) Der MAPI-Protokoll Handler crawlt den Speicher nicht, und der Speicher ist dafür verantwortlich, alle Änderungen durch Benachrichtigungen an den Indexer zu übertragen, damit Nachrichten indiziert werden.
    
STORE_READONLY 
  
> (2, 0x00000002) Alle Schnittstellen für den Nachrichtenspeicher weisen eine schreibgeschützte Zugriffsebene auf. 
    
STORE_RESTRICTION_OK 
  
> (4096, 0x00001000) Der Nachrichtenspeicher unterstützt Einschränkungen. 
    
STORE_RTF_OK 
  
> (2048, 0x00000800) Der Nachrichtenspeicher unterstützt RTF-Nachrichten (Rich Text Format), in der Regel komprimiert, und der Speicher selbst hält **PR_BODY** und **PR_RTF_COMPRESSED** synchronisiert. 
    
STORE_RULES_OK
  
> (268435456, 0x10000000) Gibt an, dass Regeln in diesem PST-Speicher gespeichert werden sollen, auch wenn es sich nicht um den Standardspeicher handelt. Wenn **STORE_RULES_OK** in Verbindung mit **NON_EMS_XP_SAVE**verwendet wird, können Regeln auf nicht-standardmäßigen PST-umgebrochenen speichern ausgeführt werden.
    
STORE_SEARCH_OK 
  
> (4, 0x00000004) Der Nachrichtenspeicher unterstützt Ordner mit Suchergebnissen. 
    
STORE_SORT_OK 
  
> (8192, 0x00002000) Der Nachrichtenspeicher unterstützt das Sortieren von Tabellen Ansichten. 
    
STORE_SUBMIT_OK 
  
> (128, 0x00000080) Der Nachrichtenspeicher unterstützt das Markieren einer Nachricht für die Übermittlung. 
    
STORE_UNCOMPRESSED_RTF 
  
> (32768, 0x00008000) Der Nachrichtenspeicher unterstützt das Speichern von RTF-Nachrichten in unkomprimierter Form. Ein unkomprimierter RTF-Datenstrom wird durch den Wert **dwMagicUncompressedRTF** im Stream-Header identifiziert. Der **dwMagicUncompressedRTF** -Wert wird in der RTFLIB definiert. H-Datei. 
    
STORE_UNICODE_OK
  
> (262144, 0x00040000) Gibt an, dass der Nachrichtenspeicher Unicode-Speicher unterstützt. Ein Client kann das Vorhandensein dieser Kennzeichnung überprüfen und entscheiden, ob er Unicode-Informationen abruft oder speichert. 
    
Eine RTF-Version einer Nachricht kann immer gespeichert werden, auch wenn der Nachrichtenspeicher nicht im RTF-Format unterstützt wird. Wenn das STORE_RTF_OK-Bit für einen bestimmten Speicher nicht festgelegt ist, muss ein Client, der RTF-Versionen verwaltet, selbst die [RTFSync](rtfsync.md) -Funktion aufrufen, um die **PR_BODY** -und **PR_RTF_COMPRESSED** -Versionen für Textinhalte zu synchronisieren. RTF wird immer in **PR_RTF_COMPRESSED**gespeichert, unabhängig davon, ob es tatsächlich komprimiert ist oder nicht. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXMSG]](https://msdn.microsoft.com/library/b046868c-9fbf-41ae-9ffb-8de2bd4eec82%28Office.15%29.aspx)
  
> Beschreibt das Format der Nachrichten, die zum Senden von Informationen im Zusammenhang mit Freigabeordnern auf dem Client verwendet werden.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

