---
title: PidTagConversionWithLossProhibited (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagConversionWithLossProhibited
api_type:
- HeaderDef
ms.assetid: a18b560a-e054-45b3-946d-6504465db5b7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 86105f1adb1fa464e2577229db936f1be4d7427e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566808"
---
# <a name="pidtagconversionwithlossprohibited-canonical-property"></a>PidTagConversionWithLossProhibited (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält TRUE, wenn es einem Nachrichtenübertragungs-Agent (Message Transfer Agent, MTA) nicht gestattet ist, Nachrichtentextkonvertierungen durchzuführen, die Informationen verlieren. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CONVERSION_WITH_LOSS_PROHIBITED  <br/> |
|Kennung:  <br/> |0x000D  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Allgemeine Konfiguration  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Ein Beispiel für den nicht zulässigen Konvertierungstyp ist die Verlustzuordnung von Unicode (zwei Bytes pro Zeichen) zu einem Einzelbyte-Zeichensatz. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

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

