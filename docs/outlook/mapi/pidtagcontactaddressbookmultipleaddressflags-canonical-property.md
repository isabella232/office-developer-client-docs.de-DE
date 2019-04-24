---
title: Kanonische Pidtagcontactaddressbookmultipleaddressflags (-Eigenschaft
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
ms.openlocfilehash: ecd795490d953f1aa237dfbd77585ba79c8b3234
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357932"
---
# <a name="pidtagcontactaddressbookmultipleaddressflags-canonical-property"></a>Kanonische Pidtagcontactaddressbookmultipleaddressflags (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält Flags, die angeben, ob die Anbieter mehrere e-Mail-Adressen pro Kontaktelement unterstützen.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CONTAB_MULTI_ADDR_FLAGS  <br/> |
|Kennung:  <br/> |0x6625  <br/> |
|Datentyp:  <br/> |PT_MV_LONG  <br/> |
|Bereich:  <br/> |Kontakt Adressbuch  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn die Flags in dieser Eigenschaft auf TRUE festgelegt sind, enthält der Anbieter keine Kontakte ohne e-Mail-Adressen. Es wird nur die primäre e-Mail-Adresse geehrt. Dies ist eine Eigenschaft in einem Profil Abschnitt des Kontakt Adressbuchs.
  
## <a name="related-resources"></a>Zugehörige Ressourcen

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

