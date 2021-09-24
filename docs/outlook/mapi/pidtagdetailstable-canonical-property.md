---
title: PidTagDetailsTable (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDetailsTable
api_type:
- HeaderDef
ms.assetid: 7a0ccad3-f497-4871-b733-771e6cb8ef6a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 81a8fd91fcc920a7ba2a165c3f4867675e3d9204
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550715"
---
# <a name="pidtagdetailstable-canonical-property"></a>PidTagDetailsTable (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein eingebettetes Anzeigetabellenobjekt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DETAILS_TABLE  <br/> |
|Kennung:  <br/> |0x3605  <br/> |
|Datentyp:  <br/> |PT_OBJECT  <br/> |
|Bereich:  <br/> |MAPI-Container  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn Sie diese Eigenschaft an die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) für das Objekt übergeben, wird eine [IMAPITable-Schnittstelle](imapitableiunknown.md) zurückgegeben, die das Erstellen der Anzeigetabelle ermöglicht. MAPI verwendet diese Tabelle, um Eigenschaftsblätter für ein Adressbuchobjekt als Reaktion auf einen [IAddrBook::D Etails-Aufruf](iaddrbook-details.md) anzuzeigen. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[PidTagCreateTemplates (kanonische Eigenschaft)](pidtagcreatetemplates-canonical-property.md)
  
[Kanonische PidTagSearch-Eigenschaft](pidtagsearch-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

