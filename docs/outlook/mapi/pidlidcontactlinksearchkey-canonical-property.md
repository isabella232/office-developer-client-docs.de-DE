---
title: PidLidContactLinkSearchKey (kanonische Eigenschaft)
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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387496"
---
# <a name="pidlidcontactlinksearchkey-canonical-property"></a>PidLidContactLinkSearchKey (kanonische Eigenschaft)

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die Liste der **SearchKeys** für den Kontakt mit verknüpften durch dieses Objekt "Message". 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidContactLinkSearchKey  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Common  <br/> |
|Long-ID (Abdeckung):  <br/> |0x00008584  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Kontakt  <br/> |
   
## <a name="remarks"></a>Hinweise

|**Länge in bytes**|**Beschreibung**|**Hinweise**|
|:-----|:-----|:-----|
|2  <br/> |ContactEntryCount  <br/> |Keine  <br/> |
|Variable  <br/> |SearchKey Daten  <br/> |ContactEntryCount-Mal wiederholt  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Nachrichten und Anlagen Objekte behandelt.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch

- [MAPI-Eigenschaften](mapi-properties.md) 
- [Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
- [Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
- [Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

