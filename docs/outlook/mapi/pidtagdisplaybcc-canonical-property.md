---
title: PidTagDisplayBcc (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayBcc
api_type:
- HeaderDef
ms.assetid: ab5bcd67-d54e-46e9-b94e-a652aac3e81c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 74669d102462e1a825568615d1d30346e99e90a6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388259"
---
# <a name="pidtagdisplaybcc-canonical-property"></a>PidTagDisplayBcc (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Liste ASCII, der den Anzeigenamen der alle blind Carbon Copy, Blindkopie (BCC) Empfänger der Nachricht, durch Semikolons (;) voneinander getrennt sind.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DISPLAY_BCC, PR_DISPLAY_BCC_A, PR_DISPLAY_BCC_W  <br/> |
|Kennung:  <br/> |0x0E02  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Nachricht  <br/> |
   
## <a name="remarks"></a>Hinweise

Der Nachrichtenspeicher berechnet diese Eigenschaften für Nachrichtenobjekte, die mit der [IMessage::ModifyRecipients](imessage-modifyrecipients.md) -Methode. Der Nachrichtenspeicher verwaltet auch diese Eigenschaften, sodass es immer den letzten gespeicherten Zustand einer Nachricht widerspiegelt. Zeitpunkt der jeder Aufruf der [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode wird der Wert synchronisiert. 
  
Wenn eine Nachricht keine Bcc-Empfänger enthält, sollte einen [IMAPIProp::GetProps](imapiprop-getprops.md) Anruf mit der Rückgabewert S_OK und eine leere Zeichenfolge für **PR_DISPLAY_BCC**des Nachrichtenspeichers beantworten. 
  
Aufgrund der möglichen Notwendigkeit Lokalisierung bietet MAPI diese Richtlinien für alle Empfängernamen:
  
- Alle Namen sollte lokalisiert werden können. 
    
- Das Semikolon sollte das Zeichen, mit dem Namen in der **PR_DISPLAY_BCC**, **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) und Eigenschaften **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) zu trennen. Semikolons dürfen nicht innerhalb von Empfängernamen in MAPI. 
    
- Clients sollte jedem Semikolon in dieser Eigenschaft auf eine lokalisierte Trennzeichen aufgetreten ist, bevor Informationen über die Eigenschaft in der Benutzeroberfläche sichtbar gemacht übersetzen. 
    
- Beim Weiterleiten von Nachrichten müssen Clients nicht die Trennzeichen in der Empfänger Bcc-Zeile übersetzen. 
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
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

