---
title: PidTagOriginalSearchKey (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagOriginalSearchKey
api_type:
- COM
ms.assetid: ac5eb91d-31c9-459b-bb22-f4ccfc92d1db
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: bad9b00aeaff1de86e73acf94c4e5a50c4f40f8b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599903"
---
# <a name="pidtagoriginalsearchkey-canonical-property"></a>PidTagOriginalSearchKey (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den ursprünglichen Suchschlüssel für einen Eintrag, der aus einem Adressbuch in ein persönliches Adressbuch oder ein anderes beschreibbares Adressbuch kopiert wurde.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ORIGINAL_SEARCH_KEY  <br/> |
|Kennung:  <br/> |0x3A14  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Allgemeines Messaging  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft ist eine der Eigenschaften, die Informationen zur ursprünglichen Quelle eines kopierten Eintrags enthalten.
  
Für einen nicht gelesenen Bericht enthält diese Eigenschaft eine Kopie des Suchschlüssels des ursprünglichen Nachrichtenempfängers, für den der Bericht generiert wird. Wenn der ursprüngliche Empfänger Teil einer Verteilerliste ist, wird der Suchschlüssel der Verteilerliste für den Bericht beibehalten.
  
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
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

