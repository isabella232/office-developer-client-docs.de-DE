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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b2ac7aa4fca8583fc59d727c55433108bee62dee
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794431"
---
# <a name="pidtaggender-canonical-property"></a>PidTagGender (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Das Geschlecht der messaging-Benutzer enthält.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_GENDER  <br/> |
|Bezeichner:  <br/> |0x3A4D  <br/> |
|Datentyp:  <br/> |PT_I2  <br/> |
|Bereich:  <br/> |MAPI-e-Mail-Benutzer  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft bietet Identifikations- und Zugriff auf Informationen über ein messaging-Benutzer und der Inhalt ist. Der Inhalt wird durch die messaging-Benutzer und Organisation messaging-Benutzer definiert. 
  
Die möglichen Werte für diese Eigenschaft sind in der Geschlecht-Aufzählung definiert. Sie sind wie folgt:
  
|**Geschlecht-Aufzählung**|**Wert**|**Beschreibung**|
|:-----|:-----|:-----|
|genderUnspecified  <br/> |0x0000  <br/> |Geschlecht des Kontakts ist nicht angegeben.  <br/> |
|genderFemale  <br/> |0x0001  <br/> |Der Kontakt ist Weiblich.  <br/> |
|genderMale  <br/> |0x0002  <br/> |Der Kontakt ist Männlich.  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

