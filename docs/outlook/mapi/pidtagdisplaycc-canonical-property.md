---
title: PidTagDisplayCc (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayCc
api_type:
- HeaderDef
ms.assetid: 00377e78-a208-4942-a7a6-893b2a71ab0b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3d27ad5fbc02e3883d6f74129323165394c4cf2b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577730"
---
# <a name="pidtagdisplaycc-canonical-property"></a>PidTagDisplayCc (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält eine Liste ASCII, der den Anzeigenamen der alle Carbon Copy, Kopie (CC) Empfänger der Nachricht, durch Semikolons (;) voneinander getrennt sind. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DISPLAY_CC, PR_DISPLAY_CC_A, PR_DISPLAY_CC_W  <br/> |
|Kennung:  <br/> |0x0E03  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Nachricht  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Der Nachrichtenspeicher berechnet diese Eigenschaften für Nachrichtenobjekte, die mit der [IMessage::ModifyRecipients](imessage-modifyrecipients.md) -Methode. Der Nachrichtenspeicher verwaltet auch diese Eigenschaften, sodass es immer den letzten gespeicherten Zustand einer Nachricht widerspiegelt. Der Wert wird zum Zeitpunkt der jedem Aufruf von [IMAPIProp::SaveChanges](imapiprop-savechanges.md)synchronisiert. 
  
Wenn eine Nachricht keine Cc-Empfänger enthält, sollte einen [IMAPIProp::GetProps](imapiprop-getprops.md) Anruf mit der Rückgabewert S_OK und eine leere Zeichenfolge für diese Eigenschaften des Nachrichtenspeichers beantworten. 
  
Aufgrund der möglichen Notwendigkeit Lokalisierung bietet MAPI diese Richtlinien für alle Empfängernamen:
  
- Alle Namen sollte lokalisiert werden können. 
    
- Das Semikolon sollte das Zeichen, mit dem Namen in der **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC**und Eigenschaften **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) zu trennen. Semikolons dürfen nicht innerhalb von Empfängernamen in MAPI. 
    
- Clients sollte jedem Semikolon in dieser Eigenschaft auf eine lokalisierte Trennzeichen aufgetreten ist, bevor Informationen über die Eigenschaft in der Benutzeroberfläche sichtbar gemacht übersetzen. 
    
- Beim Weiterleiten von Nachrichten müssen Clients nicht die Trennzeichen in der Zeile an Empfänger Carbon Copy, Blindkopie übersetzen. 
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.
    
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

