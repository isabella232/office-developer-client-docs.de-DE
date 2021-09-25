---
title: PidTagMessageStatus (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagMessageStatus
api_type:
- HeaderDef
ms.assetid: e479e863-a8de-4f7e-9eae-3f721cd16e9a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 11abc17f25324b230dafc2ba1a53be78c54153b2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59555321"
---
# <a name="pidtagmessagestatus-canonical-property"></a>PidTagMessageStatus (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine 32-Bit-Bitmaske mit Flags, die den Status einer Nachricht in einem Inhaltsverzeichnis definiert. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_MSG_STATUS  <br/> |
|Kennung:  <br/> |0x0E17  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Allgemeines Messaging  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Eine Nachricht kann in einer Inhaltstabelle und in einer oder mehreren Suchergebnissen vorhanden sein, und jede Instanz der Nachricht kann einen anderen Status aufweisen. Diese Eigenschaft sollte nicht als Eigenschaft für eine Nachricht, sondern als Spalte in einem Inhaltsverzeichnis betrachtet werden. 
  
Eine Clientanwendung kann eines oder mehrere der folgenden Flags in dieser Eigenschaft festlegen: 
  
MSGSTATUS_ANSWERED 
  
> Auf die Nachricht wurde geantwortet. 
    
MSGSTATUS_DELMARKED 
  
> Die Nachricht wurde für den nachfolgenden Löschvorgang markiert. 
    
MSGSTATUS_DRAFT 
  
> Die Nachricht befindet sich im Überarbeitungsstatus des Entwurfs. 
    
MSGSTATUS_HIDDEN 
  
> Die Nachricht soll aus dem Ordner des Empfängers unterdrückt werden. 
    
MSGSTATUS_HIGHLIGHTED 
  
> Die Nachricht soll in den Ordnern der Empfänger hervorgehoben werden. 
    
MSGSTATUS_REMOTE_DELETE 
  
> Die Nachricht wurde für den Löschvorgang im Remotenachrichtenspeicher markiert, ohne sie auf den lokalen Client herunterzuladen. 
    
MSGSTATUS_REMOTE_DOWNLOAD 
  
> Die Nachricht wurde zum Herunterladen aus dem Remotenachrichtenspeicher auf den lokalen Client markiert. 
    
MSGSTATUS_TAGGED 
  
> Die Nachricht wurde für einen clientdefinierten Zweck markiert.
    
Die Flags **MSGSTATUS_DELMARKED,** **MSGSTATUS_HIDDEN,** **MSGSTATUS_HIGHLIGHTED** und **MSGSTATUS_TAGGED** werden vom Client definiert. Transport- und Speicheranbieter übergeben diese Bits ohne Aktion. 
  
Clients können diese Werte auf beliebige Weise interpretieren, die für ihre Anwendungen geeignet ist. Eine Möglichkeit, wie viele Clients diese Eigenschaft verwenden, ist das Anzeigen von Nachrichten, die zum Löschen mit einem repräsentativen Symbol gekennzeichnet sind. 
  
Ein Remoteanzeigeclient kann **MSGSTATUS_REMOTE_DELETE** oder **MSGSTATUS_REMOTE_DOWNLOAD** für Nachrichten im Headerordner festlegen, die ihm vom Remote-Transportanbieter angezeigt werden. Die Clientanwendung kann jeden Nachrichtenkopf in diesem Ordner überprüfen, um festzustellen, ob die Nachricht im Remotenachrichtenspeicher heruntergeladen oder gelöscht werden soll. Anschließend wird die [IMAPIFolder::SetMessageStatus-Methode](imapifolder-setmessagestatus.md) verwendet, um das entsprechende Flag festzulegen. **SetMessageStatus** ist die einzige Möglichkeit, eines der Flags in dieser Eigenschaft festzulegen. die [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) kann nicht verwendet werden. Zum Abrufen dieser Eigenschaft rufen Clients [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) anstelle von [IMAPIProp::GetProps auf.](imapiprop-getprops.md)
  
Die Bits 16 bis 31 (0x10000 bis 0x80000000) dieser Eigenschaft sind für die Verwendung durch die IPM-Clientanwendung (Interpersonal Message) verfügbar. Alle anderen Bits sind für die Verwendung durch MAPI reserviert. Diejenigen, die nicht in der vorherigen Tabelle definiert sind, sollten anfänglich auf Null festgelegt und anschließend nicht geändert werden. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Behandelt die Synchronisierung von Nachrichtenobjektdaten zwischen einem Server und einem Client.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[IMAPITable::QueryRows](imapitable-queryrows.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

