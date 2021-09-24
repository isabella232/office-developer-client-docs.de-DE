---
title: SBitMaskRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SBitMaskRestriction
api_type:
- COM
ms.assetid: ddd42180-6e4f-410c-9f78-d868a91452dc
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8459e21becc85e3bee0603d5d8ade7f44ddee712
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550134"
---
# <a name="sbitmaskrestriction"></a>SBitMaskRestriction

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine Bitmaskeneinschränkung, die verwendet wird, um einen bitweisen **AND-Vorgang** auszuführen und das Ergebnis zu testen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SBitMaskRestriction
{
  ULONG relBMR;
  PT_LONG ulPropTag;
  ULONG ulMask;
} SBitMaskRestriction;

```

## <a name="members"></a>Members

 **relBMR**
  
> Relationaler Operator, der beschreibt, wie die im **ulMask-Element** angegebene Maske auf das Eigenschaftentag angewendet werden soll. Mögliche Werte sind: 
    
BMR_EQZ 
  
> Führen Sie eine bitweise **AND-Operation** der Maske im **ulMask-Element** durch, wobei die Eigenschaft durch das **ulPropTag-Element** dargestellt wird, und testen Sie, dass sie gleich Null ist. 
    
BMR_NEZ 
  
> Führen Sie eine bitweise **AND-Operation** der Maske im **ulMask-Element** durch, wobei die Eigenschaft durch das **ulPropTag-Element** dargestellt wird, und testen Sie, dass sie ungleich Null ist. 
    
 **ulPropTag**
  
> Eigenschaftstag der Eigenschaft, auf die die Bitmaske angewendet wird.
    
 **ulMask**
  
> Bitmaske, die auf die durch **ulPropTag** identifizierte Eigenschaft angewendet werden soll.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **SBitMaskRestriction-Struktur** führt einen bitweisen **AND-Vorgang** mithilfe der bitmaske aus, die im **ulMask-Element** und dem Wert der vom **ulPropTag-Element** beschriebenen Eigenschaft beschrieben wird. Wenn das Ergebnis Null ist, wird BMR_EQZ erfüllt. Wenn der Wert ungleich Null ist, d. h., wenn für den Eigenschaftswert mindestens eines der gleichen Bits wie **"ulMask"** festgelegt ist, wird BMR_NEZ erfüllt.
  
Weitere Informationen zur Struktur und Einschränkungen von **SBitMaskRestriction** im Allgemeinen finden Sie unter ["Informationen zu Einschränkungen".](about-restrictions.md)
  
## <a name="see-also"></a>Siehe auch



[SRestriction](srestriction.md)


[MAPI-Strukturen](mapi-structures.md)

