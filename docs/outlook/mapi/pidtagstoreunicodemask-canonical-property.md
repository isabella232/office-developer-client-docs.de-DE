---
title: PidTagStoreUnicodeMask (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagStoreUnicodeMask
api_type:
- COM
ms.assetid: a6082162-2a74-4850-a0df-4bdbc67b41d8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 438c770e9c004973e6635d575b7a8134891ee964
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629704"
---
# <a name="pidtagstoreunicodemask-canonical-property"></a>PidTagStoreUnicodeMask (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Bitmaske von Flags, die Clientanwendungen abfragen sollten, um die Merkmale eines Nachrichtenspeichers zu ermitteln.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_STORE_UNICODE_MASK  <br/> |
|Kennung:  <br/> |0x340F  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Nachrichtenspeicher  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gibt die Funktionen eines Nachrichtenspeichers für Clientanwendungen offen, die planen, eine Nachricht zu senden. Die Flags können Entscheidungen durch einen Client oder einen anderen Speicher erleichtern, z. B. ob **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) oder nur **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) gesendet werden soll. Ein Client sollte diese Eigenschaft niemals festlegen. Ein Versuch gibt **MAPI_E_COMPUTED** zurück. 
  
Mindestens eines der folgenden Flags kann für diese Eigenschaft festgelegt werden: 
  
STORE_ANSI_OK
  
> (131072, 0x00020000) Der Nachrichtenspeicher unterstützt Eigenschaften, die 8-Bit-Zeichen (American National Standards Institute, ANSI) enthalten.
    
STORE_ATTACH_OK 
  
> (32, 0x00000020) Der Nachrichtenspeicher unterstützt OLE-Anlagen (Object Linking and Embedding) oder Nicht-OLE-Anlagen für Nachrichten. 
    
STORE_CATEGORIZE_OK 
  
> (1024, 0x00000400) Der Nachrichtenspeicher unterstützt kategorisierte Ansichten von Tabellen. 
    
STORE_CREATE_OK 
  
> (16, 0x00000010) Der Nachrichtenspeicher unterstützt das Erstellen neuer Nachrichten. 
    
STORE_ENTRYID_UNIQUE 
  
> (1, 0x00000001) Eintragsbezeichner für die Objekte im Nachrichtenspeicher sind eindeutig, d. h. während der Lebensdauer des Speichers nie wiederverwendet. 
    
STORE_HTML_OK 
  
> (65536, 0x00010000) Der Nachrichtenspeicher unterstützt HTML-Nachrichten, die in der **eigenschaft PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)) gespeichert sind. Beachten Sie, dass **STORE_HTML_OK** in Versionen von MAPIDEFS nicht definiert ist. H, die in Microsoft Exchange 2000 Server und früheren Versionen enthalten sind. Wenn Ihre Entwicklungsumgebung EIN MAPIDEFS verwendet. H-Datei, die nicht **STORE_HTML_OK** enthält, verwenden Sie stattdessen den Wert "0x00010000". 
    
STORE_ITEMPROC
  
> (2097152, 0x00200000) Gibt in einem umschlossenen PST-Speicher an, dass beim Eintreffen einer neuen Nachricht im Speicher Regeln und die Spamfilterverarbeitung für die Nachricht separat ausgeführt werden. Der Speicher ruft [IMAPISupport::Notify](imapisupport-notify.md)auf, legt **fnevNewMail** in der [NOTIFICATION-Struktur](notification.md) fest, die als Parameter übergeben wird, und übergibt dann die Details der neuen Nachricht an den überwachenden Client. Wenn der überwachende Client die Nachricht erhält, wendet er keine Regeln darauf an. 
    
STORE_LOCALSTORE
  
> (524288, 0x00080000) Dieses Flag ist reserviert und sollte nicht verwendet werden.
    
STORE_MODIFY_OK 
  
