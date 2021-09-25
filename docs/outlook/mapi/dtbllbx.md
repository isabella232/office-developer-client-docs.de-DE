---
title: DTBLLBX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.DTBLLBX
api_type:
- COM
ms.assetid: 971b4837-6823-4f28-9803-3c22b2ec091f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c14f79914619471e864968214e93a51d3e19f9db
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588119"
---
# <a name="dtbllbx"></a>DTBLLBX

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine Liste, die in einem Dialogfeld verwendet wird, das aus einer Anzeigetabelle erstellt wird.
  
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

## <a name="members"></a>Elemente

 **ulFlags**
  
> Bitmaske mit Flags, die verwendet werden, um eine horizontale oder vertikale Bildlaufleiste aus der Liste zu entfernen. Die folgenden Flags können festgelegt werden:
    
MAPI_NO_HBAR 
  
> Es sollte keine horizontale Bildlaufleiste mit der Liste angezeigt werden.
    
MAPI_NO_VBAR 
  
> In der Liste sollte keine vertikale Bildlaufleiste angezeigt werden.
    
 **ulPRSetProperty**
  
> Eigenschaftstag für eine Eigenschaft eines beliebigen Typs. Diese Eigenschaft ist eine der Spalten in der Tabelle, die vom **ulPRTable-Element** identifiziert wird. 
    
 **ulPRTableName**
  
> Eigenschaftstag für eine Tabelleneigenschaft vom Typ PT_OBJECT, die mithilfe eines **OpenProperty-Aufrufs** geöffnet werden kann. Die Anzahl der Spalten, die die Tabelle aufweisen sollte, hängt davon ab, ob es sich bei der Liste um eine einzelne oder eine Mehrfachauswahlliste handelt. Wenn der **ulPRSetProperty-Member** auf **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) festgelegt ist, ermöglicht die Liste die Mehrfachauswahl.
    
## <a name="remarks"></a>HinwBemerkungeneise

Eine **DTBLLBX-Struktur** beschreibt eine Liste eines Steuerelements, das verwendet wird, um mehrere Elemente anzuzeigen und einem Benutzer die Auswahl eines oder mehrerer Elemente zu ermöglichen. 
  
Das **Element "ulPRSetProperty"** und **"ulPRTableName"** arbeiten zusammen. Wenn ein Wert aus der Tabelle ausgewählt wird, wird er zurück in **ulPRSetProperty** geschrieben, wenn das Dialogfeld geschlossen wird. 
  
Der Flags-Wert gibt an, ob eine horizontale oder vertikale Bildlaufleiste mit der Liste angezeigt werden soll. Standardmäßig werden bildlaufleistentypen angezeigt, wenn dies erforderlich ist. Dienstanbieter können MAPI_NO_HBAR festlegen, um eine horizontale Bildlaufleiste zu unterdrücken, und MAPI_NO_VBAR, um eine vertikale Bildlaufleiste zu unterdrücken. 
  
Die beiden Eigenschaftstagmitglieder arbeiten zusammen, um Werte in der Liste anzuzeigen und entsprechende Eigenschaften festzulegen, wenn ein Element in der Liste ausgewählt wird. Wenn die MAPI die Liste zum ersten Mal anzeigt, ruft sie die **OpenProperty-Methode** der **IMAPIProp-Implementierung** auf, um die im **ulPRTableName-Element** identifizierte Tabelle abzurufen. Die Anzahl der Spalten in der Tabelle hängt vom Wert des **UlPRSetProperty-Elements** ab. Wenn **ulPRSetProperty** auf **PR_NULL** festgelegt ist, handelt es sich bei der Liste um eine Mehrfachauswahlliste basierend auf einem Objekt, das Empfänger enthält, z. B. einen Adressbuchcontainer, eine Empfängertabelle für eine Nachricht oder eine Verteilerlisten-Inhaltstabelle. 
  
Eine Tabelle für eine Mehrfachauswahlliste muss die folgenden Spalten enthalten:
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
  
 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
  
 **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
  
 **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) und maximal fünf weitere mehrwertige Zeichenfolgeneigenschaften können auch mit den drei erforderlichen Spalten angezeigt werden. 
  
Wenn der **ulPRSetProperty-Member** nicht auf **PR_NULL** festgelegt ist, handelt es sich bei der Liste um eine einzelne Auswahlliste. Der Anfangswert von **ulPRSetProperty** bestimmt die erste ausgewählte Zeile. Wenn ein Benutzer eine der Zeilen auswählt, wird das **Element ulPRSetProperty** auf den ausgewählten Wert festgelegt, und dieser Wert wird mit einem Aufruf von [IMAPIProp::SetProps](imapiprop-setprops.md)zurück in die Implementierung der Eigenschaftenschnittstelle geschrieben. 
  
Eine Übersicht über Anzeigetabellen finden Sie unter ["Anzeigetabellen".](display-tables.md) Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle.](display-table-implementation.md)
  
## <a name="see-also"></a>Siehe auch



[DTCTL](dtctl.md)


[MAPI-Strukturen](mapi-structures.md)

