---
title: PidTagContactAddressBookMultipleAddressFlags (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookMultipleAddressFlags
api_type:
- HeaderDef
ms.assetid: ed3bc585-13f6-46a5-9e71-9c8513ddfc0a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: fbe955d3e7a509edf6ba10678e1e2538c9185193
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794185"
---
# <a name="pidtagcontactaddressbookmultipleaddressflags-canonical-property"></a>PidTagContactAddressBookMultipleAddressFlags (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Flags, die pro Kontaktelement zurück, der angibt, ob der Anbieter mehrere e-Mail unterstützt-Adressen enthält.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_CONTAB_MULTI_ADDR_FLAGS  <br/> |
|Bezeichner:  <br/> |0x6625  <br/> |
|Datentyp:  <br/> |PT_MV_LONG  <br/> |
|Bereich:  <br/> |Kontakt-Adressbuch  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn die Kennzeichen in dieser Eigenschaft TRUE sind, ist der Anbieter nicht Kontakte ohne e-Mail-Adressen enthalten. Nur die primäre e-Mail-Adresse wird berücksichtigt. Dies ist eine Eigenschaft für einen Kontakt Adressbuch Profil.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

