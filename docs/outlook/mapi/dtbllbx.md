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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2bff20af2b3e9ea4e203e38ae38a8bc19074a727
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438568"
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
  
> Bitmaske von Flags, die verwendet werden, um eine horizontale oder vertikale Bildlaufleiste aus der Liste zu entfernen. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_NO_HBAR 
  
> Es sollte keine horizontale Bildlaufleiste mit der Liste angezeigt werden.
    
MAPI_NO_VBAR 
  
> Es sollte keine vertikale Bildlaufleiste mit der Liste angezeigt werden.
    
 **ulPRSetProperty**
  
> Eigenschaftstag für eine Eigenschaft eines beliebigen Typs. Diese Eigenschaft ist eine der Spalten in der Tabelle, die vom **ulPRTableTable-Element identifiziert** wird. 
    
 **ulPRTableName**
  
> Property tag for a table property of type PT_OBJECT that can be opened by using an **OpenProperty** call. Die Anzahl der Spalten, die die Tabelle enthalten soll, hängt davon ab, ob es sich bei der Liste um eine einzelne oder mehrere Auswahlliste handelt. Wenn das **ulPRSetProperty-Element** auf PR_NULL ([PidTagNull)](pidtagnull-canonical-property.md)festgelegt ist, ermöglicht die Liste die Mehrfachauswahl. 
    
## <a name="remarks"></a>Hinweise

Eine **DTBLLBX-Struktur** beschreibt eine Liste eines Steuerelements, das zum Anzeigen mehrerer Elemente verwendet wird und einem Benutzer die Auswahl eines oder mehrerer Elemente gestatten soll. 
  
Das **ulPRSetProperty-Mitglied** und **das ulPRTableName-Mitglied** arbeiten zusammen. Wenn ein Wert aus der Tabelle ausgewählt wird, wird er in **ulPRSetProperty** zurückgeschrieben, wenn das Dialogfeld verworfen wird. 
  
Der Flags-Wert gibt an, ob eine horizontale oder vertikale Bildlaufleiste mit der Liste angezeigt werden soll. Standardmäßig werden bei Bedarf Bildlaufleistentypen angezeigt. Dienstanbieter können festlegen MAPI_NO_HBAR eine horizontale Bildlaufleiste zu unterdrücken und MAPI_NO_VBAR vertikale Bildlaufleiste zu unterdrücken. 
  
Die beiden Eigenschaftentagmitglieder arbeiten zusammen, um Werte in der Liste anzeigen und entsprechende Eigenschaften festlegen, wenn ein Element in der Liste ausgewählt ist. Wenn MAPI die Liste zum ersten Mal anzeigt, ruft sie die **OpenProperty-Methode** der **IMAPIProp-Implementierung** auf, um die im **ulPRTableName-Element identifizierte Tabelle abzurufen.** Die Anzahl der Spalten in der Tabelle hängt vom Wert des **ulPRSetProperty-Mitglieds** ab. Wenn **ulPRSetProperty** auf **PR_NULL** festgelegt ist, handelt es sich bei der Liste um eine Liste mit mehreren Auswahllisten, die auf einem Objekt basiert, das Empfänger enthält, z. B. einen Adressbuchcontainer, eine Empfängertabelle für eine Nachricht oder eine Inhaltstabelle für Verteilerlisten. 
  
Eine Tabelle für eine Liste mit mehreren Auswahlen muss die folgenden Spalten enthalten:
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
  
 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
  
 **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
  
 **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) und maximal fünf weitere mehrwertige Zeichenfolgeneigenschaften können auch mit den drei erforderlichen Spalten angezeigt werden. 
  
Wenn das **ulPRSetProperty-Element** nicht auf PR_NULL **festgelegt** ist, handelt es sich bei der Liste um eine einzelne Auswahlliste. Der Anfangswert von **ulPRSetProperty** bestimmt die erste ausgewählte Zeile. Wenn ein Benutzer eine der Zeilen auswählt, wird das **element ulPRSetProperty** auf den ausgewählten Wert festgelegt, und dieser Wert wird mit einem Aufruf von [IMAPIProp::SetProps](imapiprop-setprops.md)in die Implementierung der Eigenschaftsschnittstelle geschrieben. 
  
Eine Übersicht über Anzeigetabellen finden Sie unter [Display Tables](display-tables.md). Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md).
  
## <a name="see-also"></a>Siehe auch



[DTCTL](dtctl.md)


[MAPI-Strukturen](mapi-structures.md)

