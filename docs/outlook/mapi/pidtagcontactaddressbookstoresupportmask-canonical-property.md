---
title: PidTagContactAddressBookStoreSupportMask (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookStoreSupportMask
api_type:
- HeaderDef
ms.assetid: 34f649c8-29bf-470f-9b05-31b69d069259
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fb40e2c191056fe164c6a06bfdcf4b8e3d6eb92c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434438"
---
# <a name="pidtagcontactaddressbookstoresupportmask-canonical-property"></a>PidTagContactAddressBookStoreSupportMask (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagcontactaddressbookstoresupportmask-canonical-property.md)) -Eigenschaft, die aus dem Speicher mit dem Ordner Kontakte erhalten wurde.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CONTAB_STORE_SUPPORT_MASK  <br/> |
|Kennung:  <br/> |0x6611  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Kontaktadressenbuch  <br/> |
   
## <a name="remarks"></a>Hinweise

Der Adressbuchanbieter verwendet diese Eigenschaft, um die Angemessenheit der unterstützten Funktionen des Informationsspeichers zu bewerten. Dies ist eine Eigenschaft für einen Contact Address Book-Container und eine Spalte in der Tabelle der Kontaktadressenbuchcontainer.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

