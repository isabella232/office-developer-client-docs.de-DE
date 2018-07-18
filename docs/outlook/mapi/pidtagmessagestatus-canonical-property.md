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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 21336e158d21bba6c7204eb446df3efc80b70e46
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794622"
---
# <a name="pidtagmessagestatus-canonical-property"></a>PidTagMessageStatus (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Enthält eine 32-Bit-Bitmaske aus Flags, die den Status einer Nachricht in einer Inhaltstabelle definiert. 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_MSG_STATUS  <br/> |
|Bezeichner:  <br/> |0x0E17  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Allgemeine messaging  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Eine Nachricht kann in einer Inhaltstabelle und in eine oder mehrere Suchergebnisse Tabellen vorhanden sein, und jede Instanz der Nachricht kann einen anderen Status aufweisen. Diese Eigenschaft sollten keine-Eigenschaft für eine Nachricht aber eine Spalte in einer Inhaltstabelle berücksichtigt werden. 
  
In dieser Eigenschaft kann in eine anderen Clientanwendung eine oder mehrere der folgenden Werte festlegen: 
  
MSGSTATUS_ANSWERED 
  
> Die Nachricht wurde beantwortet. 
    
MSGSTATUS_DELMARKED 
  
> Die Nachricht wurde für nachfolgende löschen markiert. 
    
MSGSTATUS_DRAFT 
  
> Die Nachricht ist im Revision-Entwurfsstatus. 
    
MSGSTATUS_HIDDEN 
  
> Die Nachricht wird vom Empfänger Ordner zeigt unterdrückt werden soll. 
    
MSGSTATUS_HIGHLIGHTED 
  
> Die Nachricht ist in zeigt der Empfänger Ordner hervorgehoben wird. 
    
MSGSTATUS_REMOTE_DELETE 
  
> Die Nachricht wurde zum Löschen auf die entfernten Nachrichtenspeicher markiert, ohne dass auf dem lokalen Client heruntergeladen. 
    
MSGSTATUS_REMOTE_DOWNLOAD 
  
> Die Nachricht wurde für das Herunterladen aus dem remote Nachrichtenspeicher auf dem lokalen Client markiert. 
    
MSGSTATUS_TAGGED 
  
> Für einen Client definierten Zweck hat die Nachricht markiert wurde.
    
Vom Client werden die Kennzeichen **MSGSTATUS_DELMARKED**, **MSGSTATUS_HIDDEN**, **MSGSTATUS_HIGHLIGHTED**und **MSGSTATUS_TAGGED** definiert. Transport- und -Anbieter übergeben Sie diese Bits ohne Aktion. 
  
Clients können diese Werte in irgendeiner Weise interpretieren, die für ihre Anwendung geeignet ist. Eine Möglichkeit, dass viele Clients verwenden Sie diese Eigenschaft ist zum Anzeigen von Nachrichten, die für die Löschung mit einem repräsentative Symbol gekennzeichnet. 
  
Ein remote-Viewer-Client kann **MSGSTATUS_REMOTE_DELETE** oder **MSGSTATUS_REMOTE_DOWNLOAD** für Nachrichten im Ordner "Kopfzeile" vom Transportanbieter remote vorgelegte festlegen. Die Client-Anwendung kann untersuchen, jeden Nachrichtenkopf in diesem Ordner, um zu bestimmen, ob die Nachricht an die entfernten Nachrichtenspeicher gelöscht oder heruntergeladen werden soll. Anschließend wird die [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) -Methode auf das entsprechende Flag festgelegt. **SetMessageStatus** ist die einzige Möglichkeit, einen der Werte in dieser Eigenschaft festzulegen. die [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode kann nicht verwendet werden. Um diese Eigenschaft abzurufen, rufen Clients [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) statt [IMAPIProp::GetProps](imapiprop-getprops.md).
  
Bits 16 bis 31 (0 x 10000 über 0 x 80000000) dieser Eigenschaft sind für die Verwendung durch die Clientanwendung zwischen Personen Nachricht (IPM) verfügbar. Alle anderen Bits sind MAPI für die Verwendung reserviert. nicht in der obigen Tabelle definiert sollte anfänglich auf 0 (null) festgelegt und anschließend nicht geändert werden. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Synchronisieren von messaging Objektdaten zwischen einem Server und einem Client behandelt.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[IMAPITable::QueryRows](imapitable-queryrows.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