> (8, 0x00000008) Der Nachrichtenspeicher unterstützt das Ändern der vorhandenen Nachrichten. 
    
STORE_MV_PROPS_OK 
  
> (512, 0x00000200) Der Nachrichtenspeicher unterstützt mehrwertige Eigenschaften, garantiert die Stabilität der Wertreihenfolge in einer mehrwertigen Eigenschaft während eines Speichervorgangs und unterstützt die Instanziierung von mehrwertigen Eigenschaften in Tabellen. 
    
STORE_NOTIFY_OK 
  
> (256, 0x00000100) Der Nachrichtenspeicher unterstützt Benachrichtigungen. 
    
STORE_OLE_OK 
  
> (64, 0x00000040) Der Nachrichtenspeicher unterstützt OLE-Anlagen. Auf die OLE-Daten kann über eine **IStorage-Schnittstelle** zugegriffen werden, z. B. über die **eigenschaft PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)). 
    
STORE_PUBLIC_FOLDERS 
  
> (16384, 0x00004000) Die Ordner in diesem Speicher sind öffentlich (mehrere Benutzer), nicht privat (möglicherweise mehrere Instanzen, aber nicht mehrere Benutzer). 
    
STORE_PUSHER_OK
  
> (8388608, 0x00800000) Der MAPI-Protokollhandler durchforstet den Speicher nicht, und der Speicher ist dafür verantwortlich, änderungen über Benachrichtigungen an den Indexer zu senden, damit Nachrichten indiziert werden.
    
STORE_READONLY 
  
> (2, 0x00000002) Alle Schnittstellen für den Nachrichtenspeicher verfügen über eine schreibgeschützte Zugriffsebene. 
    
STORE_RESTRICTION_OK 
  
> (4096, 0x00001000) Der Nachrichtenspeicher unterstützt Einschränkungen. 
    
STORE_RTF_OK 
  
> (2048, 0x00000800) Der Nachrichtenspeicher unterstützt RTF-Nachrichten (Rich Text Format), in der Regel komprimiert, und der Speicher selbst hält **PR_BODY** und **PR_RTF_COMPRESSED** synchronisiert. 
    
STORE_SEARCH_OK 
  
> (4, 0x00000004) Der Nachrichtenspeicher unterstützt Suchergebnisordner. 
    
STORE_SORT_OK 
  
> (8192, 0x00002000) Der Nachrichtenspeicher unterstützt das Sortieren von Tabellenansichten. 
    
STORE_SUBMIT_OK 
  
> (128, 0x00000080) Der Nachrichtenspeicher unterstützt das Markieren einer Nachricht für die Übermittlung. 
    
STORE_UNCOMPRESSED_RTF 
  
> (32768, 0x00008000) Der Nachrichtenspeicher unterstützt die Speicherung von RTF-Nachrichten (Revisable Form Text) in nicht komprimiertem Format. Ein nicht komprimierter RTF-Stream wird durch den Wert **"mvMagicUncompressedRTF"** im Streamheader identifiziert. Der **wetterMagicUncompressedRTF-Wert** ist in der RTFLIB definiert. H-Datei. 
    
STORE_UNICODE_OK
  
> (262144, 0x00040000) Der Nachrichtenspeicher unterstützt Eigenschaften, die Unicode-Zeichen enthalten.
    
Eine RTF-Version einer Nachricht kann immer gespeichert werden, auch wenn der Nachrichtenspeicher nicht RTF-fähig ist. Wenn das STORE_RTF_OK Bit nicht für einen bestimmten Speicher festgelegt ist, muss ein Client, der RTF-Versionen verwaltet, selbst die [RTFSync-Funktion](rtfsync.md) aufrufen, um die **PR_BODY** und **PR_RTF_COMPRESSED** Versionen für Textinhalte synchronisiert zu halten. RTF wird immer in **PR_RTF_COMPRESSED** gespeichert, unabhängig davon, ob es tatsächlich komprimiert ist oder nicht. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

