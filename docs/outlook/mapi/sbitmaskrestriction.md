---
title: SBitMaskRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBitMaskRestriction
api_type:
- COM
ms.assetid: ddd42180-6e4f-410c-9f78-d868a91452dc
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: afac8c352ad0a07fcb1cd98683b6a5c87940ab4d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424476"
---
# <a name="sbitmaskrestriction"></a>SBitMaskRestriction

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine Bitmaskeneinschränkung, die verwendet wird, um einen bitweisen **AND-Vorgang** durchzuführen und das Ergebnis zu testen. 
  
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

## <a name="members"></a>Elemente

 **relBMR**
  
> Relationaler Operator, der beschreibt, wie die im **ulMask-Element** angegebene Maske auf das Eigenschaftstag angewendet werden soll. Mögliche Werte sind: 
    
BMR_EQZ 
  
> Führen Sie einen bitweisen **AND-Vorgang** der Maske im **ulMask-Element** aus, mit der Eigenschaft, die durch das **ulPropTag-Element** dargestellt wird, und testen Sie, ob sie gleich Null ist. 
    
BMR_NEZ 
  
> Führen Sie einen bitweisen **#A0** der Maske im **ulMask-Element** aus, mit der Eigenschaft, die durch das **ulPropTag-Element** dargestellt wird, und testen Sie, ob sie nicht gleich Null ist. 
    
 **ulPropTag**
  
> Eigenschaftstag der Eigenschaft, auf die die Bitmaske angewendet wird.
    
 **ulMask**
  
> Bitmaske, die auf die durch **ulPropTag** identifizierte Eigenschaft angewendet werden soll.
    
## <a name="remarks"></a>Hinweise

Die **SBitMaskRestriction-Struktur** führt einen bitweisen **#A0** mithilfe der im **ulMask-Element** beschriebenen Bitmaske und des Werts der Eigenschaft durch, die vom **ulPropTag-Element beschrieben** wird. Wenn das Ergebnis null ist, BMR_EQZ erfüllt. Wenn der Wert ungleich null ist, d. h. wenn der Eigenschaftswert mindestens einen der gleichen Bits wie **ulMask** festgelegt hat, ist BMR_NEZ erfüllt.
  
Weitere Informationen zur Struktur und Einschränkungen **von SBitMaskRestriction** im Allgemeinen finden Sie unter [About Restrictions](about-restrictions.md).
  
## <a name="see-also"></a>Siehe auch



[SRestriction](srestriction.md)


[MAPI-Strukturen](mapi-structures.md)

