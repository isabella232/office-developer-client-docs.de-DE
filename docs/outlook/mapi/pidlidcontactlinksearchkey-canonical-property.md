---
title: PidLidContactLinkSearchKey (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidContactLinkSearchKey
api_type:
- COM
ms.assetid: 82d21d38-a6c6-4e12-85b1-8158b2f5cce7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c455687a44b0f35a237638eb0c951042a1346932
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583884"
---
# <a name="pidlidcontactlinksearchkey-canonical-property"></a>PidLidContactLinkSearchKey (kanonische Eigenschaft)

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die Liste der **SearchKeys** für den Kontakt, mit dem dieses Nachrichtenobjekt verknüpft ist. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidContactLinkSearchKey  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x00008584  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Kontakt  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

|**Länge in Byte**|**Beschreibung**|**Hinweise**|
|:-----|:-----|:-----|
|2  <br/> |ContactEntryCount  <br/> |Keines  <br/> |
|Variable  <br/> |SearchKey-Daten  <br/> |Repeats ContactEntryCount times  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftssatzdefinitionen und Verweise auf verwandte Exchange Server Protokollspezifikationen bereit.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch

- [MAPI-Eigenschaften](mapi-properties.md) 
- [KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
- [Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
- [Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

