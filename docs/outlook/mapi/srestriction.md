---
title: SRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SRestriction
api_type:
- COM
ms.assetid: c12b4409-da6f-480b-87af-1e5baea2e8bd
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 319e41baedc69622314e10b2d5c37d54f849a8b2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566507"
---
# <a name="srestriction"></a>SRestriction

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt einen Filter zum Einschränken der Ansicht einer Tabelle auf bestimmte Zeilen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SRestriction
{
  ULONG rt;
  union
  {
    SComparePropsRestriction resCompareProps;
    SAndRestriction resAnd;
    SOrRestriction resOr;
    SNotRestriction resNot;
    SContentRestriction resContent;
    SPropertyRestriction resProperty;
    SBitMaskRestriction resBitMask;
    SSizeRestriction resSize;
    SExistRestriction resExist;
    SSubRestriction resSub;
    SCommentRestriction resComment;
  } res;
} SRestriction;

```

## <a name="members"></a>Members

 **Rt**
  
> Der Einschränkungstyp. Mögliche Werte sind: 
    
RES_AND 
  
> Eine  AND-Einschränkung, die eine bitweise **AND-Operation** auf eine Einschränkung anwendet. 
    
RES_BITMASK 
  
> Eine Bitmaskeneinschränkung, die eine Bitmaske auf einen Eigenschaftswert anwendet.
    
RES_COMMENT 
  
> Eine Kommentareinschränkung, die einen Kommentar einer Einschränkung zuweist.
    
RES_COMPAREPROPS 
  
> Eine Eigenschaftsvergleichseinschränkung, die zwei Eigenschaftswerte vergleicht.
    
RES_CONTENT 
  
> Eine Inhaltseinschränkung, die einen Eigenschaftswert nach bestimmten Inhalten durchsucht.
    
RES_EXIST 
  
> Eine vorhandene Einschränkung, die bestimmt, ob eine Eigenschaft unterstützt wird.
    
RES_NOT 
  
> Eine **NOT-Einschränkung,** die einen logischen **NOT-Vorgang** auf eine Einschränkung anwendet. 
    
RES_OR 
  
> Eine **OR-Einschränkung,** die einen logischen **OR-Vorgang** auf eine Einschränkung anwendet. 
    
RES_PROPERTY 
  
> Eine Eigenschaftseinschränkung, die bestimmt, ob ein Eigenschaftswert mit einem bestimmten Wert übereinstimmt.
    
RES_SIZE 
  
> Eine Größeneinschränkung, die bestimmt, ob ein Eigenschaftswert eine bestimmte Größe aufweist.
    
RES_SUBRESTRICTION 
  
> Eine Unterobjekteinschränkung, die eine Einschränkung auf die Anlagen oder Empfänger einer Nachricht anwendet.
    
 **res**
  
> Vereinigung von Einschränkungsstrukturen, die den anzuwendenden Filter beschreiben. Die spezifische Struktur, die im **Res-Element** enthalten ist, hängt vom Wert des **rt-Elements** ab. Die Zuordnung zwischen Einschränkungstyp und Struktur ist in der folgenden Tabelle aufgeführt. 
    
|||
|:-----|:-----|
|**Einschränkungstyp** <br/> |**Einschränkungsstruktur** <br/> |
|RES_AND  <br/> |[SAndRestriction](sandrestriction.md) <br/> |
|RES_BITMASK  <br/> |[SBitMaskRestriction](sbitmaskrestriction.md) <br/> |
|RES_COMMENT  <br/> |[SCommentRestriction](scommentrestriction.md) <br/> |
|RES_COMPAREPROPS  <br/> |[SComparePropsRestriction](scomparepropsrestriction.md) <br/> |
|RES_CONTENT  <br/> |[SContentRestriction](scontentrestriction.md) <br/> |
|RES_EXIST  <br/> |[SExistRestriction](sexistrestriction.md) <br/> |
|RES_NOT  <br/> |[SNotRestriction](snotrestriction.md) <br/> |
|RES_OR  <br/> |[SOrRestriction](sorrestriction.md) <br/> |
|RES_PROPERTY  <br/> |[SPropertyRestriction](spropertyrestriction.md) <br/> |
|RES_SIZE  <br/> |[SSizeRestriction](ssizerestriction.md) <br/> |
|RES_SUBRESTRICTION  <br/> |[SSubRestriction](ssubrestriction.md) <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Clients verwenden eine **SRestriction-Struktur,** um die Anzahl und den Typ von Zeilen in ihrer Ansicht einer Tabelle einzuschränken und nach bestimmten Nachrichten in einem Ordner zu suchen. Um die Einschränkung für eine Tabelle aufzuerlegen, rufen Clients [entweder IMAPITable::Restrict](imapitable-restrict.md) oder [IMAPITable::FindRow](imapitable-findrow.md)auf. Um die Einschränkung für einen Ordner aufzuerlegen, rufen Clients die [IMAPIContainer::SetSearchCriteria-Methode](imapicontainer-setsearchcriteria.md) des Ordners auf. 
  
Informationen zur Verwendung von Einschränkungen in Tabellen finden Sie unter ["Einschränkungen".](about-restrictions.md) 
  
## <a name="see-also"></a>Siehe auch



[SAndRestriction](sandrestriction.md)
  
[SBitMaskRestriction](sbitmaskrestriction.md)
  
[SCommentRestriction](scommentrestriction.md)
  
[SComparePropsRestriction](scomparepropsrestriction.md)
  
[SContentRestriction](scontentrestriction.md)
  
[SExistRestriction](sexistrestriction.md)
  
[SNotRestriction](snotrestriction.md)
  
[SOrRestriction](sorrestriction.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[SSizeRestriction](ssizerestriction.md)
  
[SSubRestriction](ssubrestriction.md)


[MAPI-Strukturen](mapi-structures.md)

