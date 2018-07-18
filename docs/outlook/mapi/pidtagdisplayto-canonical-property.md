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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d83683fded6a650a947caa7119d138f6f4105e1b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794329"
---
# <a name="pidtagdisplayto-canonical-property"></a>PidTagDisplayTo (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Enthält eine Liste der den Anzeigenamen der primären (Empfänger der Nachricht, durch Semikolons (;) voneinander getrennt sind To). 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_DISPLAY_TO, PR_DISPLAY_TO_A, PR_DISPLAY_TO_W  <br/> |
|Bezeichner:  <br/> |0x0E04  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Nachricht  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Nachrichtenspeicher berechnet diese Eigenschaften für Nachrichtenobjekte, die mit der [IMessage::ModifyRecipients](imessage-modifyrecipients.md) -Methode. Der Nachrichtenspeicher verwaltet auch diese Eigenschaften, sodass es immer den letzten gespeicherten Zustand einer Nachricht widerspiegelt. Zeitpunkt der jeder Aufruf der [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode wird der Wert synchronisiert. 
  
Wenn eine Nachricht keine primären Empfänger enthält, sollte der Nachrichtenspeicher auf einen [IMAPIProp::GetProps](imapiprop-getprops.md) Anruf mit der Rückgabewert S_OK und eine leere Zeichenfolge für **PR_DISPLAY_TO**reagieren. 
  
Aufgrund der möglichen Notwendigkeit Lokalisierung bietet MAPI diese Richtlinien für alle Empfängernamen:
  
- Alle Namen sollte lokalisiert werden können. 
    
- Das Semikolon sollte das Zeichen, mit dem Namen in der **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) und **PR_DISPLAY_TO** Eigenschaften zu trennen. Semikolons dürfen nicht innerhalb von Empfängernamen in MAPI. 
    
- Clients sollte jedem Semikolon festgestellt übersetzen im **PR_DISPLAY_TO** und verwandten Eigenschaften eine lokalisierte Trennzeichen, bevor die Informationen in der Benutzeroberfläche sichtbar gemacht. 
    
- Beim Weiterleiten von Nachrichten müssen Clients nicht die Trennzeichen in der primären Empfänger Zeile übersetzen. 
    
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

