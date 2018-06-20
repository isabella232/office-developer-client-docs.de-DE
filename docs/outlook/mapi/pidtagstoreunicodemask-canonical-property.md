---
title: Kanonische PidTagStoreUnicodeMask-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreUnicodeMask
api_type:
- COM
ms.assetid: a6082162-2a74-4850-a0df-4bdbc67b41d8
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 010b17de08ee5836a26c56f300b36822df2e981e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795223"
---
# <a name="pidtagstoreunicodemask-canonical-property"></a>Kanonische PidTagStoreUnicodeMask-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält eine Bitmaske aus Flags, die Clientanwendungen abgefragt werden sollen, um die Eigenschaften eines Nachrichtenspeichers zu bestimmen.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_STORE_UNICODE_MASK  <br/> |
|Bezeichner:  <br/> |0x340F  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Nachrichtenspeicher  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft gibt die Funktionen des einen Nachrichtenspeicher für Clientanwendungen, Planen sie eine Nachricht senden. Die Kennzeichen erleichtern Entscheidungen durch einen Client oder einem anderen Speicher, z. B., ob **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) oder nur **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) gesendet wird. Ein Client sollten diese Eigenschaft festlegen. Ein Versuch gibt **MAPI_E_COMPUTED**zurück. 
  
Für diese Eigenschaft kann eine oder mehrere der folgenden Werte festgelegt werden: 
  
STORE_ANSI_OK
  
> (131072, 0 x 00020000) Der Nachrichtenspeicher unterstützt Eigenschaften, die amerikanischen National Standards Institute (ANSI) (8-Bit) Zeichen enthalten.
    
STORE_ATTACH_OK 
  
> (32, 0 x 00000020) Der Nachrichtenspeicher unterstützt Object Linking und Embedding (OLE) oder nicht-OLE-Anlagen von Nachrichten. 
    
STORE_CATEGORIZE_OK 
  
> (1024, 0 x 00000400) Der Nachrichtenspeicher unterstützt kategorisierte Ansichten von Tabellen. 
    
STORE_CREATE_OK 
  
> (16, 0 x 00000010) Der Nachrichtenspeicher unterstützt die Erstellung von neuen Nachrichten. 
    
STORE_ENTRYID_UNIQUE 
  
> (1, 0 x 00000001) Für die Objekte im Nachrichtenspeicher Eintragsbezeichner sind eindeutig, d. h., während der Lebensdauer des Speichers niemals wiederverwendet. 
    
STORE_HTML_OK 
  
> (65536, 0 x 00010000) Der Nachrichtenspeicher unterstützt HTML-Nachrichten, die in der Eigenschaft **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)) gespeichert. Beachten Sie, dass **STORE_HTML_OK** in Versionen von MAPIDEFS nicht definiert ist. H, die und früher mit Microsoft Exchange 2000 Server enthalten sind. Wenn Ihre Entwicklungsumgebung ein MAPIDEFS verwendet wird. H-Datei, die nicht **STORE_HTML_OK**enthalten, verwenden Sie stattdessen den Wert "0 x 00010000". 
    
STORE_ITEMPROC
  
> (2097152, 0x00200000) Gibt an, dass beim Empfang einer neuen Nachricht im Speicher der Speicher funktioniert Regeln und Spam Filtern Verarbeitung der Nachricht getrennt, in einem gepackten PST-Speicher. Der Informationsspeicher ruft [IMAPISupport::Notify](imapisupport-notify.md), Einstellung **FnevNewMail** in der [Benachrichtigung](notification.md) -Struktur, die als Parameter übergeben wird, und klicken Sie dann die Details der neuen Nachricht an dem listening Client übergibt. Später, wenn der listening Client die Benachrichtigung erhält, verarbeitet es Regeln für die Nachricht nicht. 
    
STORE_LOCALSTORE
  
> (524288, 0x00080000) Dieses Kennzeichen ist reserviert und sollte nicht verwendet werden.
    
STORE_MODIFY_OK 
  
