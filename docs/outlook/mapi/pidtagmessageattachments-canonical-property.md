---
title: PidTagMessageAttachments (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagMessageAttachments
api_type:
- HeaderDef
ms.assetid: 85762771-b823-4227-9a7b-75b6ac280b2d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e01c5aacef78bbe911ec989c043de1cd0c5eb5fd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587489"
---
# <a name="pidtagmessageattachments-canonical-property"></a>PidTagMessageAttachments (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Tabelle mit Anlagen für eine Nachricht. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_MESSAGE_ATTACHMENTS  <br/> |
|Kennung:  <br/> |0x0E13  <br/> |
|Datentyp:  <br/> |PT_OBJECT  <br/> |
|Bereich:  <br/> |Nachrichtenanlage  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft kann in [IMAPIProp::CopyTo-Operationen](imapiprop-copyto.md) oder in [IMAPIProp::CopyProps-Operationen](imapiprop-copyprops.md) ausgeschlossen werden. Als Eigenschaft vom Typ PT_OBJECT kann sie nicht erfolgreich von der [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) abgerufen werden. Der Zugriff auf den Inhalt sollte über die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) erfolgen, die den **IID_IMAPITable** Schnittstellenbezeichner anfordert. Dienstanbieter müssen sie an die [IMAPIProp::GetPropList-Methode](imapiprop-getproplist.md) melden, wenn sie festgelegt ist, können sie aber optional melden oder nicht, wenn sie nicht festgelegt ist. 
  
Zum Abrufen von Tabelleninhalten sollte eine Clientanwendung die [IMessage::GetAttachmentTable-Methode](imessage-getattachmenttable.md) aufrufen. For more information, see [Anlagentabellen](attachment-tables.md). 
  
Diese Eigenschaft kann für die Unterobjekteinschränkung verwendet werden, indem sie in der [SSubRestriction-Struktur](ssubrestriction.md) angegeben wird. Dadurch kann der Client die Ansicht eines Containers auf Nachrichten beschränken, deren Anlagen bestimmte Kriterien erfüllen. Eine Nachricht ist für die Anzeige qualifiziert, wenn mindestens eine Zeile in der Anlagentabelle, d. h. eine Anlage, die Einschränkung des Unterobjekts erfüllt. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)
  
> Definiert die grundlegenden Datenstrukturen, die in Remotevorgängen verwendet werden.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Definiert die grundlegenden Datenstrukturen, die in Remotevorgängen verwendet werden.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Konvertiert zwischen IETF RFC2445, RFC2446 und RFC2447 sowie Termin- und Besprechungsobjekten.
    
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

