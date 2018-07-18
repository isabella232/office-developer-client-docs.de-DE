---
title: PidTagContactAddressBookMultipleAddressFlag (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookMultipleAddressFlag
api_type:
- HeaderDef
ms.assetid: aefc34c5-1beb-44cf-a455-90f466e157ce
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 42f164f09dbffcc05986771aa05f7ce14eee789c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794196"
---
# <a name="pidtagcontactaddressbookmultipleaddressflag-canonical-property"></a>PidTagContactAddressBookMultipleAddressFlag (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Enthält ein Flag, das auf true festgelegt ist, wenn der Anbieter pro Kontaktelement mehrere e-Mail-Adressen unterstützt.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_CONTAB_MULTI_ADDR_FLAG  <br/> |
|Bezeichner:  <br/> |0x6614  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Kontakt-Adressbuch  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn diese Eigenschaft auf true festgelegt ist, ist der Anbieter Kontakte ohne e-Mail-Adressen nicht zulässig. Ist der Wert FALSE ist, zeigt der Anbieter alle Kontakte unabhängig davon, ob sie eine primäre e-Mail-Adresse besitzen. Nur die primäre e-Mail-Adresse wird berücksichtigt. Dies ist eine Eigenschaft für einen Kontakt Adressbuch-Container und eine Spalte in der Tabelle der Kontakt-Adressbuch-Container.
  
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

