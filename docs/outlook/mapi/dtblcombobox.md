---
title: DTBLCOMBOBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.DTBLCOMBOBOX
api_type:
- COM
ms.assetid: 73b68614-6aca-4669-b879-5631c5d6483c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 98dbb49fa6e09939cbb503df37e5b77e2f4c2d57
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551677"
---
# <a name="dtblcombobox"></a>DTBLCOMBOBOX

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt ein Kombinationsfeld-Steuerelement, das in einem aus einer Anzeigetabelle erstellten Dialogfeld verwendet wird.
  
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

## <a name="members"></a>Members

 **ulbLpszCharsAllowed**
  
> Ein Offset vom Anfang der **DTBLCOMBOBOX-Struktur** zu einem Zeichenfolgenfilter, der ggf. Einschränkungen für die Zeichen beschreibt, die in das Bearbeitungssteuerelement des Kombinationsfelds eingegeben werden können. Der Filter wird nicht als regulärer Ausdruck interpretiert, und derselbe Filter wird auf jedes eingegebene Zeichen angewendet. Das Format des Filters lautet wie folgt: 
    
|**Zeichen**|**Beschreibung**|
|:-----|:-----|
| `*` <br/> |Ein beliebiges Zeichen ist zulässig (z. B.  `"*"` ).  <br/> |
| `[ ]` <br/> |Definiert einen Satz von Zeichen (z. B.  `"[0123456789]"` ).  <br/> |
| `-` <br/> |Gibt einen Bereich von Zeichen an (z. B.  `"[a-z]"` ).  <br/> |
| `~` <br/> |Gibt an, dass diese Zeichen nicht zulässig sind. (z. B.  `"[~0-9]"` ).  <br/> |
| `\` <br/> |Wird verwendet, um eines der vorherigen Symbole anführungszeichen (z. B.  `"[\-\\\[\]]"` "-"-" \, [und "]"-Zeichen sind zulässig).  <br/> |
   
 **ulFlags**
  
> Bitmaske mit Flags, die zum Festlegen des Formats des Zeichenfolgenfilters verwendet werden. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_UNICODE 
  
> Der Filter hat das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, weist der Filter das ANSI-Format auf.
    
 **ulNumCharsAllowed**
  
> Maximale Anzahl von Zeichen, die in das Textfeld des Kombinationsfelds eingegeben werden können.
    
 **ulPRPropertyName**
  
> Eigenschaftstag für eine Eigenschaft vom Typ PT_TSTRING. 
    
 **ulPRTableName**
  
> Eigenschaftstag für eine Eigenschaft vom Typ PT_OBJECT, für die eine **IMAPITable-Schnittstelle** mithilfe eines **OpenProperty-Aufrufs** geöffnet werden kann. Die Tabelle muss eine Spalte mit einer Eigenschaft aufweisen, die denselben Typ wie die vom **ulPRPropertyName-Element** identifizierte Eigenschaft aufweist. Die Zeilen der Tabelle werden zum Auffüllen der Liste verwendet. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Eine **DTBLCOMBOBOX-Struktur** beschreibt ein Kombinationsfeld eines Steuerelements, das aus einer Liste und einem Auswahlfeld besteht. Die Liste enthält die Informationen, aus denen ein Benutzer auswählen kann, und das Auswahlfeld zeigt die aktuelle Auswahl an. Das Auswahlfeld ist ein Bearbeitungssteuerelement, das auch zum Eingeben von Text verwendet werden kann, der nicht bereits in der Liste enthalten ist. 
  
Die beiden Eigenschaftstagmitglieder arbeiten zusammen, um die Listenanzeige mit dem Bearbeitungssteuerelement zu koordinieren. Wenn die MAPI das Kombinationsfeld zum ersten Mal anzeigt, ruft sie die **OpenProperty-Methode** der **IMAPIProp-Implementierung** auf, die der Anzeigetabelle zugeordnet ist, um die vom **ulPRTableName-Element** dargestellte Tabelle abzurufen. Diese Tabelle enthält eine Spalte in einer Spalte, die Werte für die Eigenschaft enthält, die durch den **UlPRPropertyName-Member** dargestellt wird. Daher muss diese Spalte denselben Typ wie die **ulPRPropertyName-Eigenschaft** aufweisen, und beide Spalten müssen Zeichenzeichenfolgen sein. 
  
Die Werte für die Spalte werden im Listenabschnitt des Kombinationsfelds angezeigt. Daher ist **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) kein gültiges Eigenschaftstag für **ulPRPropertyName**. Wenn ein Benutzer eine der Zeilen auswählt oder neue Daten in das Textfeld eingibt, wird die **ulPRPropertyName-Eigenschaft** auf den ausgewählten oder eingegebenen Wert festgelegt. 
  
Um einen Anfangswert für das Bearbeitungssteuerelement anzuzeigen, ruft MAPI [IMAPIProp::GetProps](imapiprop-getprops.md) auf, um die Eigenschaftswerte für die Anzeigetabelle abzurufen. Wenn eine der abgerufenen Eigenschaften mit der vom **ulPRPropertyName-Element** dargestellten Eigenschaft übereinstimmt, wird der Wert zum Anfangswert. 
  
Eine Übersicht über Anzeigetabellen finden Sie unter ["Anzeigetabellen".](display-tables.md) Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle.](display-table-implementation.md)
  
## <a name="see-also"></a>Siehe auch



[DTCTL](dtctl.md)
  
[Kanonische PidTagControlType-Eigenschaft](pidtagcontroltype-canonical-property.md)


[MAPI-Strukturen](mapi-structures.md)

