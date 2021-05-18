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
ms.openlocfilehash: 5256efbff734d4555ac263dd330e3349c789cd74
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406976"
---
# <a name="dtblcombobox"></a>DTBLCOMBOBOX

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt ein Kombinationsfeldsteuerelement, das in einem Dialogfeld verwendet wird, das aus einer Anzeigetabelle erstellt wird.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandtes Makro:  <br/> |[SizedDtblComboBox](sizeddtblcombobox.md) <br/> |
   
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
  
> Ein Offset vom Anfang der **DTBLCOMBOBOX-Struktur** zu einem Zeichenzeichenfolgenfilter, der einschränkungen (sofern möglich) zu den Zeichen beschreibt, die in das Bearbeitungssteuerelement des Kombinationsfelds eingegeben werden können. Der Filter wird nicht als regulärer Ausdruck interpretiert, und auf jedes eingegebene Zeichen wird derselbe Filter angewendet. Das Format des Filters lautet wie folgt: 
    
|**Zeichen**|**Beschreibung**|
|:-----|:-----|
| `*` <br/> |Jedes Zeichen ist zulässig (z. B.  `"*"` ).  <br/> |
| `[ ]` <br/> |Definiert eine Reihe von Zeichen (z. B.  `"[0123456789]"` ).  <br/> |
| `-` <br/> |Gibt einen Zeichenbereich an (z. B.  `"[a-z]"` ).  <br/> |
| `~` <br/> |Gibt an, dass diese Zeichen nicht zulässig sind. (z. B.  `"[~0-9]"` ).  <br/> |
| `\` <br/> |Wird verwendet, um eines der vorherigen Symbole anführungszeichen (z. B.  `"[\-\\\[\]]"` bedeutet -, \, [und ] Zeichen sind zulässig).  <br/> |
   
 **ulFlags**
  
> Bitmaske von Flags, die zum Festlegen des Formats des Zeichenzeichenfolgenfilters verwendet werden. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Der Filter hat das Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befindet sich der Filter im ANSI-Format.
    
 **ulNumCharsAllowed**
  
> Maximale Anzahl von Zeichen, die im Textfeld des Kombinationsfelds eingegeben werden können.
    
 **ulPRPropertyName**
  
> Eigenschaftstag für eine Eigenschaft vom Typ PT_TSTRING. 
    
 **ulPRTableName**
  
> Eigenschaftstag für eine Eigenschaft vom Typ PT_OBJECT, auf der eine **IMAPITable-Schnittstelle** mithilfe eines **OpenProperty-Aufrufs geöffnet werden** kann. Die Tabelle muss eine Spalte mit einer Eigenschaft enthalten, die denselben Typ wie die vom **ulPRPropertyName-Element identifizierte Eigenschaft** hat. Die Zeilen der Tabelle werden zum Auffüllen der Liste verwendet. 
    
## <a name="remarks"></a>Hinweise

Eine **DTBLCOMBOBOX-Struktur** beschreibt ein Kombinationsfeld ein Steuerelement, das aus einer Liste und einem Auswahlfeld besteht. In der Liste werden die Informationen angezeigt, aus denen ein Benutzer auswählen kann, und das Auswahlfeld zeigt die aktuelle Auswahl an. Das Auswahlfeld ist ein Bearbeitungssteuerelement, das auch zum Eingeben von Text verwendet werden kann, der noch nicht in der Liste enthalten ist. 
  
Die beiden Eigenschaftentagmitglieder arbeiten zusammen, um die Listenanzeige mit dem Bearbeitungssteuerelement zu koordinieren. Wenn MAPI das Kombinationsfeld zum ersten Mal anzeigt, ruft es die **OpenProperty-Methode** der **IMAPIProp-Implementierung** auf, die der Anzeigetabelle zugeordnet ist, um die Tabelle abzurufen, die durch das **ulPRTableName-Element** dargestellt wird. Diese Tabelle hat eine Spalte eine Spalte, die Werte für die Eigenschaft enthält, die durch das **ulPRPropertyName-Element dargestellt** wird. Daher muss diese Spalte denselben Typ wie die **ulPRPropertyName-Eigenschaft** haben, und beide Spalten müssen Zeichenzeichenfolgen sein. 
  
Die Werte für die Spalte werden im Listenabschnitt des Kombinationsfelds angezeigt. Daher ist **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) kein gültiges Eigenschaftstag für **ulPRPropertyName**. Wenn ein Benutzer eine der Zeilen auswählt oder neue Daten in das Textfeld einbetritt, wird die **ulPRPropertyName-Eigenschaft** auf den ausgewählten oder eingegebenen Wert festgelegt. 
  
Um einen anfänglichen Wert für das Bearbeitungssteuerelement anzuzeigen, ruft MAPI [IMAPIProp::GetProps](imapiprop-getprops.md) auf, um die Eigenschaftswerte für die Anzeigetabelle abzurufen. Wenn eine der abgerufenen Eigenschaften der Eigenschaft entspricht, die durch das **element ulPRPropertyName** dargestellt wird, wird ihr Wert zum Anfangswert. 
  
Eine Übersicht über Anzeigetabellen finden Sie unter [Display Tables](display-tables.md). Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md).
  
## <a name="see-also"></a>Siehe auch



[DTCTL](dtctl.md)
  
[PidTagControlType (kanonische Eigenschaft)](pidtagcontroltype-canonical-property.md)


[MAPI-Strukturen](mapi-structures.md)

