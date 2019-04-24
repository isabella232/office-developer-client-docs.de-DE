---
title: Kanonische Pidtagdisplaybcc (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 74669d102462e1a825568615d1d30346e99e90a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360816"
---
# <a name="pidtagdisplaybcc-canonical-property"></a>Kanonische Pidtagdisplaybcc (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine ASCII-Liste mit den Anzeigenamen aller BCC-Empfänger (Blind Carbon Copy), die durch Semikolons getrennt sind (;).
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DISPLAY_BCC, PR_DISPLAY_BCC_A, PR_DISPLAY_BCC_W  <br/> |
|Kennung:  <br/> |0x0E02  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Nachricht  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Nachrichtenspeicher berechnet diese Eigenschaften für Nachrichtenobjekte mithilfe der [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) -Methode. Der Nachrichtenspeicher verwaltet diese Eigenschaften auch so, dass er immer den zuletzt gespeicherten Status einer Nachricht widerspiegelt. Der Wert wird bei jedem Aufruf der [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode synchronisiert. 
  
Wenn eine Nachricht keine blinden Kopie-Empfänger hat, sollte der Nachrichtenspeicher auf einen [IMAPIProp::](imapiprop-getprops.md) GetProps-Aufruf mit einem Rückgabewert von S_OK und einer leeren Zeichenfolge für **PR_DISPLAY_BCC**reagieren. 
  
Aufgrund der möglichen Lokalisierungsanforderungen bietet MAPI folgende Richtlinien für alle Empfängernamen:
  
- Alle Namen sollten lokalisiert werden können. 
    
- Das Semikolon sollte das Zeichen sein, das zum Trennen von Namen in den Eigenschaften **PR_DISPLAY_BCC**, **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) und **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) verwendet wird. Innerhalb von Empfängernamen in MAPI sind keine Semikolons zulässig. 
    
- Clients sollten jedes Semikolon, das in dieser Eigenschaft vorliegt, in ein lokalisiertes Trennzeichen übersetzen, bevor die Eigenschaftsinformationen auf der Benutzeroberfläche sichtbar gemacht werden. 
    
- Beim Weiterleiten von Nachrichten müssen die Trennzeichen in der Empfänger Linie für die Blindkopie nicht übersetzt werden. 
    
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Beschreibt das Format der Nachrichten, die zum Senden von Informationen im Zusammenhang mit Freigabeordnern auf dem Client verwendet werden.
    
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

