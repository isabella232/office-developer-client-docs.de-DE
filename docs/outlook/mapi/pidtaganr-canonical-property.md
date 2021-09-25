---
title: Kanonische PidTagAnr-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAnr
api_type:
- HeaderDef
ms.assetid: eca3d4ff-2e92-4d20-a498-98e0773c1962
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: cd14d1b42603d81897f5bfeb177382d7e8941300
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571241"
---
# <a name="pidtaganr-canonical-property"></a>Kanonische PidTagAnr-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Zeichenfolgenwert für die Verwendung in einer Eigenschaftseinschränkung in einer Adressbuchcontainer-Inhaltstabelle. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ANR, PR_ANR_A, PR_ANR_W  <br/> |
|Kennung:  <br/> |0x360C  <br/> |
|Datentyp:  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Bereich:  <br/> |Adressbuch  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaften gehören keinem Objekt; es wird von Adressbuchanbietern in [SPropertyRestriction-Strukturen](spropertyrestriction.md) bereitgestellt. Diese Eigenschaft enthält eine Anr-Zeichenfolge (Ambiguous Name Resolution), die anhand des Inhaltsverzeichnisses eines Adressbuchcontainers getestet werden kann, um entsprechende Nachrichtenempfänger zu finden. 
  
Adressbuchanbieter stimmen mithilfe eines vom Anbieter definierten Vergleichsalgorithmus den Wert **von PR_ANR** und zugehörigen Eigenschaften mit jedem Eintrag im Inhaltsverzeichnis ab. Die Spalten, die in dieser Übereinstimmung verwendet werden, werden vom Anbieter als Teil des Algorithmus ausgewählt. Die **spalte PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) wird am häufigsten verwendet. die **Spalte PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) ist auch nützlich, wenn sie den E-Mail-Namen des Benutzers enthält. 
  
Weitere Informationen zur Auflösung nicht eindeutiger Namen finden Sie unter [Adressbucheinschränkungen.](address-book-restrictions.md) 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[IAddrBook::ResolveName](iaddrbook-resolvename.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

