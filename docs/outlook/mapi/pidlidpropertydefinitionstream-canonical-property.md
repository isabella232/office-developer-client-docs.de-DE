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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f7f764d95c2fc36ba6af617333cb47d266cd2aa9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793715"
---
# <a name="pidlidpropertydefinitionstream-canonical-property"></a>PidLidPropertyDefinitionStream (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Stellt Definitionen der benutzerdefinierten Felder und Datenbindung Einstellungen für integrierte Felder einer Nachricht.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |dispidPropDefStream  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Common  <br/> |
|Long-ID (Abdeckung):  <br/> |0x00008540  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Laufzeit-Konfiguration  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Wert der Eigenschaft **PidLidPropertyDefinitionStream** wird als Teil der Definition der benutzerdefiniertes Formular für die Nachricht gespeichert. 
  
Der Wert dieser Eigenschaft ist einen binären Datenstrom. Informationen zur Struktur dieses Streams finden Sie unter [PropertyDefinition Stream Struktur](propertydefinition-stream-structure.md). 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[Elemente und Felder in Outlook](outlook-items-and-fields.md)
  
[Hinzufügen einer Definition für ein neues benutzerdefiniertes Feld](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[Beispiel für PropertyDefinition-Stream](propertydefinition-stream-sample.md)
  
[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

