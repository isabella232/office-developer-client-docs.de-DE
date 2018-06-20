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
ms.openlocfilehash: 8d9f6311b19ddb489885004a9e507f780d9f1ea9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795220"
---
# <a name="pidtagstoresupportmask-canonical-property"></a>Kanonische PidTagStoreSupportMask-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält einer Bitmaske aus Flags dieser Client Applications Abfrage aus, um die Eigenschaften eines Nachrichtenspeichers bestimmen. 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_STORE_SUPPORT_MASK  <br/> |
|Bezeichner:  <br/> |0x340D  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Verschiedenes  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft gibt die Funktionen des einen Nachrichtenspeicher für Clientanwendungen, die planen sie eine Nachricht senden. Die Kennzeichen unterstützen Entscheidungen durch einen Client oder einem anderen Speicher, z. B., ob **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) oder nur **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) gesendet. Ein Client sollte niemals **PR_STORE_SUPPORT_MASK**festgelegt. Beim Festlegen dieses Kennzeichen gibt MAPI_E_COMPUTED zurück. 
  
Für die Bitmaske **PR_STORE_SUPPORT_MASK** kann eine oder mehrere der folgenden Werte festgelegt werden: 
  
STORE_ANSI_OK
  
> (131072, 0 x 00020000) Der Nachrichtenspeicher unterstützt Eigenschaften, die ANSI (8-Bit) Zeichen enthalten.
    
STORE_ATTACH_OK 
  
> (32, 0 x 00000020) Nachrichtenspeicher werden Anlagen (OLE oder nicht-OLE) von Nachrichten unterstützt. 
    
STORE_CATEGORIZE_OK 
  
> (1024, 0 x 00000400) Der Nachrichtenspeicher unterstützt kategorisierte Ansichten von Tabellen. 
    
STORE_CREATE_OK 
  
> (16, 0 x 00000010) Der Nachrichtenspeicher unterstützt die Erstellung von neuen Nachrichten. 
    
STORE_ENTRYID_UNIQUE 
  
> (1, 0 x 00000001) Für die Objekte im Nachrichtenspeicher Eintragsbezeichner sind eindeutig, d. h., während der Lebensdauer des Speichers niemals wiederverwendet. 
    
STORE_HTML_OK 
  
> (65536, 0 x 00010000) Der Nachrichtenspeicher unterstützt HTML-Nachrichten, die in der Eigenschaft **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)) gespeichert. Wenn Ihre Entwicklungsumgebung ein MAPIDEFS verwendet wird. H-Datei, die nicht STORE_HTML_OK enthalten, verwenden Sie stattdessen den Wert 0 x 00010000. 
    
STORE_ITEMPROC
  
> (2097152, 0x00200000) In einem gepackten PST-Speicher, dass beim Empfang einer neuen Nachricht an den Speicher der Speicher Regeln und Spam-Filter Verarbeitung der Nachricht getrennt aufwendet. Der Informationsspeicher ruft [IMAPISupport::Notify](imapisupport-notify.md), Einstellung **FnevNewMail** in der [Benachrichtigung](notification.md) -Struktur, die als Parameter übergeben wird, und klicken Sie dann die Details der neuen Nachricht an dem listening Client übergibt. Später, wenn der listening Client die Benachrichtigung erhält, verarbeitet es Regeln für die Nachricht nicht. 
    
STORE_LOCALSTORE
  
> (524288, 0x00080000) Dieses Kennzeichen ist reserviert und sollte nicht verwendet werden.
    
STORE_MODIFY_OK 
  
> (8, 0 x 00000008) Der Nachrichtenspeicher unterstützt die Änderung der vorhandenen Nachrichten. 
    
STORE_MV_PROPS_OK 
  
> (512, 0 x 00000200) Der Nachrichtenspeicher mehrwertige Eigenschaften unterstützt, die Stabilität der Reihenfolge der Wert in einer mehrwertigen Eigenschaft in der gesamten Speichervorgang garantiert Vorgang und unterstützt die Instanziierung von mehrwertigen Eigenschaften in Tabellen. 
    
STORE_NOTIFY_OK 
  
> (256, 0 x 00000100) Der Nachrichtenspeicher unterstützt Benachrichtigungen. 
    