> (8, 0 x 00000008) Der Nachrichtenspeicher unterstützt die Änderung der vorhandenen Nachrichten. 
    
STORE_MV_PROPS_OK 
  
> (512, 0 x 00000200) Der Nachrichtenspeicher mehrwertige Eigenschaften unterstützt, die Stabilität der Reihenfolge der Wert in einer mehrwertigen Eigenschaft in der gesamten Speichervorgang garantiert Vorgang und unterstützt die Instanziierung von mehrwertigen Eigenschaften in Tabellen. 
    
STORE_NOTIFY_OK 
  
> (256, 0 x 00000100) Der Nachrichtenspeicher unterstützt Benachrichtigungen. 
    
STORE_OLE_OK 
  
> (64, 0 x 00000040) Der Nachrichtenspeicher unterstützt OLE-Anlagen. OLE-Daten ist wie über eine Schnittstelle **IStorage** zugänglich über die **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md))-Eigenschaft verfügbar sind. 
    
STORE_PUBLIC_FOLDERS 
  
> (16384, 0x00004000) Der Ordner in diesem Zertifikatspeicher sind öffentliche (mehrere Benutzer) wird nicht private (möglicherweise mit mehreren Instanzen, aber nicht mehrere Benutzer). 
    
STORE_PUSHER_OK
  
> (8388608, 0 x 00800000) Der MAPI-Protokollhandler wird nicht durchforstet werden den Speicher und der Speicher wird zum Pushen von Änderungen durch Benachrichtigungen auf die Indizierung Nachrichten indiziert werden.
    
STORE_READONLY 
  
> (2, 0 x 00000002) Alle Schnittstellen für den Nachrichtenspeicher verfügen über eine nur-Lese-Zugriffsebene. 
    
STORE_RESTRICTION_OK 
  
> (4096, 0 x 00001000) Der Nachrichtenspeicher unterstützt Einschränkungen. 
    
STORE_RTF_OK 
  
> (2048, 0x00000800) Der Nachrichtenspeicher unterstützt Rich Text Format (RTF)-Nachrichten, die in der Regel komprimiert und der Informationsspeicher selbst behält **PR_BODY** **PR_RTF_COMPRESSED** synchronisiert. 
    
STORE_SEARCH_OK 
  
> (4, 0 x 00000004) Der Nachrichtenspeicher unterstützt Suchergebnisse Ordner. 
    
STORE_SORT_OK 
  
> (8192, 0 x 00002000) Der Nachrichtenspeicher unterstützt Sortierung Ansichten von Tabellen. 
    
STORE_SUBMIT_OK 
  
> (128, 0x00000080) Der Nachrichtenspeicher unterstützt Markierens einer Nachricht für die Übermittlung. 
    
STORE_UNCOMPRESSED_RTF 
  
> (32768, 0x00008000) Der Nachrichtenspeicher unterstützt die Speicherung Versionsfähige-Format (RTF)-Text-Nachrichten nicht komprimierten Format. Ein nicht komprimierter RTF-Stream wird durch den Wert **DwMagicUncompressedRTF** im Streamheader identifiziert. Der Wert **DwMagicUncompressedRTF** ist in der RTFLIB definiert. H-Datei. 
    
STORE_UNICODE_OK
  
> (262144, 0 x 00040000) Der Nachrichtenspeicher unterstützt Eigenschaften, die Unicode-Zeichen enthält.
    
Eine RTF-Version einer Nachricht kann immer gespeichert werden, selbst wenn der Nachrichtenspeicher RTF nicht bekannt ist. Wenn das Bit STORE_RTF_OK für einen bestimmten Speicher nicht festgelegt ist, müssen einen Client RTF-Versionen verwalten die [RTFSync](rtfsync.md) -Funktion, um die **PR_BODY** und **PR_RTF_COMPRESSED** Versionen für Textinhalt synchronisiert halten aufrufen. RTF wird immer in **PR_RTF_COMPRESSED**, gespeichert, ob es tatsächlich oder nicht komprimiert werden. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

