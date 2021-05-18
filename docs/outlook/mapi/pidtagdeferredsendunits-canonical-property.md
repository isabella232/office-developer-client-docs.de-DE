---
title: PidTagDeferredSendUnits (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredSendUnits
api_type:
- HeaderDef
ms.assetid: 2386be9f-18c9-4949-a2aa-efc8e212801c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: becc076efe0f4f805eb2a8db071b70ad731ee256
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359906"
---
# <a name="pidtagdeferredsendunits-canonical-property"></a>PidTagDeferredSendUnits (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die Zeiteinheit an, mit der **der Wert der PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) multipliziert werden soll.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DEFERRED_SEND_UNITS  <br/> |
|Kennung:  <br/> |0x3FEC  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Status  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn festgelegt, muss diese Eigenschaft über einen der folgenden Werte verfügen:
  
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
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

