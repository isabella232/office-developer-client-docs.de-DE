---
title: PidTagRemoteValidateOk (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRemoteValidateOk
api_type:
- COM
ms.assetid: e336d2ec-57cb-4d08-bd6e-330ef7d9939e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8b5c9e5bb2aa915d4b76d9998baaf504e7929b78
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424224"
---
# <a name="pidtagremotevalidateok-canonical-property"></a>PidTagRemoteValidateOk (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Diese Eigenschaft enthält TRUE, wenn der Remoteanzeige die [IMAPIStatus::ValidateState-Methode aufrufen](imapistatus-validatestate.md) darf. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_REMOTE_VALIDATE_OK  <br/> |
|Kennung:  <br/> |0x3E0D  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |MAPI-Status  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird in der Statustabelle angezeigt und bietet eine gewisse Kontrolle über die Transportleistung. Es kann als eine weitere Möglichkeit betrachtet werden, den Remoteanzeiger in den Leerlauf zu leitet. Wenn sie auf TRUE festgelegt ist, kann die Remoteanzeige **IMAPIStatus::ValidateState** so oft wie gewünscht aufrufen. Der Wert FALSE gibt an, dass der Remoteanzeige keine weiteren Aufrufe mehr machen kann. 
  
Der Transportanbieter legt diese Eigenschaft in der Regel dynamisch fest, indem der Wert auf FALSE gesetzt wird, um zusätzliche Aufrufe zu deaktivieren, wenn der Transportanbieter über eine ausreichende Verarbeitungsmenge verfügt. Wenn der Transportanbieter fertig ist, wird der Wert auf TRUE festgelegt, damit die Clientanwendung weitere **IMAPIStatus::ValidateState-Aufrufe erstellen** kann. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

