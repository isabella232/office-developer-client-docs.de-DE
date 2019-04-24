---
title: Kanonische Pidtagimplicitconversionprohibited (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagImplicitConversionProhibited
api_type:
- HeaderDef
ms.assetid: c6cb5a86-0105-4743-9f8e-b832e898da52
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a0e18ef529b65317abd9446408ed73638c792809
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346606"
---
# <a name="pidtagimplicitconversionprohibited-canonical-property"></a>Kanonische Pidtagimplicitconversionprohibited (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält TRUE, wenn für einen MTA (Message Transfer Agent) keine impliziten Nachrichtentext Konvertierungen zulässig sind.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_IMPLICIT_CONVERSION_PROHIBITED  <br/> |
|Kennung:  <br/> |0x0016  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Server  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn diese Eigenschaft auf TRUE festgelegt ist, darf das Messagingsystem keine Inhaltskonvertierung für die Nachricht durchführen, es sei denn, Sie wird explizit pro Empfänger mit der **PR_EXPLICIT_CONVERSION** ([pidtagexplicitconversion (](pidtagexplicitconversion-canonical-property.md))-Eigenschaft angefordert.
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

