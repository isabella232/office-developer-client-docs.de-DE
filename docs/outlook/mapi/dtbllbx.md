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
ms.openlocfilehash: 04fbfb2e6938c1ae5971e90b30f5ef749e7963e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791604"
---
# <a name="dtbllbx"></a>DTBLLBX

  
  
**Betrifft**: Outlook 
  
Beschreibt eine Liste, die in einem Dialogfeld verwendet werden, die aus einer Tabelle anzeigen erstellt wird.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _DTBLLBX
{
  ULONG ulFlags;
  ULONG ulPRSetProperty;
  ULONG ulPRTableName;
} DTBLLBX, FAR *LPDTBLLBX

```

## <a name="members"></a>Members

 **ulFlags**
  
> Bitmaske von Flags, um eine horizontale oder vertikale Bildlaufleiste aus der Liste zu entfernen. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_NO_HBAR 
  
> Keine horizontale Bildlaufleiste angezeigt, die mit der Liste angezeigt werden soll.
    
MAPI_NO_VBAR 
  
> Keine vertikale Bildlaufleiste angezeigt, die mit der Liste angezeigt werden soll.
    
 **ulPRSetProperty**
  
> Eigenschaftentag für eine Eigenschaft eines beliebigen Typs. Diese Eigenschaft ist eine der Spalten in der Tabelle, die durch das **UlPRTableTable** -Element identifiziert. 
    
 **ulPRTableName**
  
> Rufen Sie die Eigenschaftentag für ein Table-Eigenschaft vom Typ PT_OBJECT, die mithilfe einer **OpenProperty** geöffnet werden können. Die Anzahl der Spalten, die die Tabelle verfügen soll, hängt davon ab, ob die Liste eine einzelne oder mehrere Auswahlliste enthält. Wenn das Element **UlPRSetProperty** **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) festgelegt ist, können die Liste für die Mehrfachauswahl.
    
## <a name="remarks"></a>Hinweise

Eine Struktur **DTBLLBX** beschreibt eine Liste ein Steuerelement, das verwendet wird, um mehrere Elemente anzeigen, und lassen Sie einen Benutzer ein oder mehrere Elemente auswählen. 
  
Die **UlPRSetProperty** und **UlPRTableName** arbeiten zusammen, Wenn ein Wert aus der Tabelle ausgewählt ist, wird sie wieder in **UlPRSetProperty** geschrieben, wenn das Dialogfeld geschlossen wird. 
  
Der Wert des Flags gibt an, ob eine horizontale oder vertikale Bildlaufleiste mit der Liste angezeigt werden soll. Die Standardmethode ist auf Typen von Rollen haben, die Bildlaufleisten angezeigt werden, wenn es erforderlich ist. Dienstanbieter können MAPI_NO_HBAR unterdrückt werden, eine horizontale Bildlaufleiste und MAPI_NO_VBAR unterdrückt werden, eine vertikale Bildlaufleiste festlegen. 
  
Die zwei-Eigenschaft Tag Member arbeiten zusammen, um Werte in der Liste anzeigen und die entsprechenden Eigenschaften festgelegt werden, wenn ein Element in der Liste ausgewählt wird. Wenn MAPI zuerst der Liste angezeigt wird, wird die **IMAPIProp** Implementierung **OpenProperty** -Methode zum Abrufen der Tabelle im **UlPRTableName** -Member identifiziert. Die Anzahl der Spalten in der Tabelle, hängt von den Wert des Elements **UlPRSetProperty** ab. Wenn **UlPRSetProperty** auf **PR_NULL**festgelegt ist, wird die Liste eine mehrere Auswahlliste basierend auf ein Objekt, Empfänger, wie ein Adressbuchcontainer, Tabellengröße Empfänger für eine Nachricht oder einer Verteilergruppe Liste Inhalt-Tabelle enthält. 
  
Eine Tabelle für eine mehrere Auswahlliste muss die folgenden Spalten enthalten:
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
  
 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
  
 **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
  
 **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) und bis zu fünf Zeichenfolgeneigenschaften andere mehrwertige kann auch mit den drei erforderlichen Spalten angezeigt werden. 
  
Wenn das Element **UlPRSetProperty** nicht auf **PR_NULL**festgelegt ist, ist die Liste eine einzelne Auswahlliste aus. Der Anfangswert der **UlPRSetProperty** bestimmt die zuerst ausgewählte Zeile. Wenn ein Benutzer eine der Zeilen auswählt, **UlPRSetProperty** Elements auf den ausgewählten Wert festgelegt ist, und dieser Wert wird zurück an die Implementierung der Eigenschaft-Schnittstelle mit einem Aufruf von [IMAPIProp::SetProps](imapiprop-setprops.md)geschrieben. 
  
Eine Übersicht über die Anzeige Tabellen finden Sie unter [Tabellen angezeigt](display-tables.md). Informationen zum Implementieren einer Tabelle anzeigen finden Sie unter [Implementieren einer Tabelle anzuzeigen](display-table-implementation.md).
  
## <a name="see-also"></a>Siehe auch



[DTCTL](dtctl.md)


[MAPI-Strukturen](mapi-structures.md)

