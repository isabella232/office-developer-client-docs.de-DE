---
title: SRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRestriction
api_type:
- COM
ms.assetid: c12b4409-da6f-480b-87af-1e5baea2e8bd
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a2a6d273495df52adb83393dc5549b0872c8f6f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439359"
---
# <a name="srestriction"></a>SRestriction

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt einen Filter zum Einschränken der Ansicht einer Tabelle auf bestimmte Zeilen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
   
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

 **RT**
  
> Der Einschränkungs. Folgende Werte sind möglich: 
    
RES_AND 
  
> Eine **and-** Einschränkung, die eine bitweise **and-** Operation auf eine Einschränkung anwendet. 
    
RES_BITMASK 
  
> Eine Bitmasken Einschränkung, die eine Bitmaske auf einen Eigenschaftswert anwendet.
    
RES_COMMENT 
  
> Eine Kommentar Einschränkung, die einer Einschränkung einen Kommentar zuordnet.
    
RES_COMPAREPROPS 
  
> Eine Eigenschafts Vergleichs Einschränkung, die zwei Eigenschaftswerte vergleicht.
    
RES_CONTENT 
  
> Eine Inhaltseinschränkung, die einen Eigenschaftswert nach bestimmten Inhalten durchsucht.
    
RES_EXIST 
  
> Eine exist-Einschränkung, die bestimmt, ob eine Eigenschaft unterstützt wird.
    
RES_NOT 
  
> Eine **nicht** -Einschränkung, die einen logischen **Not** -Vorgang auf eine Einschränkung anwendet. 
    
RES_OR 
  
> Eine **oder** -Einschränkung, die eine logische **or** -Operation auf eine Einschränkung anwendet. 
    
RES_PROPERTY 
  
> Eine Eigenschaftseinschränkung, die bestimmt, ob ein Eigenschaftswert einem bestimmten Wert entspricht.
    
RES_SIZE 
  
> Eine Größeneinschränkung, die bestimmt, ob ein Eigenschaftswert eine bestimmte Größe aufweist.
    
RES_SUBRESTRICTION 
  
> Eine Unterobjekt Einschränkung, die eine Einschränkung auf die Anlagen oder Empfänger einer Nachricht anwendet.
    
 **res**
  
> Vereinigung von Einschränkungs Strukturen zur Beschreibung des anzuwendenden Filters. Die im **Res** -Element enthaltene spezifische Struktur hängt vom Wert des **RT** -Members ab. Die Zuordnung zwischen dem Einschränkungs und der Struktur ist in der folgenden Tabelle aufgeführt. 
    
|||
|:-----|:-----|
|**Einschränkungs** <br/> |**Einschränkungs Struktur** <br/> |
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
   
## <a name="remarks"></a>Bemerkungen

Clients verwenden eine **SRestriction** -Struktur, um die Anzahl und den Typ von Zeilen in der Ansicht einer Tabelle zu begrenzen und nach bestimmten Nachrichten in einem Ordner zu suchen. Um die Einschränkung für eine Tabelle aufzuerlegen, rufen die Clients entweder [IMAPITable:: Restrict](imapitable-restrict.md) oder [IMAPITable:: FindRow](imapitable-findrow.md)auf. Um die Einschränkung für einen Ordner aufzuerlegen, rufen die Clients die [IMAPIContainer:: SetSearchCriteria](imapicontainer-setsearchcriteria.md) -Methode des Ordners auf. 
  
Informationen zur Verwendung von Einschränkungen mit Tabellen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md). 
  
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

