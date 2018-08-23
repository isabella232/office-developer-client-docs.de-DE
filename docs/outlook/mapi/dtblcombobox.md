---
title: DTBLCOMBOBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLCOMBOBOX
api_type:
- COM
ms.assetid: 73b68614-6aca-4669-b879-5631c5d6483c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a8d2f2c82c61280bae88c715f8ffae19e10f00f9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577842"
---
# <a name="dtblcombobox"></a>DTBLCOMBOBOX

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Beschreibt ein Kombinationsfeld-Steuerelement, das in einem Dialogfeld erstellt aus einer Tabelle anzeigen verwendet wird.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Makro:  <br/> |[SizedDtblComboBox](sizeddtblcombobox.md) <br/> |
   
```cpp
typedef struct _DTBLCOMBOBOX
{
  ULONG ulbLpszCharsAllowed;
  ULONG ulFlags;
  ULONG ulNumCharsAllowed;
  ULONG ulPRPropertyName;
  ULONG ulPRTableName;
} DTBLCOMBOBOX, FAR *LPDTBLCOMBOBOX;

```

## <a name="members"></a>Elemente

 **ulbLpszCharsAllowed**
  
> Ein Offset ab dem Anfang der **DTBLCOMBOBOX** -Struktur zu einem Zeichen Zeichenfolge Filter, der Einschränkungen, wenn vorhanden, um die Zeichen, die in des Kombinationsfelds eingegeben werden können Bearbeitungssteuerelement beschreibt. Der Filter wird nicht als regulärer Ausdruck interpretiert und der gleiche Filter auf jedes eingegebene Zeichen angewendet wird. Das Format des Filters lautet wie folgt: 
    
|**Zeichen**|**Beschreibung**|
|:-----|:-----|
| `*` <br/> |Ein beliebiges Zeichen ist zulässig (z. B. `"*"`).  <br/> |
| `[ ]` <br/> |Definiert eine Reihe von Zeichen (z. B. `"[0123456789]"`).  <br/> |
| `-` <br/> |Gibt einen Bereich von Zeichen (z. B. `"[a-z]"`).  <br/> |
| `~` <br/> |Gibt an, dass diese Zeichen nicht zulässig sind. (z. B. `"[~0-9]"`).  <br/> |
| `\` <br/> |Verwendet, um die vorherigen Zeichen quote (z. B. `"[\-\\\[\]]"` bedeutet-, \, [, und] Zeichen sind zulässig).  <br/> |
   
 **ulFlags**
  
> Bitmaske aus Flags verwendet, um das Format des Filters Zeichen Zeichenfolge festzulegen. Das folgende Flag kann festgelegt werden:
    
PARAMETER MAPI_UNICODE 
  
> Der Filter ist im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, ist der Filter im ANSI-Format.
    
 **ulNumCharsAllowed**
  
> Maximale Anzahl von Zeichen, die im Textfeld des Kombinationsfelds eingegeben werden können.
    
 **ulPRPropertyName**
  
> Eigenschaftentag für eine Eigenschaft vom Typ PT_TSTRING. 
    
 **ulPRTableName**
  
> Eigenschaftentag für eine Eigenschaft vom Typ PT_OBJECT auf dem eine **IMAPITable** -Schnittstelle mithilfe eines Anrufs **OpenProperty** geöffnet werden kann. Die Tabelle muss eine Spalte mit einer Eigenschaft besitzen, die denselben Typ aufweist wie die-Eigenschaft, die durch das **UlPRPropertyName** -Element identifiziert. Die Zeilen der Tabelle dienen zum Auffüllen der Liste verwendet. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Eine Struktur **DTBLCOMBOBOX** beschreibt ein Kombinationsfeld ein Steuerelement, das eine Liste und ein Auswahlfeld besteht. Die Liste enthält die Informationen, die von dem ein Benutzer kann auswählen, und im Auswahlfeld zeigt die aktuelle Auswahl. Im Auswahlfeld ist ein Bearbeitungssteuerelement, die auch für die Texteingabe noch nicht in der Liste verwendet werden kann. 
  
Zwei-Eigenschaft Tag Mitglieder arbeiten zusammen, um die Anzeige der Browserliste mit dem Bearbeitungssteuerelement zu koordinieren. Wenn MAPI zunächst das Kombinationsfeld angezeigt wird, ruft es die **OpenProperty** -Methode der **IMAPIProp** -Implementierung, die die Tabelle anzeigen zum Abrufen der Tabelle, dargestellt durch das **UlPRTableName** -Element zugeordnet ist. Diese Tabelle hat eine Spalte eine Spalte, die Werte für die Eigenschaft, dargestellt durch das **UlPRPropertyName** -Element enthält. Aus diesem Grund diese Spalte muss vom gleichen Typ wie die **UlPRPropertyName** -Eigenschaft, und beide Spalten müssen Zeichenfolgen sein. 
  
Die Werte für die Spalte werden im Listenabschnitt des Kombinationsfelds angezeigt. Aus diesem Grund ist **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) keine gültige Eigenschaftentag für **UlPRPropertyName**. Wenn ein Benutzer eine der Zeilen auswählt, oder neue Daten in das Textfeld eingegeben, wird die **UlPRPropertyName** -Eigenschaft auf den ausgewählten oder eingegebenen Wert festgelegt. 
  
Um einen Anfangswert für das Bearbeitungssteuerelement anzuzeigen, ruft MAPI [IMAPIProp::GetProps](imapiprop-getprops.md) zum Abrufen der Eigenschaftswerte für die Anzeige-Tabelle. Wenn der abgerufenen Eigenschaften die Eigenschaft, dargestellt durch das **UlPRPropertyName** -Element entspricht, wird ihr Wert der Anfangswert. 
  
Eine Übersicht über die Anzeige Tabellen finden Sie unter [Tabellen angezeigt](display-tables.md). Informationen zum Implementieren einer Tabelle anzeigen finden Sie unter [Implementieren einer Tabelle anzuzeigen](display-table-implementation.md).
  
## <a name="see-also"></a>Siehe auch



[DTCTL](dtctl.md)
  
[PidTagControlType (kanonische Eigenschaft)](pidtagcontroltype-canonical-property.md)


[MAPI-Strukturen](mapi-structures.md)

