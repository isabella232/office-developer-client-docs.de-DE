---
title: PidTagMessageStatus (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: dacd759d978394a5f4ed028915ed1c717bf6efe5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355720"
---
# <a name="pidtagmessagestatus-canonical-property"></a>PidTagMessageStatus (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine 32-Bit-Bitmaske mit Flags, die den Status einer Nachricht in einer Inhaltstabelle definiert. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_MSG_STATUS  <br/> |
|Kennung:  <br/> |0x0E17  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Allgemeines Messaging  <br/> |
   
## <a name="remarks"></a>Hinweise

Eine Nachricht kann in einer Inhaltstabelle und in einer oder mehreren Suchergebnissen vorhanden sein, und jede Instanz der Nachricht kann einen anderen Status haben. Diese Eigenschaft sollte nicht als Eigenschaft für eine Nachricht, sondern als Spalte in einer Inhaltstabelle betrachtet werden. 
  
Eine Clientanwendung kann mindestens eines der folgenden Kennzeichen in dieser Eigenschaft festlegen: 
  
MSGSTATUS_ANSWERED 
  
> Die Nachricht wurde beantwortet. 
    
MSGSTATUS_DELMARKED 
  
> Die Nachricht wurde für das nachfolgende Löschen markiert. 
    
MSGSTATUS_DRAFT 
  
> Die Nachricht befindet sich im Entwurfsrevisionsstatus. 
    
MSGSTATUS_HIDDEN 
  
> Die Nachricht soll aus den Ordneranzeigen der Empfänger unterdrückt werden. 
    
MSGSTATUS_HIGHLIGHTED 
  
> Die Nachricht soll in den Anzeigeordnern der Empfänger hervorgehoben werden. 
    
MSGSTATUS_REMOTE_DELETE 
  
> Die Nachricht wurde zum Löschen im Remotenachrichtenspeicher ohne Download auf den lokalen Client markiert. 
    
MSGSTATUS_REMOTE_DOWNLOAD 
  
> Die Nachricht wurde zum Herunterladen aus dem Remotenachrichtenspeicher auf den lokalen Client markiert. 
    
MSGSTATUS_TAGGED 
  
> Die Nachricht wurde für einen clientdefinierten Zweck markiert.
    
Die **MSGSTATUS_DELMARKED**, **MSGSTATUS_HIDDEN**, **MSGSTATUS_HIGHLIGHTED** und **MSGSTATUS_TAGGED** werden vom Client definiert. Transport- und Speicheranbieter übergeben diese Bits ohne Aktion. 
  
Clients können diese Werte auf eine für ihre Anwendungen geeignete Weise interpretieren. Eine Möglichkeit, mit der viele Clients diese Eigenschaft verwenden, besteht in der Anzeige von Nachrichten, die zum Löschen mit einem repräsentativen Symbol markiert sind. 
  
Ein Remote-Viewer-Client kann **MSGSTATUS_REMOTE_DELETE** oder **MSGSTATUS_REMOTE_DOWNLOAD** Nachrichten im Headerordner festlegen, der vom Remotetransportanbieter angezeigt wird. Die Clientanwendung kann jeden Nachrichtenkopf in diesem Ordner untersuchen, um zu bestimmen, ob die Nachricht im Remotenachrichtenspeicher heruntergeladen oder gelöscht werden soll. Anschließend wird die [IMAPIFolder::SetMessageStatus-Methode](imapifolder-setmessagestatus.md) verwendet, um das entsprechende Flag zu setzen. **SetMessageStatus** ist die einzige Möglichkeit zum Festlegen von Flags in dieser Eigenschaft. die [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) kann nicht verwendet werden. Zum Abrufen dieser Eigenschaft rufen Clients [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) statt [IMAPIProp::GetProps auf.](imapiprop-getprops.md)
  
Die Bits 16 bis 31 (0x10000 bis 0x80000000) dieser Eigenschaft stehen für die Verwendung durch die Clientanwendung für zwischenpersonelle Nachrichten (IPM) zur Verfügung. Alle anderen Bits sind für die Verwendung durch MAPI reserviert. Diejenigen, die in der vorherigen Tabelle nicht definiert sind, sollten zunächst auf Null festgelegt und anschließend nicht geändert werden. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Behandelt die Synchronisierung von Messagingobjektdaten zwischen einem Server und einem Client.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[IMAPITable::QueryRows](imapitable-queryrows.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

