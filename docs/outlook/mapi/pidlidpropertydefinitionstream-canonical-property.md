---
title: Kanonische PidLidPropertyDefinitionStream-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidPropertyDefinitionStream
api_type:
- COM
ms.assetid: ead35049-e60e-4b46-bf12-f73d77cd36b2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2ba6fc19d52e0dbc54c863e0906bf8ff56b512a2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616677"
---
# <a name="pidlidpropertydefinitionstream-canonical-property"></a>Kanonische PidLidPropertyDefinitionStream-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt Definitionen von benutzerdefinierten Feldern und Datenbindungseinstellungen integrierter Felder einer Nachricht dar.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidPropDefStream  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x00008540  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Laufzeitkonfiguration  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Wert der **PidLidPropertyDefinitionStream-Eigenschaft** wird als Teil der benutzerdefinierten Formulardefinition für die Nachricht gespeichert. 
  
Der Wert dieser Eigenschaft ist ein binärer Datenstrom. Informationen zur Struktur dieses Datenstroms finden Sie unter [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md). 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftssatzdefinitionen und Verweise auf verwandte Exchange Server Protokollspezifikationen bereit.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[Outlook Elemente und Felder](outlook-items-and-fields.md)
  
[Hinzufügen einer Definition für ein Neues User-Defined Feld](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[PropertyDefinition-Streambeispiel](propertydefinition-stream-sample.md)
  
[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

