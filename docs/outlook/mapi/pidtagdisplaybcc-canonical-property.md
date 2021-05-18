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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360816"
---
# <a name="pidtagdisplaybcc-canonical-property"></a>PidTagDisplayBcc (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine ASCII-Liste der Anzeigenamen aller BCC(Blind Carbon Copy)-Nachrichtenempfänger, getrennt durch Semikolons (;).
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DISPLAY_BCC, PR_DISPLAY_BCC_A, PR_DISPLAY_BCC_W  <br/> |
|Kennung:  <br/> |0x0E02  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Message  <br/> |
   
## <a name="remarks"></a>Hinweise

Der Nachrichtenspeicher berechnet diese Eigenschaften für Nachrichtenobjekte mithilfe der [IMessage::ModifyRecipients-Methode.](imessage-modifyrecipients.md) Der Nachrichtenspeicher behält diese Eigenschaften auch bei, sodass er immer den letzten gespeicherten Status einer Nachricht widerspiegelt. Der Wert wird bei jedem Aufruf der [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) synchronisiert. 
  
Wenn eine Nachricht keine Blindkopieempfänger hat, sollte der Nachrichtenspeicher auf einen [IMAPIProp::GetProps-Aufruf](imapiprop-getprops.md) mit dem Rückgabewert S_OK und einer leeren Zeichenfolge für PR_DISPLAY_BCC **.** 
  
Aufgrund des möglichen Lokalisierungsbedarfs bietet MAPI die folgenden Richtlinien für alle Empfängernamen:
  
- Alle Namen sollten lokalisiert werden können. 
    
- Das Semikolon sollte das Zeichen **sein,** das zum Trennen von Namen in den Eigenschaften PR_DISPLAY_BCC , **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) und **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) verwendet wird. Semikolons sind innerhalb von Empfängernamen in MAPI nicht zulässig. 
    
- Clients sollten jedes in dieser Eigenschaft gefundene Semikolon in ein lokalisiertes Trennzeichen übersetzen, bevor die Eigenschaftsinformationen auf der Benutzeroberfläche angezeigt werden. 
    
- Beim Weiterleiten von Nachrichten müssen Clients die Trennzeichen in der Empfängerzeile für blinde Kopiekopien nicht übersetzen. 
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Beschreibt das Format von Nachrichten, die zum Senden von Informationen im Zusammenhang mit Freigabeordnern auf dem Client verwendet werden.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

