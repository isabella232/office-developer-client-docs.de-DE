---
title: DTBLEDIT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLEDIT
api_type:
- COM
ms.assetid: ec3566a0-75ad-466d-a61e-f7d61ccb946d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b07ea265b5dcc6b9a9abb15c6be7ac9e0f94e8ed
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404680"
---
# <a name="dtbledit"></a>DTBLEDIT

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt ein Bearbeitungssteuerelement, das in einem von einer Anzeigetabelle erstellten Dialogfeldverwendet wird.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Zugehöriges Makro:  <br/> |[SizedDtblEdit](sizeddtbledit.md) <br/> |
   
```cpp
typedef struct _DTBLEDIT
{
  ULONG ulbLpszCharsAllowed;
  ULONG ulFlags;
  ULONG ulNumCharsAllowed;
  ULONG ulPropTag;
} DTBLEDIT, FAR *LPDTBLEDIT;

```

## <a name="members"></a>Members

 **ulbLpszCharsAllowed**
  
> Ein Offset vom Anfang der **DTBLEDIT** -Struktur zu einem Zeichenfolgenfilter, der ggf. Einschränkungen für die Zeichen beschreibt, die in das Bearbeitungssteuerelement eingegeben werden können. Der Filter wird nicht als regulärer Ausdruck interpretiert, und auf jedes eingegebene Zeichen wird derselbe Filter angewendet. Das Format des Filters lautet wie folgt: 
    
|**Zeichen**|**Beschreibung**|
|:-----|:-----|
| `*` <br/> |Ein beliebiges Zeichen ist zulässig (Beispiels `"*"`Weise).  <br/> |
| `[ ]` <br/> |Definiert eine Gruppe von Zeichen (beispielsweise `"[0123456789]".`).  <br/> |
| `-` <br/> |Gibt einen Zeichentyp an (beispielsweise `"[a-z]"`).  <br/> |
| `~` <br/> |Gibt an, dass diese Zeichen nicht zulässig sind (Beispiels `"[~0-9]"`Weise).  <br/> |
| `\` <br/> |Wird verwendet, um eines der vorherigen Symbole zu zitieren ( `"[\-\\\[\]]"` beispielsweise sind \, means-, [und] characters zulässig).  <br/> |
   
 **ulFlags**
  
> Bitmaske von Flags, die zum Festlegen des Formats des Zeichen Filters verwendet werden. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE
  
> Der Filter ist im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, ist der Filter im ANSI-Format.
    
 **ulNumCharsAllowed**
  
> Maximale Anzahl von Zeichen, die der Benutzer in das Textfeld eingeben kann.
    
 **ulPropTag**
  
> Property-Tag für eine Eigenschaft vom Typ PT_TSTRING. Das **ulPropTag** -Element identifiziert die String-Eigenschaft, deren Daten im Bearbeitungssteuerelement angezeigt und bearbeitet werden. 
    
## <a name="remarks"></a>Bemerkungen

Eine **DTBLEDIT** -Struktur beschreibt ein Bearbeitungssteuerelement einen Bereich in einem Dialogfeld, das alphanumerische Informationen enthält. Fast alle Dialogfelder verfügen über mindestens ein Bearbeitungssteuerelement. Bearbeitungssteuerelemente können von einem Benutzer oder schreibgeschützt geändert werden. 
  
Bearbeitungssteuerelemente können auch einzeilige oder Multiline sein. Multiline-Bearbeitungssteuerelemente haben normalerweise eine Bildlaufleiste zugeordnet. 
  
Eine Übersicht über Anzeige Tabellen finden Sie unter [Display Tables](display-tables.md). Weitere Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md).
  
## <a name="see-also"></a>Siehe auch



[DTCTL](dtctl.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[Kanonische Pidtagcontroltype (-Eigenschaft](pidtagcontroltype-canonical-property.md)


[MAPI-Strukturen](mapi-structures.md)

