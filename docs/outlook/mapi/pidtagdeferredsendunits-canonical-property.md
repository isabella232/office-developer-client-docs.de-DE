---
title: PidTagDeferredSendUnits (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDeferredSendUnits
api_type:
- HeaderDef
ms.assetid: 2386be9f-18c9-4949-a2aa-efc8e212801c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5e7cbc5729d2545b0d342913dcd16921b9d8bd94
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600204"
---
# <a name="pidtagdeferredsendunits-canonical-property"></a>PidTagDeferredSendUnits (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die Zeiteinheit an, mit der der Wert der **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) multipliziert werden soll.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DEFERRED_SEND_UNITS  <br/> |
|Kennung:  <br/> |0x3FEC  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Status  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn diese Eigenschaft festgelegt ist, muss sie einen der folgenden Werte aufweisen:
  
|||
|:-----|:-----|
|**PidTagDeferredSendUnits** <br/> |Beschreibung  <br/> |
|0  <br/> |Minuten, z. B. 60 Sekunden  <br/> |
|1  <br/> |Stunden, z. B. 60 x 60 Sekunden  <br/> |
|2  <br/> |Tag, z. B. 24 x 60 x 60 Sekunden  <br/> |
|3  <br/> |Woche, z. B. 7x24x60x60 Sekunden  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.
    
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

