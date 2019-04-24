---
title: DTBLLBX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLLBX
api_type:
- COM
ms.assetid: 971b4837-6823-4f28-9803-3c22b2ec091f
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2bff20af2b3e9ea4e203e38ae38a8bc19074a727
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321235"
---
# <a name="dtbllbx"></a>DTBLLBX

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine Liste, die in einem Dialogfeldverwendet wird, das aus einer Anzeigetabelle erstellt wird.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _DTBLLBX
{
  ULONG ulFlags;
  ULONG ulPRSetProperty;
  ULONG ulPRTableName;
} DTBLLBX, FAR *LPDTBLLBX

```

## <a name="members"></a>Elemente

 **ulFlags**
  
> Bitmaske der Flags, die verwendet werden, um eine horizontale oder vertikale Bildlaufleiste aus der Liste zu entfernen. Die folgenden Flags können festgelegt werden:
    
MAPI_NO_HBAR 
  
> Es sollte keine horizontale Bildlaufleiste mit der Liste angezeigt werden.
    
MAPI_NO_VBAR 
  
> Es sollte keine vertikale Bildlaufleiste mit der Liste angezeigt werden.
    
 **ulPRSetProperty**
  
> Property-Tag für eine Eigenschaft eines beliebigen Typs. Diese Eigenschaft ist eine der Spalten in der Tabelle, die durch das **ulPRTableTable** -Element identifiziert wird. 
    
 **ulPRTableName**
  
> Property-Tag für eine Table-Eigenschaft vom Typ PT_OBJECT, die mithilfe eines **openProperty** -Aufrufs geöffnet werden kann. Die Anzahl der Spalten, die die Tabelle aufweisen sollte, hängt davon ab, ob es sich bei der Liste um eine einzelne oder mehrere Auswahllisten handelt. Wenn das **ulPRSetProperty** -Element auf **PR_NULL** ([pidtagnull (](pidtagnull-canonical-property.md)) festgelegt ist, ermöglicht die Liste die Mehrfachauswahl.
    
## <a name="remarks"></a>Bemerkungen

Eine **DTBLLBX** -Struktur beschreibt eine Liste ein Steuerelement, das zum Anzeigen mehrerer Elemente verwendet wird, und lassen Sie einen Benutzer eines oder mehrere der Elemente auswählen. 
  
Das **ulPRSetProperty** -Element und das **ulPRTableName** -Element arbeiten zusammen; Wenn ein Wert aus der Tabelle ausgewählt wird, wird er zurück in **ulPRSetProperty** geschrieben, wenn das Dialogfeld geschlossen wird. 
  
Der Flags-Wert gibt an, ob eine horizontale oder vertikale Bildlaufleiste mit der Liste angezeigt werden soll. Der Standardwert ist, dass bei Bedarf Typen von Bildlaufleisten angezeigt werden. Dienstanbieter können festlegen, dass MAPI_NO_HBAR eine horizontale Bildlaufleiste und MAPI_NO_VBAR zum unterdrücken einer vertikalen Bildlaufleiste unterdrückt. 
  
Die beiden Elemente des Property-Tags arbeiten zusammen, um Werte in der Liste anzuzeigen und entsprechende Eigenschaften festzulegen, wenn ein Element in der Liste ausgewählt ist. Wenn die Liste von MAPI zuerst angezeigt wird, wird die OpenProperty **** -Methode der **IMAPIProp** -Implementierung aufgerufen, um die im **ulPRTableName** -Element identifizierte Tabelle abzurufen. Die Anzahl der Spalten in der Tabelle hängt vom Wert des **ulPRSetProperty** -Elements ab. Wenn **ulPRSetProperty** auf **PR_NULL**festgelegt ist, handelt es sich bei der Liste um eine Liste mit mehreren Auswahlen, die auf einem Objekt mit Empfängern wie einem Adressbuchcontainer, einer Empfängertabelle für eine Nachricht oder einer Tabelle mit Verteilerlisten Inhalten basiert. 
  
Eine Tabelle für eine Liste mit mehreren Auswahlen muss die folgenden Spalten enthalten:
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
  
 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
  
 **PR_INSTANCE_KEY** ([Pidtaginstancekey (](pidtaginstancekey-canonical-property.md))
  
 **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) und maximal fünf weitere Zeichenfolgeneigenschaften können auch mit den drei erforderlichen Spalten angezeigt werden. 
  
Wenn das **ulPRSetProperty** -Element nicht auf **PR_NULL**festgelegt ist, handelt es sich bei der Liste um eine einzelne Auswahlliste. Der Anfangswert von **ulPRSetProperty** bestimmt die erste ausgewählte Zeile. Wenn ein Benutzer eine der Zeilen auswählt, wird das **ulPRSetProperty** -Element auf den ausgewählten Wert festgelegt, und dieser Wert wird in die Implementierung der Property-Schnittstelle mit einem Aufruf von [IMAPIProp::](imapiprop-setprops.md)SetProps zurückgeschrieben. 
  
Eine Übersicht über Anzeige Tabellen finden Sie unter [Display Tables](display-tables.md). Weitere Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md).
  
## <a name="see-also"></a>Siehe auch



[DTCTL](dtctl.md)


[MAPI-Strukturen](mapi-structures.md)

