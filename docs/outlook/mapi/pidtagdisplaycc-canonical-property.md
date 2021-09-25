---
title: PidTagDisplayCc (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDisplayCc
api_type:
- HeaderDef
ms.assetid: 00377e78-a208-4942-a7a6-893b2a71ab0b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3dcdcdcbcc8b6d8ece3cfc0bff31253bfe6f1f20
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600176"
---
# <a name="pidtagdisplaycc-canonical-property"></a>PidTagDisplayCc (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine ASCII-Liste der Anzeigenamen aller Cc-Nachrichtenempfänger (Carbon Copy), getrennt durch Semikolons (;). 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DISPLAY_CC, PR_DISPLAY_CC_A, PR_DISPLAY_CC_W  <br/> |
|Kennung:  <br/> |0x0E03  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Nachricht  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Der Nachrichtenspeicher berechnet diese Eigenschaften für Nachrichtenobjekte mithilfe der [IMessage::ModifyRecipients-Methode.](imessage-modifyrecipients.md) Der Nachrichtenspeicher verwaltet diese Eigenschaften auch so, dass er immer den letzten gespeicherten Status einer Nachricht widerspiegelt. Der Wert wird zum Zeitpunkt jedes Aufrufs von [IMAPIProp::SaveChanges](imapiprop-savechanges.md)synchronisiert. 
  
Wenn eine Nachricht keine Empfänger von Kopie hat, sollte der Nachrichtenspeicher auf einen [IMAPIProp::GetProps-Aufruf](imapiprop-getprops.md) mit dem Rückgabewert S_OK und einer leeren Zeichenfolge für diese Eigenschaften antworten. 
  
Aufgrund der möglichen Notwendigkeit der Lokalisierung stellt MAPI diese Richtlinien für alle Empfängernamen bereit:
  
- Alle Namen sollten lokalisiert werden können. 
    
- Das Semikolon sollte das Zeichen sein, das zum Trennen von Namen in den **Eigenschaften PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC** und **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) verwendet wird. Semikolons sind innerhalb von Empfängernamen in MAPI nicht zulässig. 
    
- Clients sollten jedes in dieser Eigenschaft auftretende Semikolon in ein lokalisiertes Trennzeichen übersetzen, bevor die Eigenschafteninformationen auf der Benutzeroberfläche sichtbar werden. 
    
- Beim Weiterleiten von Nachrichten müssen Clients die Trennzeichen in der Empfängerzeile der Kopie nicht übersetzen. 
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.
    
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

