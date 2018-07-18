---
title: PidLidNonSendableTo (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendableTo
api_type:
- COM
ms.assetid: 90e14969-652b-422a-9b0a-ee99e58bc8d5
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 297d9047944388afcf75b9645d76eb2670841ba8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793678"
---
# <a name="pidlidnonsendableto-canonical-property"></a>PidLidNonSendableTo (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Enthält eine Liste aller senden Teilnehmer, die auch die erforderlichen Teilnehmer sind.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |dispidNonSendableTo  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Common  <br/> |
|Long-ID (Abdeckung):  <br/> |0x00008536  <br/> |
|Datentyp:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |Besprechungen  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Wert für jeden Teilnehmer ist die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft des Adressbuchs des Teilnehmers. Separate Einträge müssen durch ein Semikolon, gefolgt von einem Leerzeichen getrennt sein. Diese Eigenschaft ist nicht erforderlich.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

