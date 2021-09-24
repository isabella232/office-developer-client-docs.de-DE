---
title: PROP_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PROP_ID
api_type:
- COM
ms.assetid: 6ddaced5-49bb-41fe-95da-4e3300883bf7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 765f1c0aae042721e2a03f6b22a7652786b50af3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550197"
---
# <a name="prop_id"></a>PROP_ID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den Eigenschaftsbezeichner eines angegebenen Eigenschaftstags zurück.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_ID (ulPropTag)
```

## <a name="parameters"></a>Parameter

 _ulPropTag_
  
> Eigenschaftstag, das den zurückzugebenden Bezeichner enthält.
    
## <a name="remarks"></a>HinwBemerkungeneise

Jedes Eigenschaftstag enthält den Eigenschaftstyp im Wort in niedriger Reihenfolge (Bits 0 bis 15) und den Eigenschaftsbezeichner im Hochkomma (Bits 16 bis 31). Das **PROP_ID** Makro extrahiert den Eigenschaftsbezeichner und fügt ihn in die Bits 0 bis 15 der ganzen Zahl ein, die zurückgegeben werden soll. Die verbleibenden Bits des Rückgabewerts werden auf Nullen festgelegt. 
  
Das **PROP_ID** Makro kann beispielsweise verwendet werden, um einen Bezeichner abzurufen, der an [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)übergeben werden soll. **GetNamesFromIDs** ruft den Eigenschaftennamen ab, der einem Bezeichner für eine benannte Eigenschaft zugeordnet ist. 
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)


[Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

