---
title: PidTagSupplementaryInfo (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPIi.PidTagSupplementaryInfo
api_type:
- COM
ms.assetid: 2d4231b5-4096-4c0d-b694-65e2d04172b8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0806f6c51ef215b2b839cd136a20a9f8be28272f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609747"
---
# <a name="pidtagsupplementaryinfo-canonical-property"></a>PidTagSupplementaryInfo (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält zusätzliche Informationen für die Verwendung in einem Bericht.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SUPPLEMENTARY_INFO, PR_SUPPLEMENTARY_INFO_A, PR_SUPPLEMENTARY_INFO_W  <br/> |
|Kennung:  <br/> |0x0C1B  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |MAPI-Empfänger  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaften enthalten Informationen, die vom Nachrichtenübertragungs-Agent oder -Transportanbieter im Zusammenhang mit dem Bericht generiert werden. Es wird in der Regel für Übermittlungs- oder Nichtübermittlungsberichtstext verwendet, der vom zugrunde liegenden Messagingsystem stammt.
  
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

