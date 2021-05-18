---
title: PidLidPropertyDefinitionStream (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidPropertyDefinitionStream
api_type:
- COM
ms.assetid: ead35049-e60e-4b46-bf12-f73d77cd36b2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b5ddb87111cfb0039cb1150338945615bbd5afc5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315939"
---
# <a name="pidlidpropertydefinitionstream-canonical-property"></a>PidLidPropertyDefinitionStream (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt Definitionen von benutzerdefinierten Feldern und Datenbindungseinstellungen von integrierten Feldern einer Nachricht dar.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidPropDefStream  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Common  <br/> |
|Lange ID (LID):  <br/> |0x00008540  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Laufzeitkonfiguration  <br/> |
   
## <a name="remarks"></a>Hinweise

Der Wert der **PidLidPropertyDefinitionStream-Eigenschaft** wird als Teil der benutzerdefinierten Formulardefinition für die Nachricht gespeichert. 
  
Der Wert dieser Eigenschaft ist ein binärer Datenstrom. Informationen zur Struktur dieses Datenstroms finden Sie unter [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md). 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[Outlook-Elemente und -Felder](outlook-items-and-fields.md)
  
[Hinzufügen einer Definition für ein new User-Defined Field](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[PropertyDefinition Stream Sample](propertydefinition-stream-sample.md)
  
[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

