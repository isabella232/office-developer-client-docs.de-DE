---
title: PidTagAssistantTelephoneNumber (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAssistantTelephoneNumber
api_type:
- HeaderDef
ms.assetid: edb0782c-6671-4e98-9028-a2f9ad547c1d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6eafe51490b231b9cc64242595aef54bcc85c3ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360417"
---
# <a name="pidtagassistanttelephonenumber-canonical-property"></a>PidTagAssistantTelephoneNumber (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die Telefonnummer des Administrativen Assistenten des Empfängers. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ASSISTANT_TELEPHONE_NUMBER, PR_ASSISTANT_TELEPHONE_NUMBER_A, PR_ASSISTANT_TELEPHONE_NUMBER_W  <br/> |
|Kennung:  <br/> |0x3A2E  <br/> |
|Datentyp:  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Bereich:  <br/> |Adresse  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaften stellen Identifikations- und Zugriffsinformationen für einen Empfänger zur Verfügung. Sie werden vom Empfänger und seiner Organisation definiert. 
  
Die Telefonnummer ist für den in der Eigenschaft **PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md)) angegebenen Assistenten. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.
    
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

