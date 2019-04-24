---
title: Kanonische Pidtagsentmailentryid (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSentMailEntryId
api_type:
- COM
ms.assetid: 8f14dc15-d7d7-4894-b6a8-0d589f576c42
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e7aef8e9ba605d47b110a496e46f629df60a28ea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342511"
---
# <a name="pidtagsentmailentryid-canonical-property"></a>Kanonische Pidtagsentmailentryid (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die Eintrags-ID des Ordners, in den die Nachricht nach der Übermittlung verschoben werden soll.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SENTMAIL_ENTRYID  <br/> |
|Kennung:  <br/> |0x0E0A  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Nicht transmitable MAPI  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird häufig aus der **PR_IPM_SENTMAIL_ENTRYID** ([pidtagipmsentmailentryid (](pidtagipmsentmailentryid-canonical-property.md))-Eigenschaft, dem standardOrdner "Gesendete Elemente" der Clientanwendung, kopiert.
  
Die Clientanwendung verwendet diese Eigenschaft mit der **PR_DELETE_AFTER_SUBMIT** ([pidtagdeleteaftersubmit (](pidtagdeleteaftersubmit-canonical-property.md))-Eigenschaft, um zu steuern, was mit einer Nachricht geschieht, nachdem Sie übermittelt wurde. Entweder die eine oder die andere sollte festgelegt werden, aber nicht beides.
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.
    
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

