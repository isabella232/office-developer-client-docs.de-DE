---
title: PidTagContentCorrelator (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagContentCorrelator
api_type:
- HeaderDef
ms.assetid: 0bf78879-2f9f-4c29-b1f4-2f4882d8464d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: baad9a247687f9753a5c63d27c7e9cdc07b74e5e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616544"
---
# <a name="pidtagcontentcorrelator-canonical-property"></a>PidTagContentCorrelator (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Wert, den der Absender der Nachricht verwenden kann, um einen Bericht mit der ursprünglichen Nachricht zuzuordnen.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CONTENT_CORRELATOR  <br/> |
|Kennung:  <br/> |0x0007  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Inhalt der binären Zeichenfolge wird vom Nachrichtenursprungsgeber definiert. Wenn diese Eigenschaft für eine ausgehende Nachricht festgelegt ist, sollte sie in alle Berichte kopiert werden, die als Reaktion auf die Nachricht generiert wurden.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