STORE_OLE_OK 
  
> (64, 0 x 00000040) Der Nachrichtenspeicher unterstützt OLE-Anlagen. OLE-Daten können über einen **IStorage** -Schnittstelle, z. B., die über die **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md))-Eigenschaft zugegriffen werden. 
    
STORE_PUBLIC_FOLDERS 
  
> (16384, 0x00004000) Der Ordner in diesem Zertifikatspeicher sind öffentliche (mehrere Benutzer) wird nicht private (möglicherweise mit mehreren Instanzen, aber nicht mehrere Benutzer). 
    
STORE_PUSHER_OK
  
> (8388608, 0 x 00800000) Der MAPI-Protokollhandler wird nicht durchforstet werden den Speicher und der Speicher ist verantwortlich für die pushen von Änderungen durch Benachrichtigungen an den Indexer Nachrichten indiziert werden.
    
STORE_READONLY 
  
> (2, 0 x 00000002) Alle Schnittstellen für den Nachrichtenspeicher verfügen über eine nur-Lese-Zugriffsebene. 
    
STORE_RESTRICTION_OK 
  
> (4096, 0 x 00001000) Der Nachrichtenspeicher unterstützt Einschränkungen. 
    
STORE_RTF_OK 
  
> (2048, 0x00000800) Der Nachrichtenspeicher unterstützt Rich Text Format (RTF)-Nachrichten, die in der Regel komprimiert und der Informationsspeicher selbst behält **PR_BODY** **PR_RTF_COMPRESSED** synchronisiert. 
    
STORE_RULES_OK
  
> (268435456, 0 x 10000000) Gibt an, dass Regeln in diesem PST-Speicher gespeichert werden soll, auch wenn es sich nicht um die Standard-Informationsspeichers ist. Wenn **STORE_RULES_OK** in Verbindung mit **NON_EMS_XP_SAVE**verwendet wird, sind Regeln in einem nicht standardmäßigen PST umfließendem Informationsspeicher ausführen können.
    
STORE_SEARCH_OK 
  
> (4, 0 x 00000004) Der Nachrichtenspeicher unterstützt Suchergebnisse Ordner. 
    
STORE_SORT_OK 
  
> (8192, 0 x 00002000) Der Nachrichtenspeicher unterstützt Sortierung Ansichten von Tabellen. 
    
STORE_SUBMIT_OK 
  
> (128, 0x00000080) Der Nachrichtenspeicher unterstützt Markierens einer Nachricht für die Übermittlung. 
    
STORE_UNCOMPRESSED_RTF 
  
> (32768, 0x00008000) Nachrichtenspeicher unterstützt das Speichern von RTF-Nachrichten in nicht komprimierten Format. Ein nicht komprimierter RTF-Stream wird durch den Wert **DwMagicUncompressedRTF** im Streamheader identifiziert. Der Wert **DwMagicUncompressedRTF** ist in der RTFLIB definiert. H-Datei. 
    
STORE_UNICODE_OK
  
> (262144, 0 x 00040000) Gibt an, dass der Nachrichtenspeicher Unicode-Speicher unterstützt. Ein Client kann für das Vorhandensein des Flags entscheiden, ob anfordern oder Unicode-Informationen im Speicher speichern aussehen. 
    
Eine RTF-Version einer Nachricht kann immer gespeichert werden, selbst wenn der Nachrichtenspeicher RTF nicht bekannt ist. Wenn das Bit STORE_RTF_OK für einen bestimmten Speicher nicht festgelegt ist, müssen einen Client RTF-Versionen verwalten die [RTFSync](rtfsync.md) -Funktion, um die **PR_BODY** und **PR_RTF_COMPRESSED** Versionen für Textinhalt synchronisiert halten aufrufen. RTF wird immer in **PR_RTF_COMPRESSED**, gespeichert, ob es tatsächlich oder nicht komprimiert werden. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXMSG]](http://msdn.microsoft.com/library/b046868c-9fbf-41ae-9ffb-8de2bd4eec82%28Office.15%29.aspx)
  
> Beschreibt das Format von Nachrichten, die zum Senden von Informationen im Zusammenhang mit der Freigabe von Ordnern auf dem Client verwendet.
    
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

