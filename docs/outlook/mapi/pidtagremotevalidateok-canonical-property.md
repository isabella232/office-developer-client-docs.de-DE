---
title: Kanonische Pidtagremotevalidateok (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8b5c9e5bb2aa915d4b76d9998baaf504e7929b78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355615"
---
# <a name="pidtagremotevalidateok-canonical-property"></a>Kanonische Pidtagremotevalidateok (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Diese Eigenschaft enthält TRUE, wenn die Remoteanzeige berechtigt ist, die [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) -Methode aufzurufen. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_REMOTE_VALIDATE_OK  <br/> |
|Kennung:  <br/> |0x3E0D  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |MAPI-Status  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird in der Statustabelle angezeigt und bietet eine gewisse Kontrolle über die Transportleistung. Er kann als eine andere Möglichkeit angesehen werden, um den Remote Viewer in den Leerlauf zu lenken. Wenn Sie auf TRUE festgelegt ist, kann die Remoteanzeige **IMAPIStatus:: ValidateState** so oft wie gewünscht aufrufen. Der Wert FALSE gibt an, dass die Remoteanzeige keine weiteren Anrufe tätigen kann. 
  
Der Transportanbieter legt diese Eigenschaft normalerweise dynamisch fest, indem der Wert auf FALSE festgelegt wird, um zusätzliche Aufrufe zu deaktivieren, wenn der Transportanbieter über ausreichend Verarbeitungsleistung verfügt. Wenn der Transportanbieter fertig ist, wird der Wert auf TRUE festgelegt, damit die Clientanwendung weitere **IMAPIStatus:: ValidateState** -Aufrufe durchführen kann. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

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

