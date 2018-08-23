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
ms.openlocfilehash: 9b06ebbe8cb162d77d60cfffa866438567c84c27
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576834"
---
# <a name="pidtagremotevalidateok-canonical-property"></a>PidTagRemoteValidateOk (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Diese Eigenschaft enthält True, wenn der remote-Viewer zulässig ist, die [IMAPIStatus::ValidateState](imapistatus-validatestate.md) -Methode aufrufen. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_REMOTE_VALIDATE_OK  <br/> |
|Kennung:  <br/> |0x3E0D  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |MAPI-Status  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft wird in der Tabelle "Status" und einige Kontrolle über die Transport Leistung bietet. Es kann als eine andere Möglichkeit, leiten den remote Viewer, im Leerlauf betrachtet werden. Wenn sie auf "true" festgelegt ist, kann die remote-Ansicht so oft wie gewünscht **IMAPIStatus::ValidateState** aufrufen. Der Wert FALSE gibt an, dass keine weitere Aufrufe der remote-Viewer nicht ausgeführt werden kann. 
  
Der Transportdienst festgelegt, dass in der Regel diese Eigenschaft dynamisch durch Festlegen des Werts auf false fest, um zusätzliche Anrufe deaktivieren, wenn der Adressbuchhierarchie eine ausreichende Menge der Verarbeitung ausführen hat. Klicken Sie nach Abschluss der Adressbuchhierarchie wird dann den Wert auf TRUE, um die Clientanwendung auf Weitere **IMAPIStatus::ValidateState** tätigen können. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

