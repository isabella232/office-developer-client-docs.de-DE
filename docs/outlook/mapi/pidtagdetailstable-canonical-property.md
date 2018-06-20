---
title: Kanonische PidTagDetailsTable-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDetailsTable
api_type:
- HeaderDef
ms.assetid: 7a0ccad3-f497-4871-b733-771e6cb8ef6a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a267f9a9fb8d97256cf7a448b453d04db2118180
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794301"
---
# <a name="pidtagdetailstable-canonical-property"></a>Kanonische PidTagDetailsTable-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält eine eingebettete Anzeige Table-Objekt.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_DETAILS_TABLE  <br/> |
|Bezeichner:  <br/> |0x3605  <br/> |
|Datentyp:  <br/> |PT_OBJECT  <br/> |
|Bereich:  <br/> |MAPI-container  <br/> |
   
## <a name="remarks"></a>Hinweise

Übergeben diese Eigenschaft an die [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode für das Objekt gibt eine [IMAPITable](imapitableiunknown.md) -Schnittstelle, mit der Erstellung der Tabelle anzeigen kann. MAPI verwendet diese Tabelle, um die Eigenschaftenseiten für ein Address Book-Objekt als Reaktion auf einen Anruf [IAddrBook::Details](iaddrbook-details.md) angezeigt. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[Kanonische PidTagCreateTemplates-Eigenschaft](pidtagcreatetemplates-canonical-property.md)
  
[Kanonische PidTagSearch-Eigenschaft](pidtagsearch-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

