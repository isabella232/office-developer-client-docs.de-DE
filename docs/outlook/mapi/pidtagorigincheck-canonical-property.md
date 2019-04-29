---
title: Kanonische Pidtagorigincheck (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginCheck
api_type:
- COM
ms.assetid: 27e0ab2f-b373-41ae-b922-2f45f9671ac6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a82b1351c9d2d19c32e34b03a537a12bf93deb8a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435761"
---
# <a name="pidtagorigincheck-canonical-property"></a>Kanonische Pidtagorigincheck (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen binären Überprüfungs Wert, der es einem Zustellungs Berichtsempfänger ermöglicht, den Ursprung der ursprünglichen Nachricht zu überprüfen.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ORIGIN_CHECK  <br/> |
|Kennung:  <br/> |0x0027  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Server  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft bietet einem Drittanbieter, beispielsweise einem MTA (Message Transfer Agent) oder einem Messagingbenutzer, der einen Zustellungsbericht empfängt, die Möglichkeit, den Ursprung der übermittelten Nachricht zu überprüfen. Wenn diese Eigenschaft für eine empfangene Nachricht vorhanden ist, sollte Sie in einen beliebigen Übermittlungsbericht kopiert werden, der als Antwort auf die Nachricht generiert wurde.
  
## <a name="related-resources"></a>Verwandte Ressourcen

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

