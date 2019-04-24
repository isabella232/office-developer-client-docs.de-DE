---
title: Kanonische PidTagDisplayTo-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayTo
api_type:
- HeaderDef
ms.assetid: 700cc03b-5d98-40ce-adb5-a11fdac8aa28
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0c7ae8951b02f099161871b17ff59ea23f8fbcc4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360788"
---
# <a name="pidtagdisplayto-canonical-property"></a>Kanonische PidTagDisplayTo-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Liste der Anzeigenamen der primären (an) Nachrichtenempfänger, getrennt durch Semikolons (;). 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DISPLAY_TO, PR_DISPLAY_TO_A, PR_DISPLAY_TO_W  <br/> |
|Kennung:  <br/> |0x0E04  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Nachricht  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Nachrichtenspeicher berechnet diese Eigenschaften für Nachrichtenobjekte mithilfe der [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) -Methode. Der Nachrichtenspeicher verwaltet diese Eigenschaften auch so, dass er immer den zuletzt gespeicherten Status einer Nachricht widerspiegelt. Der Wert wird bei jedem Aufruf der [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode synchronisiert. 
  
Wenn eine Nachricht keine primären Empfänger hat, sollte der Nachrichtenspeicher auf einen [IMAPIProp::](imapiprop-getprops.md) GetProps-Aufruf mit einem Rückgabewert von S_OK und einer leeren Zeichenfolge für **PR_DISPLAY_TO**reagieren. 
  
Aufgrund der möglichen Lokalisierungsanforderungen bietet MAPI folgende Richtlinien für alle Empfängernamen:
  
- Alle Namen sollten lokalisiert werden können. 
    
- Das Semikolon sollte das Zeichen sein, das zum Trennen von Namen in den **PR_DISPLAY_BCC** ([pidtagdisplaybcc (](pidtagdisplaybcc-canonical-property.md))-, **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))-und **PR_DISPLAY_TO** -Eigenschaften verwendet wird. Innerhalb von Empfängernamen in MAPI sind keine Semikolons zulässig. 
    
- Clients sollten jedes Semikolon, das in der **PR_DISPLAY_TO** und den dazugehörigen Eigenschaften vorliegt, übersetzen, bevor die Informationen auf der Benutzeroberfläche sichtbar gemacht werden. 
    
- Beim Weiterleiten von Nachrichten müssen die Trennzeichen in der primären Empfänger Linie von Clients nicht übersetzt werden. 
    
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

