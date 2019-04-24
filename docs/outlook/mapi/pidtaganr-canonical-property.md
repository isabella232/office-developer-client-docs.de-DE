---
title: Kanonische Pidtaganr (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAnr
api_type:
- HeaderDef
ms.assetid: eca3d4ff-2e92-4d20-a498-98e0773c1962
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ce08ba971662b7f5060e6b24a6d2c5ee1a921d5b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327965"
---
# <a name="pidtaganr-canonical-property"></a>Kanonische Pidtaganr (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Zeichenfolgenwert für die Verwendung in einer Eigenschaftseinschränkung in einer Adressbuchcontainer-Inhaltstabelle. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ANR, PR_ANR_A, PR_ANR_W  <br/> |
|Kennung:  <br/> |0x360C  <br/> |
|Datentyp:  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Bereich:  <br/> |Adressbuch  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaften gehören nicht zu einem Objekt; Sie wird von Adressbuch Anbietern in [SPropertyRestriction](spropertyrestriction.md) -Strukturen bereitgestellt. Diese Eigenschaft enthält eine ANR-Zeichenfolge (mehrdeutige Namensauflösung), die anhand der Inhaltstabelle eines Adressbuch Containers getestet werden kann, um entsprechende Nachrichtenempfänger zu finden. 
  
Adressbuchanbieter entsprechen dem Wert von **PR_ANR** und zugeordneten Eigenschaften für jeden Eintrag in der Inhaltstabelle mithilfe eines vom Anbieter definierten übereinstimmenden Algorithmus. Die Spalten, die in dieser Übereinstimmung verwendet werden, werden vom Anbieter als Teil des Algorithmus ausgewählt. Die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Spalte ist die am häufigsten verwendete; die **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))-Spalte ist auch nützlich, wenn Sie den e-Mail-Namen des Benutzers enthält. 
  
Weitere Informationen zur Auflösung mehrdeutiger Namen finden Sie unter [Address Book Restrictions](address-book-restrictions.md). 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[IAddrBook::ResolveName](iaddrbook-resolvename.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

