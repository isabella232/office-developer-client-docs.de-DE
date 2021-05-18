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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a8fa683fecd59ec813fee0c15d5b4f08084c645d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412786"
---
# <a name="dtblbutton"></a>DTBLBUTTON

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält Informationen zu einem Schaltflächensteuerelement für ein Dialogfeld, das aus einer Anzeigetabelle erstellt wurde.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandtes Makro:  <br/> |[SizedDtblButton](sizeddtblbutton.md) <br/> |
   
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
  
> Position im Arbeitsspeicher der Zeichenzeichenfolge, die auf der Schaltfläche angezeigt wird.
    
 **ulFlags**
  
> Bitmaske von Flags, die verwendet werden, um das Format der Bezeichnung zu bestimmen, auf das das **ulbLpszLabel-Element** verweist. Das folgende Flag kann festgelegt werden: 
    
MAPI_UNICODE 
  
> Die Bezeichnung ist im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befindet sich die Bezeichnung im ANSI-Format.
    
 **ulPRControl**
  
> Eigenschaftstag für eine Eigenschaft vom Typ PT_OBJECT, die die [IMAPIControl-Schnittstelle](imapicontroliunknown.md) implementiert. Wenn auf die Schaltfläche geklickt wird, ruft MAPI die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) auf, damit die [IMAPIProp-Implementierung](imapipropiunknown.md) der Anzeigetabelle diese Eigenschaft abruft. 
    
## <a name="remarks"></a>Hinweise

Eine **DTBLBUTTON-Struktur** beschreibt eine Schaltfläche, die einem Benutzer beim Klicken auf ein Steuerelement das Starten eines Vorgangs ermöglicht. In der Regel wird durch Klicken auf eine Schaltfläche ein modales Dialogfeld angezeigt oder eine programmgesteuerte Aufgabe aufgerufen. Dienstanbieter können alles über ein Schaltflächensteuerelement implementieren. Wenn die Schaltfläche eine Aufgabe basierend auf den Werten anderer Steuerelemente ausführen soll, müssen diese Steuerelemente das Flag DT_SET_IMMEDIATE haben. 
  
Das **ulbLpszLabel-Element** ist die Position im Speicher der Zeichenzeichenfolge, die auf der Schaltfläche angezeigt wird. Dienstanbieter können ein kaufmännisches Und -Zeichen ( ) hinzufügen, um eine Windows &amp; in der Schaltflächenbeschriftung anzugeben. Das Drücken einer Zugriffstaste hat dieselbe Auswirkung wie das Klicken auf die Schaltfläche. 
  
Das **ulPRControl-Element** beschreibt eine Objekteigenschaft, die beim Öffnen mit der **IMAPIProp::OpenProperty-Methode** einen Zeiger auf ein Steuerelementobjekt zurückgibt. Die Implementierung eines Steuerelementobjekts, das die **IMAPIControl-Schnittstelle** unterstützt, ist eine Möglichkeit, den MAPI-Featuresatz zu erweitern und den Vorgang oder die Aufgabe zu definieren, die beim Klicken auf die Schaltfläche ausgeführt wird. **IMAPIControl bietet** zwei Methoden zum Bearbeiten von Schaltflächen: [GetState](imapicontrol-getstate.md) zum Deaktivieren oder Aktivieren von Schaltflächen und [Aktivieren,](imapicontrol-activate.md) um Schaltflächenklicks zu verarbeiten. 
  
Eine Übersicht über Anzeigetabellen finden Sie unter [Display Tables](display-tables.md). Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md).
  
## <a name="see-also"></a>Siehe auch



[DTCTL](dtctl.md)


[MAPI-Strukturen](mapi-structures.md)

