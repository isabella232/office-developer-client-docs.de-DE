---
title: Kanonische pidlidcontactlinksearchkey (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContactLinkSearchKey
api_type:
- COM
ms.assetid: 82d21d38-a6c6-4e12-85b1-8158b2f5cce7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ea815631f63b5585a3f2705cfbd2639b8c655e6e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319775"
---
# <a name="pidlidcontactlinksearchkey-canonical-property"></a>Kanonische pidlidcontactlinksearchkey (-Eigenschaft

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die Liste der **SearchKeys** für den Kontakt, der mit diesem Nachrichtenobjekt verknüpft ist. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidContactLinkSearchKey  <br/> |
|Eigenschaftengruppe:  <br/> |PSETID_Common  <br/> |
|Lange ID (LID):  <br/> |0x00008584  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Kontakt  <br/> |
   
## <a name="remarks"></a>Hinweise

|**Länge in Bytes**|**Beschreibung**|**Hinweise**|
|:-----|:-----|:-----|
|2  <br/> |ContactEntryCount  <br/> |Keine  <br/> |
|Variable  <br/> |SearchKey-Daten  <br/> |Wiederholt ContactEntryCount mal  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftenmengen Definitionen und Verweise auf zugehörige Exchange Server Protokollspezifikationen bereit.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Verarbeitet Nachrichten-und Attachment-Objekte.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Definitionen von Datentypen bereit.
    
## <a name="see-also"></a>Siehe auch

- [MAPI-Eigenschaften](mapi-properties.md) 
- [Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
- [Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
- [Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

