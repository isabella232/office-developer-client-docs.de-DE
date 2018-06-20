---
title: Kanonische PidTagMessageDeliveryTime-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageDeliveryTime
api_type:
- HeaderDef
ms.assetid: 4f9d44f2-4faa-4f16-9e33-22f80c17db85
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4fd74e99a8073db03ad47292677ff98efca58af3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794598"
---
# <a name="pidtagmessagedeliverytime-canonical-property"></a>Kanonische PidTagMessageDeliveryTime-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält Datum und Uhrzeit, wenn eine Nachricht nicht übermittelt wurde. 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_MESSAGE_DELIVERY_TIME  <br/> |
|Bezeichner:  <br/> |0x0E06  <br/> |
|Datentyp:  <br/> |PT_SYSTIME  <br/> |
|Bereich:  <br/> |Nachrichtzeit  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft beschreibt Zeitpunkt, zu dem die Nachricht auf dem Server gespeichert wurde, statt die Uhrzeit des Downloads, wenn der Adressbuchhierarchie die Nachricht vom Server auf den lokalen Speicher kopiert.
  
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

