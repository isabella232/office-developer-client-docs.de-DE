---
title: PidTagGender (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagGender
api_type:
- HeaderDef
ms.assetid: a79a139a-6813-49f6-b622-bb66d62c4462
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b8ce3898ac021bc6eec2af6220889d71ff5a18dc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316156"
---
# <a name="pidtaggender-canonical-property"></a>PidTagGender (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält das Geschlecht des Messagingbenutzers.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_GENDER  <br/> |
|Kennung:  <br/> |0x3A4D  <br/> |
|Datentyp:  <br/> |PT_I2  <br/> |
|Bereich:  <br/> |MAPI-E-Mail-Benutzer  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft stellt Identifikations- und Zugriffsinformationen zu einem Messagingbenutzer und den Inhalten zur Verfügung. Der Inhalt wird vom Messagingbenutzer und der Organisation des Messagingbenutzers definiert. 
  
Die möglichen Werte für diese Eigenschaft werden in der Gender-Enumeration definiert. Sie sind wie folgt aufgeführt:
  
|**Gender enumeration**|**Wert**|**Beschreibung**|
|:-----|:-----|:-----|
|genderUnspecified  <br/> |0x0000  <br/> |Das Geschlecht des Kontakts ist nicht angegeben.  <br/> |
|genderFemale  <br/> |0x0001  <br/> |Der Kontakt ist weiblich.  <br/> |
|genderMale  <br/> |0x0002  <br/> |Der Kontakt ist männlich.  <br/> |
   
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
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

