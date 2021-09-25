---
title: PidTagContactAddressBookMultipleAddressFlag (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagContactAddressBookMultipleAddressFlag
api_type:
- HeaderDef
ms.assetid: aefc34c5-1beb-44cf-a455-90f466e157ce
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7ade77c6c519e2c58b45ff60c1748b623e723fbd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571066"
---
# <a name="pidtagcontactaddressbookmultipleaddressflag-canonical-property"></a>PidTagContactAddressBookMultipleAddressFlag (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Flag, das TRUE ist, wenn der Anbieter mehrere E-Mail-Adressen pro Kontaktelement unterstützt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CONTAB_MULTI_ADDR_FLAG  <br/> |
|Kennung:  <br/> |0x6614  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Kontaktadressbuch  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn diese Eigenschaft TRUE ist, lässt der Anbieter keine Kontakte ohne E-Mail-Adressen zu. Bei FALSE zeigt der Anbieter alle Kontakte unabhängig davon an, ob sie über eine primäre E-Mail-Adresse verfügen. Nur die primäre E-Mail-Adresse wird berücksichtigt. Dies ist eine Eigenschaft für einen Kontaktadressbuchcontainer und eine Spalte in der Tabelle der Kontaktadressbuchcontainer.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

