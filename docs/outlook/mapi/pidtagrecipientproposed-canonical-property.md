---
title: PidTagRecipientProposed (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientProposed
api_type:
- COM
ms.assetid: 8cb0e46c-0937-482f-be78-1f2e5261b210
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1b09d8d7621121b3652ceb9824f6d36b53844206
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283135"
---
# <a name="pidtagrecipientproposed-canonical-property"></a>PidTagRecipientProposed (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, ob ein Besprechungsteilnehmer geantwortet hat.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RECIPIENT_PROPOSED  <br/> |
|Kennung:  <br/> |0x5FE1  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Transportempfänger  <br/> |
   
## <a name="remarks"></a>Hinweise

Der Wert TRUE für diese Eigenschaft gibt an, dass der Teilnehmer ein neues Datum und/oder eine neue Uhrzeit vorgeschlagen hat. Der Wert FALSE oder das Fehlen dieser Eigenschaft bedeutet, dass der Teilnehmer noch nicht geantwortet hat oder die letzte Antwort des Teilnehmers keinen neuen Datums-/Uhrzeitvorschlag enthält. Dieser Wert darf für Teilnehmer in einer Serienserie nicht TRUE sein.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.
    
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

