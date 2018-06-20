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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d0418ac2ec5d01d58c63e4ad48a1066cc386e946
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791603"
---
# <a name="dtbledit"></a>DTBLEDIT

  
  
**Betrifft**: Outlook 
  
Beschreibt ein Edit-Steuerelement, das in einem Dialogfeld erstellt aus einer Tabelle anzeigen verwendet wird.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Makro:  <br/> |[SizedDtblEdit](sizeddtbledit.md) <br/> |
   
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
  
> Ein Offset ab dem Anfang der **DTBLEDIT** -Struktur zu einem Zeichen Zeichenfolge Filter, der Einschränkungen, falls vorhanden, auf die Zeichen beschreibt, die in das Bearbeitungssteuerelement eingegeben werden können. Der Filter wird nicht als regulärer Ausdruck interpretiert und der gleiche Filter auf jedes eingegebene Zeichen angewendet wird. Das Format des Filters lautet wie folgt: 
    
|**Zeichen**|**Beschreibung**|
|:-----|:-----|
| `*` <br/> |Ein beliebiges Zeichen ist zulässig (z. B. `"*"`).  <br/> |
| `[ ]` <br/> |Definiert eine Reihe von Zeichen (z. B. `"[0123456789]".`)  <br/> |
| `-` <br/> |Gibt einen Bereich von Zeichen (z. B. `"[a-z]"`).  <br/> |
| `~` <br/> |Gibt an, dass diese Zeichen nicht zulässig sind (beispielsweise `"[~0-9]"`).  <br/> |
| `\` <br/> |Verwendet, um die vorherigen Zeichen quote (z. B. `"[\-\\\[\]]"` bedeutet-, \, [, und] Zeichen sind zulässig).  <br/> |
   
 **ulFlags**
  
> Bitmaske aus Flags verwendet, um das Format des Filters Zeichen festzulegen. Das folgende Flag kann festgelegt werden:
    
PARAMETER MAPI_UNICODE
  
> Der Filter ist im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, ist der Filter im ANSI-Format.
    
 **ulNumCharsAllowed**
  
> Maximale Anzahl von Zeichen, die der Benutzer in das Textfeld eingeben kann.
    
 **ulPropTag**
  
> Eigenschaftentag für eine Eigenschaft vom Typ PT_TSTRING. Der **UlPropTag** Member identifiziert die Zeichenfolgeneigenschaft, deren Daten angezeigt und im Bearbeitungssteuerelement bearbeitet werden. 
    
## <a name="remarks"></a>Hinweise

Eine Struktur **DTBLEDIT** beschreibt ein Edit-Steuerelement einen Bereich in einem Dialogfeld, das alphanumerische Informationen enthält. Nahezu alle Dialogfelder verfügen über mindestens ein Edit-Steuerelement. Bearbeitungssteuerelemente können geändert werden, von einem Benutzer oder schreibgeschützt sein. 
  
Bearbeitungssteuerelemente können auch sein, einzelne Zeile oder die MultiLine-Eigenschaft. Mehrzeilige Bearbeitungssteuerelemente haben in der Regel eine Bildlaufleiste angezeigt. 
  
Eine Übersicht über die Anzeige Tabellen finden Sie unter [Tabellen angezeigt](display-tables.md). Informationen zum Implementieren einer Tabelle anzeigen finden Sie unter [Implementieren einer Tabelle anzuzeigen](display-table-implementation.md).
  
## <a name="see-also"></a>Siehe auch



[DTCTL](dtctl.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[Kanonische PidTagControlType-Eigenschaft](pidtagcontroltype-canonical-property.md)


[MAPI-Strukturen](mapi-structures.md)

