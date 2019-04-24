---
title: Kanonische Pidtagmessageattachments (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageAttachments
api_type:
- HeaderDef
ms.assetid: 85762771-b823-4227-9a7b-75b6ac280b2d
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 975f52e6ea0ca7a469a027565f845f9dc0f9c2cf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342567"
---
# <a name="pidtagmessageattachments-canonical-property"></a>Kanonische Pidtagmessageattachments (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Tabelle mit Anlagen für eine Nachricht. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_MESSAGE_ATTACHMENTS  <br/> |
|Kennung:  <br/> |0x0E13  <br/> |
|Datentyp:  <br/> |PT_OBJECT  <br/> |
|Bereich:  <br/> |Nachrichtenanlage  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft kann in [IMAPIProp:: CopyTo](imapiprop-copyto.md) -Vorgängen oder in [IMAPIProp:: CopyProps](imapiprop-copyprops.md) -Vorgängen ausgeschlossen werden. Als Eigenschaft vom Typ PT_OBJECT kann Sie nicht erfolgreich von der [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode abgerufen werden. Auf den Inhalt sollte von der [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode zugegriffen werden, um den **IID_IMAPITable** -Schnittstellenbezeichner anzufordern. Dienstanbieter müssen Sie an die [IMAPIProp::](imapiprop-getproplist.md) getproplist-Methode melden, wenn Sie festgelegt ist, aber Sie kann Sie optional melden oder nicht, wenn Sie nicht festgelegt ist. 
  
Zum Abrufen von Tabelleninhalten sollte eine Clientanwendung die [IMessage::](imessage-getattachmenttable.md) getattachmentable-Methode aufrufen. For more information, see [Anlagentabellen](attachment-tables.md). 
  
Diese Eigenschaft kann für SubObject-Einschränkungen verwendet werden, indem Sie Sie in der [SSubRestriction](ssubrestriction.md) -Struktur angibt. Dadurch kann der Client die Ansicht eines Containers auf Nachrichten mit Anlagen begrenzen, die bestimmte Kriterien erfüllen. Eine Nachricht kann angezeigt werden, wenn mindestens eine Zeile in der Attachments-Tabelle, also eine Anlage, der SubObject-Einschränkung entspricht. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)
  
> Definiert die grundlegenden Datenstrukturen, die in Remotevorgängen verwendet werden.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Definiert die grundlegenden Datenstrukturen, die in Remotevorgängen verwendet werden.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Konvertiert zwischen IETF-RFC2445, RFC2446 und RFC2447 sowie Termin-und Besprechungs Objekten.
    
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

