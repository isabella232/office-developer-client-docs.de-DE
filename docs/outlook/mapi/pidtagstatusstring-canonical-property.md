---
title: Kanonische PidTagStatusString-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagStatusString
api_type:
- COM
ms.assetid: 42cd946c-c55a-4371-99ee-05e2248fdd5f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f1c82448e3989ca45676e1347d86ca1f53ed9062
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599389"
---
# <a name="pidtagstatusstring-canonical-property"></a>Kanonische PidTagStatusString-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Meldung, die den aktuellen Status einer Sitzungsressource angibt. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_STATUS_STRING, PR_STATUS_STRING_A, PR_STATUS_STRING_W  <br/> |
|Kennung:  <br/> |0x3E08  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |MAPI-Status  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaften bieten Dienstanbietern und MAPI die Möglichkeit, spezifische Informationen zum Status einer Sitzungsressource, z. B. das integrierte Adressbuch oder einen bestimmten Dienstanbieter, zur Verfügung zu stellen. Diese Eigenschaft erläutert und stellt zusätzliche Informationen zu einem Statuscode oder der **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) -Eigenschaft bereit. Während **PR_STATUS_CODE** für alle Statusobjekte erforderlich ist, sind **PR_STATUS_STRING** und zugehörige Eigenschaften optional. Wenn der Transportanbieter keinen Wert bereitstellt, stellt der MAPI-Spooler einen Standardwert bereit. 
  
Die Zeichenfolge wird auf derselben Seite des Remoteprozeduraufrufs wie der MAPI-Spooler generiert. er durchfre den freigegebenen Speicher, anstatt über eine Prozessgrenze gemarshallt zu werden.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[Kanonische PidTagStatusCode-Eigenschaft](pidtagstatuscode-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

