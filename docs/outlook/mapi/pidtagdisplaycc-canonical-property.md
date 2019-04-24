---
title: Kanonische PidTagDisplayCc-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2bf862317ca1d2f2a09a71e1af62b82661b33326
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360809"
---
# <a name="pidtagdisplaycc-canonical-property"></a>Kanonische PidTagDisplayCc-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine ASCII-Liste mit den Anzeigenamen aller CC-Empfänger, getrennt durch Semikolons (;). 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DISPLAY_CC, PR_DISPLAY_CC_A, PR_DISPLAY_CC_W  <br/> |
|Kennung:  <br/> |0x0E03  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Nachricht  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Nachrichtenspeicher berechnet diese Eigenschaften für Nachrichtenobjekte mithilfe der [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) -Methode. Der Nachrichtenspeicher verwaltet diese Eigenschaften auch so, dass er immer den zuletzt gespeicherten Status einer Nachricht widerspiegelt. Der Wert wird bei jedem Aufruf von [IMAPIProp:: SaveChanges](imapiprop-savechanges.md)synchronisiert. 
  
Wenn eine Nachricht keine CC-Empfänger hat, sollte der Nachrichtenspeicher auf einen [IMAPIProp::](imapiprop-getprops.md) GetProps-Aufruf mit einem Rückgabewert von S_OK und einer leeren Zeichenfolge für diese Eigenschaften reagieren. 
  
Aufgrund der möglichen Lokalisierungsanforderungen bietet MAPI folgende Richtlinien für alle Empfängernamen:
  
- Alle Namen sollten lokalisiert werden können. 
    
- Das Semikolon sollte das Zeichen sein, das zum Trennen von Namen in den Eigenschaften **PR_DISPLAY_BCC** ([Pidtagdisplaybcc (](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC**und **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) verwendet wird. Innerhalb von Empfängernamen in MAPI sind keine Semikolons zulässig. 
    
- Clients sollten jedes Semikolon, das in dieser Eigenschaft vorliegt, in ein lokalisiertes Trennzeichen übersetzen, bevor die Eigenschaftsinformationen auf der Benutzeroberfläche sichtbar gemacht werden. 
    
- Beim Weiterleiten von Nachrichten müssen die Trennzeichen in der Empfänger Linie für den CC nicht übersetzt werden. 
    
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.
    
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

