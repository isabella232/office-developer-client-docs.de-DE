---
title: PidTagExceptionReplaceTime (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagExceptionReplaceTime
api_type:
- HeaderDef
ms.assetid: bd4d1311-15e4-4275-a967-c6d11d2e48d2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d8e0120969700974bdf387e65cafe5adc5b96783
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563602"
---
# <a name="pidtagexceptionreplacetime-canonical-property"></a>PidTagExceptionReplaceTime (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt das ursprüngliche Datum und die ursprüngliche Uhrzeit an, zu der die Instanz im Serienmuster aufgetreten wäre, wenn es sich nicht um eine Ausnahme handelte.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_EXCEPTION_REPLACETIME  <br/> |
|Kennung:  <br/> |0x7FF9  <br/> |
|Datentyp:  <br/> |PT_SYSTIME  <br/> |
|Bereich:  <br/> |Nachrichtenklassendefiniert nicht datenübertragungsfähig  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Dieser Wert muss in koordinierter Weltzeit (COORDINATED Universal Time, UTC) angegeben werden.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungsanfrage- und Antwortnachrichten an.
    
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

