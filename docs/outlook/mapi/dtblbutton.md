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
ms.openlocfilehash: a8fa683fecd59ec813fee0c15d5b4f08084c645d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338311"
---
# <a name="dtblbutton"></a>DTBLBUTTON

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält Informationen zu einem Schaltflächen-Steuerelement für ein Dialogfeld, das aus einer Anzeigetabelle erstellt wurde.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Zugehöriges Makro:  <br/> |[SizedDtblButton](sizeddtblbutton.md) <br/> |
   
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
  
> Position im Speicher der Zeichenfolge, die auf der Schaltfläche angezeigt wird.
    
 **ulFlags**
  
> Bitmaske der Flags, mit denen das Format der Bezeichnung festgelegt wird, auf die durch das **ulbLpszLabel** -Element verwiesen wird. Das folgende Flag kann festgelegt werden: 
    
MAPI_UNICODE 
  
> Die Bezeichnung ist im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, ist die Bezeichnung im ANSI-Format.
    
 **ulPRControl**
  
> Property-Tag für eine Eigenschaft vom Typ PT_OBJECT, die die [IMAPIControl](imapicontroliunknown.md) -Schnittstelle implementiert. Wenn auf die Schaltfläche geklickt wird, ruft MAPI die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode für die [IMAPIProp](imapipropiunknown.md) -Implementierung der Display-Tabelle auf, um diese Eigenschaft abzurufen. 
    
## <a name="remarks"></a>Bemerkungen

Eine **DTBLBUTTON** -Struktur beschreibt ein Schaltflächen-Steuerelement, mit dem ein Benutzer beim Klicken einen Vorgang beginnen kann. Wenn Sie auf eine Schaltfläche klicken, wird in der Regel ein modales Dialogfeld angezeigt oder eine programmgesteuerte Aufgabe aufgerufen. Dienstanbieter können beliebige Elemente über ein Schaltflächen-Steuerelement implementieren. Wenn die Schaltfläche eine Aufgabe basierend auf den Werten anderer Steuerelemente ausführen soll, müssen diese Steuerelemente das DT_SET_IMMEDIATE-Flag festgelegt haben. 
  
Das **ulbLpszLabel** -Element ist die Position im Arbeitsspeicher der Zeichenfolge, die auf der Schaltfläche angezeigt wird. Dienstanbieter können ein kaufmännisches und-&amp;Zeichen () hinzufügen, um einen Windows-Beschleuniger in der Schaltflächenbeschriftung anzugeben. Das Drücken einer Tastenkombination hat dieselbe Wirkung wie das Klicken auf die Schaltfläche. 
  
Das **ulPRControl** -Element beschreibt eine Objekteigenschaft, die beim Öffnen mit der **IMAPIProp:: OpenProperty** -Methode einen Zeiger auf ein Control-Objekt zurückgibt. Das Implementieren eines Control-Objekts, das die **IMAPIControl** -Schnittstelle unterstützt, stellt eine Möglichkeit dar, die MAPI-Featuregruppe zu erweitern und die Operation oder Aufgabe zu definieren, die beim Klicken auf die Schaltfläche auftritt. **IMAPIControl** stellt zwei Methoden zum Bearbeiten von Schaltflächen [](imapicontrol-getstate.md) bereit: GetState zum Deaktivieren oder Aktivieren von Schaltflächen und [aktivieren](imapicontrol-activate.md) zum Behandeln von Tastenklicks. 
  
Eine Übersicht über Anzeige Tabellen finden Sie unter [Display Tables](display-tables.md). Weitere Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md).
  
## <a name="see-also"></a>Siehe auch



[DTCTL](dtctl.md)


[MAPI-Strukturen](mapi-structures.md)

