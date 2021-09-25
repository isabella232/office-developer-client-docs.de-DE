---
title: PidTagContactAddressBookMultipleAddressFlags (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagContactAddressBookMultipleAddressFlags
api_type:
- HeaderDef
ms.assetid: ed3bc585-13f6-46a5-9e71-9c8513ddfc0a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 72cf1ee919ce9bc49792712f9e0b441d23f1ae01
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566843"
---
# <a name="pidtagcontactaddressbookmultipleaddressflags-canonical-property"></a>PidTagContactAddressBookMultipleAddressFlags (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält Flags, die angeben, ob die Anbieter mehrere E-Mail-Adressen pro Kontaktelement unterstützen.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CONTAB_MULTI_ADDR_FLAGS  <br/> |
|Kennung:  <br/> |0x6625  <br/> |
|Datentyp:  <br/> |PT_MV_LONG  <br/> |
|Bereich:  <br/> |Kontaktadressbuch  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn die Flags in dieser Eigenschaft TRUE sind, schließt der Anbieter keine Kontakte ohne E-Mail-Adressen ein. Nur die primäre E-Mail-Adresse wird berücksichtigt. Dies ist eine Eigenschaft in einem Kontaktadressbuch-Profilabschnitt.
  
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

