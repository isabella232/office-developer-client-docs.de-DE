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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 94e83f4a93bac4ee144c5fbf94fd4b3fdb6c2f55
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794072"
---
# <a name="pidtaganr-canonical-property"></a>PidTagAnr (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Einen String-Wert für die Verwendung in einer eigenschaftseinschränkung auf eine Adresse Adressbuch Container Inhaltstabelle enthält. 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_ANR, PR_ANR_A, PR_ANR_W  <br/> |
|Bezeichner:  <br/> |0x360C  <br/> |
|Datentyp:  <br/> |PT_UNICODE PT_STRING8  <br/> |
|Bereich:  <br/> |Adressbuch  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaften gehören nicht auf ein beliebiges Objekt; Es wird von adressbuchanbietern implementierte in [SPropertyRestriction](spropertyrestriction.md) Strukturen bereitgestellt. Diese Eigenschaft enthält eine Zeichenfolge der mehrdeutiger Name-Lösung (ANR), die ein Adressbuchcontainer Inhaltstabelle, entsprechende Empfänger der Nachricht erhalten verglichen werden kann. 
  
Von adressbuchanbietern implementierte gleich dem Wert der **PR_ANR** und zugeordneten Eigenschaften für jeden Eintrag in der Inhaltstabelle mit einer vom Anbieter definiertes übereinstimmenden Algorithmus. Die Spalte oder Spalten, die in diese Übereinstimmung verwendet werden, werden vom Anbieter als Teil des Algorithmus ausgewählt. Die Spalte **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) ist die am häufigsten verwendet. die Spalte **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) ist auch nützlich, wenn sie den Namen des Benutzers e-Mail enthält. 
  
Weitere Informationen über die Auflösung nicht eindeutiger Namen finden Sie unter [Address Book Einschränkungen](address-book-restrictions.md). 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[IAddrBook::ResolveName](iaddrbook-resolvename.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

