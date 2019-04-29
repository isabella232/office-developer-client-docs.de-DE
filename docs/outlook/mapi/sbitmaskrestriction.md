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
  
Beschreibt eine Bitmasken Einschränkung, die zum Durchführen einer bitweisen **and-** Operation und zum Testen des Ergebnisses verwendet wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
   
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
  
> Relationaler Operator, der beschreibt, wie die im **ulMask** -Element angegebene Maske auf das Property-Tag angewendet werden soll. Folgende Werte sind möglich: 
    
BMR_EQZ 
  
> Führen Sie eine bitweise **and** -Operation der Maske im **ulMask** -Element mit der vom **ulPropTag** -Element dargestellten Eigenschaft aus, und testen Sie, dass Sie gleich NULL ist. 
    
BMR_NEZ 
  
> Führen Sie eine bitweise **and** -Operation der Maske im **ulMask** -Element mit der vom **ulPropTag** -Element dargestellten Eigenschaft aus, und testen Sie, ob Sie ungleich NULL ist. 
    
 **ulPropTag**
  
> Property-Tag der Eigenschaft, auf die die Bitmaske angewendet wird.
    
 **ulMask**
  
> Bitmaske, die auf die durch **ulPropTag**angegebene Eigenschaft angewendet werden soll.
    
## <a name="remarks"></a>Bemerkungen

Die **SBitMaskRestriction** -Struktur führt eine bitweise **and** -Operation mit der im **ulMask** -Element beschriebenen Bitmaske und dem Wert der vom **ulPropTag** -Element beschriebenen Eigenschaft aus. Wenn das Ergebnis NULL ist, ist BMR_EQZ zufrieden. Wenn es ungleich NULL ist, das heißt, wenn der Eigenschaftswert mindestens eines der Bits hat, die als **ulMask**festgelegt sind, dann BMR_NEZ.
  
Weitere Informationen zur **SBitMaskRestriction** -Struktur und zu Einschränkungen im Allgemeinen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).
  
## <a name="see-also"></a>Siehe auch



[SRestriction](srestriction.md)


[MAPI-Strukturen](mapi-structures.md)

