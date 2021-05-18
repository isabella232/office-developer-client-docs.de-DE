---
title: PidTagDeferredSendTime (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredSendTime
api_type:
- HeaderDef
ms.assetid: ee206c2d-8371-4d19-b42b-78f6479e13ca
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2d6374c2fd3c277e2bb976930e9e105cc839b1e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359878"
---
# <a name="pidtagdeferredsendtime-canonical-property"></a>PidTagDeferredSendTime (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt einen Zeitpunkt an, zu dem ein Client das Senden einer Nachricht aufschubsen möchte.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DEFERRED_SEND_TIME  <br/> |
|Kennung:  <br/> |0x3FEF  <br/> |
|Datentyp:  <br/> |PT_SYSTIME  <br/> |
|Bereich:  <br/> |MAPI-Status  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn die **Eigenschaften PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) und **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) vorhanden sind, wird der Wert dieser Eigenschaft mithilfe der folgenden Formel neu berechnet, und der alte Wert wird ignoriert.
  
 **PR_DEFERRED_SEND_TIME**  =  **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) + **PR_DEFERRED_SEND_NUMBER** * TimeOf(**PR_DEFERRED_SEND_UNITS**)
  
Wenn **PR_DEFERRED_SEND_TIME** wert vor der aktuellen Uhrzeit (in UTC) liegt, wird die Nachricht sofort gesendet. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

