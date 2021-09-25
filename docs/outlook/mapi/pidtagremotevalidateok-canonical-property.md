---
title: PidTagRemoteValidateOk (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRemoteValidateOk
api_type:
- COM
ms.assetid: e336d2ec-57cb-4d08-bd6e-330ef7d9939e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 686bfbd5f023d5d5c22b047633c80d3a86055663
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591605"
---
# <a name="pidtagremotevalidateok-canonical-property"></a>PidTagRemoteValidateOk (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Diese Eigenschaft enthält TRUE, wenn der Remoteviewer die [IMAPIStatus::ValidateState-Methode](imapistatus-validatestate.md) aufrufen darf. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_REMOTE_VALIDATE_OK  <br/> |
|Kennung:  <br/> |0x3E0D  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |MAPI-Status  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft wird in der Statustabelle angezeigt und bietet eine gewisse Kontrolle über die Transportleistung. Es kann als eine andere Möglichkeit betrachtet werden, den Remoteviewer in den Leerlauf zu leiten. Wenn sie auf TRUE festgelegt ist, kann die Remoteanzeige **IMAPIStatus::ValidateState** so oft wie gewünscht aufrufen. Der Wert FALSE gibt an, dass der Remoteviewer keine weiteren Aufrufe ausführen kann. 
  
Der Transportanbieter legt diese Eigenschaft in der Regel dynamisch fest, indem der Wert auf FALSE festgelegt wird, um zusätzliche Aufrufe zu deaktivieren, wenn der Transportanbieter über eine ausreichende Verarbeitungsmenge verfügt. Wenn der Transportanbieter abgeschlossen ist, wird der Wert auf TRUE festgelegt, damit die Clientanwendung weitere **IMAPIStatus::ValidateState-Aufrufe** ausführen kann. 
  
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

