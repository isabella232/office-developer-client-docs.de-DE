---
title: PidTagStatusString (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9b4510a32fe14e4316a6bcddafcc163ee899436e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421564"
---
# <a name="pidtagstatusstring-canonical-property"></a>PidTagStatusString (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Meldung, die den aktuellen Status einer Sitzungsressource angibt. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_STATUS_STRING, PR_STATUS_STRING_A, PR_STATUS_STRING_W  <br/> |
|Kennung:  <br/> |0x3E08  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |MAPI-Status  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaften bieten Dienstanbietern und MAPI die Möglichkeit, spezifische Informationen über den Status einer Sitzungsressource, z. B. das integrierte Adressbuch oder einen bestimmten Dienstanbieter, zur Verfügung zu haben. Diese Eigenschaft erläutert und stellt zusätzliche Informationen zu einem Statuscode oder der **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) -Eigenschaft zur Verfügung. Während **PR_STATUS_CODE** für alle Statusobjekte erforderlich ist, **sind PR_STATUS_STRING** und zugeordnete Eigenschaften optional. Wenn der Transportanbieter keinen Wert liefert, gibt der MAPI-Spooler einen Standardwert an. 
  
Die Zeichenfolge wird auf derselben Seite des Remoteprozeduraufrufs wie der #A0 generiert. Es wird durch freigegebenen Speicher anstatt über eine Prozessgrenze ge marshallt.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[PidTagStatusCode (kanonische Eigenschaft)](pidtagstatuscode-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

