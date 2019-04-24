---
title: Kanonische Pidtagstatusstring (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStatusString
api_type:
- COM
ms.assetid: 42cd946c-c55a-4371-99ee-05e2248fdd5f
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9b4510a32fe14e4316a6bcddafcc163ee899436e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278893"
---
# <a name="pidtagstatusstring-canonical-property"></a>Kanonische Pidtagstatusstring (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Meldung, die den aktuellen Status einer Sitzungs Ressource angibt. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_STATUS_STRING, PR_STATUS_STRING_A, PR_STATUS_STRING_W  <br/> |
|Kennung:  <br/> |0x3E08  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |MAPI-Status  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaften bieten Dienstanbietern und MAPI die Möglichkeit, bestimmte Informationen zum Status einer Sitzungs Ressource anzugeben, beispielsweise das integrierte Adressbuch oder einen bestimmten Dienstanbieter. Diese Eigenschaft erläutert und bietet zusätzliche Informationen zu einem Statuscode oder der **PR_STATUS_CODE** ([pidtagstatuscode (](pidtagstatuscode-canonical-property.md))-Eigenschaft. Während **PR_STATUS_CODE** für alle Status-Objekte erforderlich ist, sind **PR_STATUS_STRING** und zugehörige Eigenschaften optional. Wenn der Transportanbieter keinen Wert angibt, stellt der MAPI-Spooler einen Standardwert bereit. 
  
Die Zeichenfolge wird auf derselben Seite des Remoteprozeduraufrufs als MAPI-Spooler generiert; Sie durchläuft Shared Memory, statt über eine Prozessgrenze hinweg gemarshallt zu werden.
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[Kanonische Pidtagstatuscode (-Eigenschaft](pidtagstatuscode-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

