---
title: DTBLBUTTON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLBUTTON
api_type:
- COM
ms.assetid: 6058c78b-05d4-45a3-988c-1fbf8322125e
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2505f555fd8867fdc24a14f523a74b6f478a3e70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791598"
---
# <a name="dtblbutton"></a>DTBLBUTTON

  
  
**Betrifft**: Outlook 
  
Enthält Informationen über ein Button-Steuerelement für ein Dialogfeld erstellt aus einer Tabelle anzeigen.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Makro:  <br/> |[SizedDtblButton](sizeddtblbutton.md) <br/> |
   
```cpp
typedef struct _DTBLBUTTON
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRControl;
} DTBLBUTTON, FAR *LPDTBLBUTTON;

```

## <a name="members"></a>Elemente

 **ulbLpszLabel**
  
> Die Position im Speicher der Zeichenfolge, die auf der Schaltfläche angezeigt wird.
    
 **ulFlags**
  
> Bitmaske aus Flags verwendet, um das Format der Beschriftung festzulegen, auf die der **UlbLpszLabel** Member. Das folgende Flag kann festgelegt werden: 
    
PARAMETER MAPI_UNICODE 
  
> Die Beschriftung wird im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, ist die Bezeichnung im ANSI-Format.
    
 **ulPRControl**
  
> Eigenschaftentag für eine Eigenschaft vom Typ PT_OBJECT, die die [IMAPIControl](imapicontroliunknown.md) -Schnittstelle implementiert wird. Wenn die Schaltfläche geklickt wird, ruft MAPI die [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode für die Anzeige Tabelle [IMAPIProp](imapipropiunknown.md) Implementierung dieser Eigenschaft abgerufen. 
    
## <a name="remarks"></a>Bemerkungen

Eine Struktur **DTBLBUTTON** beschreibt eine Schaltfläche ein Steuerelement, das bei geklickt haben, kann sich einen Benutzer einen Vorgang beginnen. In der Regel wird eine Schaltfläche auf die ein modales Dialogfeld angezeigt werden oder eine programmtechnische Aufgabe aufgerufen werden. Dienstanbieter können alles über ein Button-Steuerelement implementieren. Wenn die Schaltfläche zum Ausführen einer Aufgabe basierend auf den Werten der andere Steuerelemente, müssen diese Steuerelemente das Flag DT_SET_IMMEDIATE festgelegt haben. 
  
Der **UlbLpszLabel** -Member ist die Position im Speicher der Zeichenfolge, die auf der Schaltfläche angezeigt wird. Dienstanbieter können kaufmännischen und-Zeichen hinzufügen (&amp;) an, dass ein Windows-Accelerator die Bezeichnung der Schaltfläche. Drücken der Zugriffstaste hat die gleiche Auswirkung wie das Klicken auf die Schaltfläche. 
  
Der **UlPRControl** -Member beschreibt-Eigenschaft eines Objekts, das beim Öffnen mit der **IMAPIProp::OpenProperty** -Methode gibt einen Zeiger auf ein Control-Objekt zurück. Ein Control-Objekt, das die **IMAPIControl** -Schnittstelle unterstützt die Implementierung ist eine Möglichkeit zum Erweitern der MAPI-Featuregruppe und legen Sie den Vorgang oder eine Aufgabe, das auftritt, wenn auf die Schaltfläche geklickt wird. **IMAPIControl** unterstützt zwei Methoden zum Bearbeiten von Schaltflächen: [GetState](imapicontrol-getstate.md) zu deaktivieren oder Aktivieren der Schaltflächen und [Aktivieren](imapicontrol-activate.md) , auf eine Schaltfläche zu behandeln. 
  
Eine Übersicht über die Anzeige Tabellen finden Sie unter [Tabellen angezeigt](display-tables.md). Informationen zum Implementieren einer Tabelle anzeigen finden Sie unter [Implementieren einer Tabelle anzuzeigen](display-table-implementation.md).
  
## <a name="see-also"></a>Siehe auch



[DTCTL](dtctl.md)


[MAPI-Strukturen](mapi-structures.md)

