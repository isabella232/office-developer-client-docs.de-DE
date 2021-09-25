---
title: PidTagOriginCheck (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagOriginCheck
api_type:
- COM
ms.assetid: 27e0ab2f-b373-41ae-b922-2f45f9671ac6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f87f2a56c9b0c69875bcf4f139052cc1d0ef4505
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619792"
---
# <a name="pidtagorigincheck-canonical-property"></a>PidTagOriginCheck (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen binären Überprüfungswert, mit dem ein Empfänger des Übermittlungsberichts den Ursprung der ursprünglichen Nachricht überprüfen kann.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ORIGIN_CHECK  <br/> |
|Kennung:  <br/> |0x0027  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Server  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft stellt eine Möglichkeit für einen Drittanbieter bereit, z. B. einen Nachrichtenübertragungs-Agent (Message Transfer Agent, MTA) oder einen Nachrichtenbenutzer, der einen Übermittlungsbericht erhält, um den Ursprung der gesendeten Nachricht zu überprüfen. Wenn diese Eigenschaft in einer empfangenen Nachricht vorhanden ist, sollte sie in einen übermittlungsbericht kopiert werden, der als Antwort auf die Nachricht generiert wurde.
  
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

