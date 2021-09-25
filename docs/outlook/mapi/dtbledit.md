---
title: DTBLEDIT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.DTBLEDIT
api_type:
- COM
ms.assetid: ec3566a0-75ad-466d-a61e-f7d61ccb946d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 908cde20bf22f53df7e3025a1f47b623ce00f9e9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596512"
---
# <a name="dtbledit"></a>DTBLEDIT

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt ein Bearbeitungssteuerelement, das in einem Dialogfeld verwendet wird, das aus einer Anzeigetabelle erstellt wird.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandtes Makro:  <br/> |[SizedDtblEdit](sizeddtbledit.md) <br/> |
   
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
  
> Ein Offset vom Anfang der **DTBLEDIT-Struktur** zu einem Zeichenfolgenfilter, der ggf. Einschränkungen für die Zeichen beschreibt, die in das Bearbeitungssteuerelement eingegeben werden können. Der Filter wird nicht als regulärer Ausdruck interpretiert, und derselbe Filter wird auf jedes eingegebene Zeichen angewendet. Das Format des Filters lautet wie folgt: 
    
|**Zeichen**|**Beschreibung**|
|:-----|:-----|
| `*` <br/> |Ein beliebiges Zeichen ist zulässig (z. B.  `"*"` ).  <br/> |
| `[ ]` <br/> |Definiert einen Satz von Zeichen (z. B.  `"[0123456789]".` )  <br/> |
| `-` <br/> |Gibt einen Bereich von Zeichen an (z. B.  `"[a-z]"` ).  <br/> |
| `~` <br/> |Gibt an, dass diese Zeichen nicht zulässig sind (z. B.  `"[~0-9]"` ).  <br/> |
| `\` <br/> |Wird verwendet, um eines der vorherigen Symbole anführungszeichen (z. B.  `"[\-\\\[\]]"` "-"-" \, [und "]"-Zeichen sind zulässig).  <br/> |
   
 **ulFlags**
  
> Bitmaske mit Kennzeichen, die zum Festlegen des Formats des Zeichenfilters verwendet werden. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_UNICODE
  
> Der Filter hat das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, weist der Filter das ANSI-Format auf.
    
 **ulNumCharsAllowed**
  
> Maximale Anzahl von Zeichen, die der Benutzer in das Textfeld eingeben kann.
    
 **ulPropTag**
  
> Eigenschaftstag für eine Eigenschaft vom Typ PT_TSTRING. Der **ulPropTag-Member** identifiziert die Zeichenfolgeneigenschaft, deren Daten im Bearbeitungssteuerelement angezeigt und bearbeitet werden. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Eine **DTBLEDIT-Struktur** beschreibt ein Bearbeitungssteuerelement eines Bereichs in einem Dialogfeld, das alphanumerische Informationen enthält. Fast alle Dialogfelder verfügen über mindestens ein Bearbeitungssteuerelement. Bearbeitungssteuerelemente können von einem Benutzer geändert werden oder schreibgeschützt sein. 
  
Bearbeitungssteuerelemente können auch einzeilige oder mehrzeilige Bearbeitungssteuerelemente sein. Steuerelementen für mehrzeilige Bearbeitung ist in der Regel eine Bildlaufleiste zugeordnet. 
  
Eine Übersicht über Anzeigetabellen finden Sie unter ["Anzeigetabellen".](display-tables.md) Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle.](display-table-implementation.md)
  
## <a name="see-also"></a>Siehe auch



[DTCTL](dtctl.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[Kanonische PidTagControlType-Eigenschaft](pidtagcontroltype-canonical-property.md)


[MAPI-Strukturen](mapi-structures.md)

