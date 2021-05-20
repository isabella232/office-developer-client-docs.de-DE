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

 **rt**
  
> Der Einschränkungstyp. Mögliche Werte sind: 
    
RES_AND 
  
> Eine **AND-Einschränkung,** die einen bitweisen **AND-Vorgang** auf eine Einschränkung angewendet wird. 
    
RES_BITMASK 
  
> Eine Bitmaskeneinschränkung, die eine Bitmaske auf einen Eigenschaftswert angewendet wird.
    
RES_COMMENT 
  
> Eine Kommentareinschränkung, die einen Kommentar einer Einschränkung zu ordnet.
    
RES_COMPAREPROPS 
  
> Eine Eigenschaftsvergleichseinschränkung, die zwei Eigenschaftswerte vergleicht.
    
RES_CONTENT 
  
> Eine Inhaltseinschränkung, die einen Eigenschaftswert nach bestimmten Inhalten durchsucht.
    
RES_EXIST 
  
> Eine exist-Einschränkung, die bestimmt, ob eine Eigenschaft unterstützt wird.
    
RES_NOT 
  
> Eine **NOT-Einschränkung,** die einen logischen **NOT-Vorgang** auf eine Einschränkung angewendet. 
    
RES_OR 
  
> Eine **OR-Einschränkung,** die einen logischen **OR-Vorgang** auf eine Einschränkung angewendet. 
    
RES_PROPERTY 
  
> Eine Eigenschaftseinschränkung, die bestimmt, ob ein Eigenschaftswert einem bestimmten Wert entspricht.
    
RES_SIZE 
  
> Eine Größeneinschränkung, die bestimmt, ob ein Eigenschaftswert eine bestimmte Größe ist.
    
RES_SUBRESTRICTION 
  
> Eine Unterobjekteinschränkung, die eine Einschränkung auf die Anlagen oder Empfänger einer Nachricht angewendet.
    
 **res**
  
> Union von Einschränkungsstrukturen, die den anzuwendende Filter beschreiben. Die spezifische Struktur, die im **res-Element** enthalten ist, hängt vom Wert des **rt-Mitglieds** ab. Die Zuordnung zwischen Einschränkungstyp und Struktur ist in der folgenden Tabelle aufgeführt. 
    
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
   
## <a name="remarks"></a>Hinweise

Clients verwenden eine **SRestriction-Struktur,** um die Anzahl und den Typ der Zeilen in ihrer Tabellenansicht zu begrenzen und nach bestimmten Nachrichten in einem Ordner zu suchen. Um eine Tabelle zu beschränken, rufen Clients [entweder IMAPITable::Restrict](imapitable-restrict.md) oder [IMAPITable::FindRow auf.](imapitable-findrow.md) Um die Einschränkung für einen Ordner zu verhängen, rufen Clients die [IMAPIContainer::SetSearchCriteria-Methode](imapicontainer-setsearchcriteria.md) des Ordners auf. 
  
Informationen zur Verwendung von Einschränkungen für Tabellen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md). 
  
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

