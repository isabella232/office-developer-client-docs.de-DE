---
title: Kanonische Pidtagcontactaddressbookmultipleaddressflag (-Eigenschaft
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6fabb03d552f195c200b0ecbd8fd69f470c0e1fd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431568"
---
# <a name="pidtagcontactaddressbookmultipleaddressflag-canonical-property"></a>Kanonische Pidtagcontactaddressbookmultipleaddressflag (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Flag, das TRUE ist, wenn der Anbieter mehrere e-Mail-Adressen pro Kontaktelement unterstützt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CONTAB_MULTI_ADDR_FLAG  <br/> |
|Kennung:  <br/> |0x6614  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Kontakt Adressbuch  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn diese Eigenschaft auf TRUE festgelegt ist, lässt der Anbieter keine Kontakte ohne e-Mail-Adressen zu. Wenn FALSE, zeigt der Anbieter alle Kontakte an, ob er eine primäre e-Mail-Adresse hat oder nicht. Es wird nur die primäre e-Mail-Adresse geehrt. Hierbei handelt es sich um eine Eigenschaft in einem Adressbuchcontainer des Kontakts und eine Spalte in der Tabelle mit Adressbuch Containern des Kontakts.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

