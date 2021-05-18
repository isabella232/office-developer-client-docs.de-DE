---
title: PidTagAnr (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ce08ba971662b7f5060e6b24a6d2c5ee1a921d5b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327965"
---
# <a name="pidtaganr-canonical-property"></a>PidTagAnr (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Zeichenfolgenwert für die Verwendung in einer Eigenschaftseinschränkung für eine Adressbuchcontainerinhaltstabelle. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ANR, PR_ANR_A, PR_ANR_W  <br/> |
|Kennung:  <br/> |0x360C  <br/> |
|Datentyp:  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Bereich:  <br/> |Adressbuch  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaften gehören zu keinem Objekt. Es wird von Adressbuchanbietern in [SPropertyRestriction-Strukturen](spropertyrestriction.md) eingerichtet. Diese Eigenschaft enthält eine zeichenfolge mit mehrdeutiger Namensauflösung (ANR), die mit der Inhaltstabelle eines Adressbuchcontainers getestet werden kann, um nach entsprechenden Nachrichtenempfängern zu suchen. 
  
Adressbuchanbieter entsprechen dem Wert der **PR_ANR** und zugeordneten Eigenschaften mit jedem Eintrag in der Inhaltstabelle, indem sie einen vom Anbieter definierten Abgleichsalgorithmus verwenden. Die spalte oder spalten, die in dieser Übereinstimmung verwendet werden, werden vom Anbieter als Teil des Algorithmus ausgewählt. Die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) ist die am häufigsten verwendete Spalte. Die **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) ist auch hilfreich, wenn sie den E-Mail-Namen des Benutzers enthält. 
  
Weitere Informationen zur mehrdeutigen Namensauflösung finden Sie unter [Adressbucheinschränkungen](address-book-restrictions.md). 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[IAddrBook::ResolveName](iaddrbook-resolvename.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

