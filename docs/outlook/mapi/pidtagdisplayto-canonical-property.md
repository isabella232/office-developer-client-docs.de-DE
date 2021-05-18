---
title: PidTagDisplayTo (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0c7ae8951b02f099161871b17ff59ea23f8fbcc4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360788"
---
# <a name="pidtagdisplayto-canonical-property"></a>PidTagDisplayTo (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Liste der Anzeigenamen der primären (An)-Nachrichtenempfänger, getrennt durch Semikolons (;). 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DISPLAY_TO, PR_DISPLAY_TO_A, PR_DISPLAY_TO_W  <br/> |
|Kennung:  <br/> |0x0E04  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Message  <br/> |
   
## <a name="remarks"></a>Hinweise

Der Nachrichtenspeicher berechnet diese Eigenschaften für Nachrichtenobjekte mithilfe der [IMessage::ModifyRecipients-Methode.](imessage-modifyrecipients.md) Der Nachrichtenspeicher behält diese Eigenschaften auch bei, sodass er immer den letzten gespeicherten Status einer Nachricht widerspiegelt. Der Wert wird bei jedem Aufruf der [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) synchronisiert. 
  
Wenn eine Nachricht keine primären Empfänger hat, sollte der Nachrichtenspeicher auf einen [IMAPIProp::GetProps-Aufruf](imapiprop-getprops.md) mit dem Rückgabewert S_OK und einer leeren Zeichenfolge für PR_DISPLAY_TO **.** 
  
Aufgrund des möglichen Lokalisierungsbedarfs bietet MAPI die folgenden Richtlinien für alle Empfängernamen:
  
- Alle Namen sollten lokalisiert werden können. 
    
- Das Semikolon sollte das Zeichen sein, das zum Trennen von Namen in den Eigenschaften **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) und **PR_DISPLAY_TO** wird. Semikolons sind innerhalb von Empfängernamen in MAPI nicht zulässig. 
    
- Clients sollten jedes Semikolon,  das in der PR_DISPLAY_TO und zugehörigen Eigenschaften auftritt, in ein lokalisiertes Trennzeichen übersetzen, bevor die Informationen auf der Benutzeroberfläche angezeigt werden. 
    
- Beim Weiterleiten von Nachrichten müssen Clients die Trennzeichen in der primären Empfängerzeile nicht übersetzen. 
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.
    
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

