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
ms.openlocfilehash: 5f8a76cb317ac9bf1b6a4dc4a92b6d6f0098e1d7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577401"
---
# <a name="srestriction"></a>SRestriction

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Beschreibt einen Filter zum Einschränken der Ansicht in bestimmten Zeilen einer Tabelle. 
  
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

## <a name="members"></a>Elemente

 **RT**
  
> Der Typ der Einschränkung. Mögliche Werte sind wie folgt: 
    
RES_AND 
  
> Eine **AND** -Einschränkung, die eine bitweise **AND** -Operation für eine Beschränkung gilt. 
    
RES_BITMASK 
  
> Eine Bitmaske-Einschränkung, die eine Bitmaske mit einem Eigenschaftswert angewendet wird.
    
RES_COMMENT 
  
> Eine Einschränkung Kommentar, die einen Kommentar mit einer Einschränkung verknüpft.
    
RES_COMPAREPROPS 
  
> Einen Vergleich eigenschaftseinschränkung, die zwei Eigenschaftswerten vergleicht.
    
RES_CONTENT 
  
> Eine Content Einschränkung, die einen Eigenschaftswert nach bestimmten Inhalten sucht.
    
RES_EXIST 
  
> Eine Einschränkung vorhanden, die bestimmt, ob eine Eigenschaft unterstützt wird.
    
RES_NOT 
  
> Eine **nicht** Einschränkung, die eine logische **NOT** -Operation für eine Beschränkung gilt. 
    
RES_OR 
  
> Eine **oder** -Einschränkung, die eine logische **OR** -Operation für eine Beschränkung gilt. 
    
RES_PROPERTY 
  
> Eine eigenschaftseinschränkung, die bestimmt, ob der Wert einer Eigenschaft mit einem bestimmten Wert übereinstimmt.
    
RES_SIZE 
  
> Eine Einschränkung Größe, die bestimmt, ob der Wert einer Eigenschaft eine bestimmte Größe ist.
    
RES_SUBRESTRICTION 
  
> Eine Einschränkung Sub-Objekt, die eine Beschränkung auf Anlagen oder Empfänger einer Nachricht angewendet wird.
    
 **res**
  
> Union der Einschränkung Strukturen zur Beschreibung des Filters angewendet werden soll. Die spezifische Struktur im **Res** -Member enthalten, hängt von den Wert des Elements **rt** ab. Die Zuordnung zwischen mygal und Struktur wird in der folgenden Tabelle aufgeführt. 
    
|||
|:-----|:-----|
|**Einschränkungstyp** <br/> |**Struktur der Einschränkung** <br/> |
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

Clients verwenden eine **SRestriction** -Struktur, Anzahl und Typ der Zeilen in einer Tabelle ihre Ansicht einzuschränken und bestimmte Nachrichten in einem Ordner suchen. Um die Einschränkung für eine Tabelle zu erzwingen, rufen Clients [Methode IMAPITable:: Restrict](imapitable-restrict.md) oder [IMAPITable](imapitable-findrow.md). Um die Einschränkung für einen Ordner zu erzwingen, rufen Clients auf den Ordner [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) -Methode. 
  
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

