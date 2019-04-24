---
title: Kanonische Pidtagmessagestatus (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageStatus
api_type:
- HeaderDef
ms.assetid: e479e863-a8de-4f7e-9eae-3f721cd16e9a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: dacd759d978394a5f4ed028915ed1c717bf6efe5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355720"
---
# <a name="pidtagmessagestatus-canonical-property"></a>Kanonische Pidtagmessagestatus (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine 32-Bit-Bitmaske von Flags, die den Status einer Nachricht in einer Inhaltstabelle definiert. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_MSG_STATUS  <br/> |
|Kennung:  <br/> |0x0E17  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Allgemeine Nachrichtenübermittlung  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Eine Nachricht kann in einer Inhaltstabelle und in einer oder mehreren Suchergebnis Tabellen vorhanden sein, und jede Instanz der Nachricht kann einen anderen Status aufweisen. Diese Eigenschaft sollte nicht als Eigenschaft einer Nachricht, sondern als eine Spalte in einer Inhaltstabelle betrachtet werden. 
  
Eine Clientanwendung kann eine oder mehrere der folgenden Flags in dieser Eigenschaft festlegen: 
  
MSGSTATUS_ANSWERED 
  
> Die Nachricht wurde beantwortet. 
    
MSGSTATUS_DELMARKED 
  
> Die Nachricht wurde zum späteren Löschen markiert. 
    
MSGSTATUS_DRAFT 
  
> Die Nachricht befindet sich im Entwurfsstatus der Revision. 
    
MSGSTATUS_HIDDEN 
  
> Die Nachricht soll aus dem Ordner des Empfängers angezeigt werden. 
    
MSGSTATUS_HIGHLIGHTED 
  
> Die Nachricht soll im Ordner des Empfängers hervorgehoben werden. 
    
MSGSTATUS_REMOTE_DELETE 
  
> Die Nachricht wurde zum Löschen im Remotenachrichtenspeicher markiert, ohne Sie auf den lokalen Client herunterzuladen. 
    
MSGSTATUS_REMOTE_DOWNLOAD 
  
> Die Nachricht wurde zum Herunterladen aus dem Remotenachrichtenspeicher auf den lokalen Client markiert. 
    
MSGSTATUS_TAGGED 
  
> Die Nachricht wurde für einen Client definierten Zweck markiert.
    
Die **MSGSTATUS_DELMARKED**-, **MSGSTATUS_HIDDEN**-, **MSGSTATUS_HIGHLIGHTED**-und **MSGSTATUS_TAGGED** -Flags werden vom Client definiert. Transport-und Speicheranbieter führen diese Bits ohne Aktion aus. 
  
Clients können diese Werte auf eine beliebige Weise interpretieren, die für Ihre Anwendungen geeignet ist. Eine Möglichkeit, die diese Eigenschaft für viele Clients verwendet wird, ist das Anzeigen von zum Löschen markierten Nachrichten mit einem repräsentativen Symbol. 
  
Ein Remoteanzeige Client kann **MSGSTATUS_REMOTE_DELETE** oder **MSGSTATUS_REMOTE_DOWNLOAD** für Nachrichten im Überschriften Ordner festlegen, der vom Remote Transportanbieter angezeigt wird. Die Clientanwendung kann jeden Nachrichtenkopf in diesem Ordner überprüfen, um zu bestimmen, ob die Nachricht im Remotenachrichtenspeicher heruntergeladen oder gelöscht werden soll. Anschließend wird die [IMAPIFolder:: SetMessageStatus](imapifolder-setmessagestatus.md) -Methode verwendet, um das entsprechende Flag festzulegen. **SetMessageStatus** ist die einzige Möglichkeit, die Flags in dieser Eigenschaft festzulegen. die [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode kann nicht verwendet werden. Um diese Eigenschaft abzurufen, rufen die Clients [IMAPIFolder:: GetMessageStatus](imapifolder-getmessagestatus.md) anstelle von [IMAPIProp::](imapiprop-getprops.md)GetProps auf.
  
Die Bits 16 bis 31 (0x10000 bis 0x80000000) dieser Eigenschaft stehen für die Clientanwendung für die zwischenmenschlichen Nachrichten (IPM) zur Verfügung. Alle anderen Bits sind für die Verwendung durch MAPI reserviert; diejenigen, die nicht in der obigen Tabelle definiert sind, sollten anfänglich auf NULL festgelegt werden und nicht nachträglich geändert werden. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Behandelt das Synchronisieren von Messagingobjekt Daten zwischen einem Server und einem Client.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[IMAPITable::QueryRows](imapitable-queryrows.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

