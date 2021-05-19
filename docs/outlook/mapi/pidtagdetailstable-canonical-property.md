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
ms.openlocfilehash: 74eae4a4ed742c3bb90496f5975ad7dac6ff798f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419254"
---
# <a name="pidtagdetailstable-canonical-property"></a>PidTagDetailsTable (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein eingebettetes Anzeigetabelle-Objekt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DETAILS_TABLE  <br/> |
|Kennung:  <br/> |0x3605  <br/> |
|Datentyp:  <br/> |PT_OBJECT  <br/> |
|Bereich:  <br/> |MAPI-Container  <br/> |
   
## <a name="remarks"></a>Hinweise

Durch Übergeben dieser Eigenschaft an die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) für das Objekt wird eine [IMAPITable-Schnittstelle](imapitableiunknown.md) zurückgegeben, die das Erstellen der Anzeigetabelle ermöglicht. MAPI verwendet diese Tabelle, um Eigenschaftenblätter für ein Adressbuchobjekt als Reaktion auf einen [IAddrBook::D etails-Aufruf anzuzeigen.](iaddrbook-details.md) 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[PidTagCreateTemplates (kanonische Eigenschaft)](pidtagcreatetemplates-canonical-property.md)
  
[PidTagSearch (kanonische Eigenschaft)](pidtagsearch-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

