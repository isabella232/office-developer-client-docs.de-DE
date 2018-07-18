---
title: PidTagRecipientNumberForAdvice (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientNumberForAdvice
api_type:
- COM
ms.assetid: 636c1e75-3024-43ca-a7dd-1bb480dfbb5b
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ac4da2d4082cac632548594411528b7bf1d6dc64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794900"
---
# <a name="pidtagrecipientnumberforadvice-canonical-property"></a>PidTagRecipientNumberForAdvice (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Diese Eigenschaft enthält einen Nachrichtenempfänger Telefonnummer von der physischen Übermittlung einer Nachricht informiert.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_RECIPIENT_NUMBER_FOR_ADVICE, PR_RECIPIENT_NUMBER_FOR_ADVICE_A, PR_RECIPIENT_NUMBER_FOR_ADVICE_W  <br/> |
|Bezeichner:  <br/> |0x0C14  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |MAPI-Empfänger  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaften sind in Verbindung mit der Zustellung an eine physische Ziel, statt ein elektronisches-Postfach verwendet werden, wenn der menschliche Empfänger nicht erwartet wird, Übermittlung vorhanden sein soll. Ein Beispiel ist die Telefonnummer auf ein Faxdeckblatt.
  
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

