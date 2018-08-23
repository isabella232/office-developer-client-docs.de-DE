---
title: PidTagDetailsTable (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1602d1753d9f7f6e6f407a85dab0a33255db7aae
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585787"
---
# <a name="pidtagdetailstable-canonical-property"></a>PidTagDetailsTable (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält eine eingebettete Anzeige Table-Objekt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DETAILS_TABLE  <br/> |
|Kennung:  <br/> |0x3605  <br/> |
|Datentyp:  <br/> |PT_OBJECT  <br/> |
|Bereich:  <br/> |MAPI-container  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Übergeben diese Eigenschaft an die [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode für das Objekt gibt eine [IMAPITable](imapitableiunknown.md) -Schnittstelle, mit der Erstellung der Tabelle anzeigen kann. MAPI verwendet diese Tabelle, um die Eigenschaftenseiten für ein Address Book-Objekt als Reaktion auf einen Anruf [IAddrBook::Details](iaddrbook-details.md) angezeigt. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[PidTagCreateTemplates (kanonische Eigenschaft)](pidtagcreatetemplates-canonical-property.md)
  
[PidTagSearch (kanonische Eigenschaft)](pidtagsearch-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

