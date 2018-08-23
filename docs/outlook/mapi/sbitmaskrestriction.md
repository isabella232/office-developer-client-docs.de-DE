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
ms.openlocfilehash: c9197201388530bd7755eb1987ecc863220e3847
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566607"
---
# <a name="sbitmaskrestriction"></a>SBitMaskRestriction

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine Einschränkung Bitmaske, die eine bitweise **AND** -Operation ausführen und testen das Ergebnis verwendet wird. 
  
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
  
> Relationale Operator, der beschreibt, wie die Maske angegeben im **UlMask** -Member auf das Eigenschafts-Tag angewendet werden soll. Mögliche Werte sind wie folgt: 
    
BMR_EQZ 
  
> Führen Sie eine bitweise **AND** -Operation der Maske im **UlMask** -Member, mit der-Eigenschaft, die durch die **UlPropTag** Member und Test für gleich 0 (null). 
    
BMR_NEZ 
  
> Führen Sie eine bitweise **AND** -Operation der Maske im **UlMask** -Member, mit der-Eigenschaft, die durch die **UlPropTag** Member und Test für wird nicht gleich 0 (null). 
    
 **ulPropTag**
  
> Eigenschaftentag der-Eigenschaft auf der die Bitmaske angewendet wird.
    
 **ulMask**
  
> Bitmaske für die Eigenschaft identifizierten **UlPropTag**gelten.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die Struktur **SBitMaskRestriction** führt eine bitweise **AND** -Operation verwenden die Bitmaske beschrieben in das **UlMask** -Element, und der Wert der Eigenschaft vom **UlPropTag** Member beschrieben. Wenn das Ergebnis gleich NULL ist, wird die BMR_EQZ erfüllt. Wenn es ungleich NULL ist, d. h., ist mindestens eines der gleichen Bits als **UlMask**, verfügt der Eigenschaftswert dann BMR_NEZ erfüllt.
  
Weitere Informationen zu den **SBitMaskRestriction** Struktur und Einschränkungen im Allgemeinen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).
  
## <a name="see-also"></a>Siehe auch



[SRestriction](srestriction.md)


[MAPI-Strukturen](mapi-structures.md)

