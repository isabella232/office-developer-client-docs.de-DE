---
title: DTBLBUTTON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.DTBLBUTTON
api_type:
- COM
ms.assetid: 6058c78b-05d4-45a3-988c-1fbf8322125e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: beb61d82ae0fe07355e3501d6b8f4cda3fc7f405
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588102"
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

## <a name="members"></a>Members

 **ulbLpszLabel**
  
> Position im Speicher der Zeichenzeichenfolge, die auf der Schaltfläche angezeigt wird.
    
 **ulFlags**
  
> Bitmaske von Flags, die zum Festlegen des Formats der Bezeichnung verwendet werden, auf die vom **ulbLpszLabel-Element** verwiesen wird. Das folgende Kennzeichen kann festgelegt werden: 
    
MAPI_UNICODE 
  
> Die Beschriftung hat das Unicode-Format. Wenn das MAPI_UNICODE-Kennzeichen nicht festgelegt ist, hat die Bezeichnung das ANSI-Format.
    
 **ulPRControl**
  
> Eigenschaftstag für eine Eigenschaft vom Typ PT_OBJECT, die die [IMAPIControl-Schnittstelle](imapicontroliunknown.md) implementiert. Wenn auf die Schaltfläche geklickt wird, ruft MAPI die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) für die [IMAPIProp-Implementierung](imapipropiunknown.md) der Anzeigetabelle auf, um diese Eigenschaft abzurufen. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Eine **DTBLBUTTON-Struktur** beschreibt eine Schaltfläche eines Steuerelements, mit dem ein Benutzer, wenn darauf geklickt wird, einen Vorgang starten kann. In der Regel wird durch Klicken auf eine Schaltfläche ein modales Dialogfeld angezeigt oder eine programmgesteuerte Aufgabe aufgerufen. Dienstanbieter können alles über ein Schaltflächensteuerelement implementieren. Wenn die Schaltfläche eine Aufgabe basierend auf den Werten anderer Steuerelemente ausführen soll, müssen diese Steuerelemente das flag DT_SET_IMMEDIATE festgelegt haben. 
  
Der **ulbLpszLabel-Member** ist die Position im Speicher der Zeichenzeichenfolge, die auf der Schaltfläche angezeigt wird. Dienstanbieter können ein kaufmännisches Und-Zeichen &amp; () hinzufügen, um eine Windows Zugriffstaste in der Schaltflächenbeschriftung anzugeben. Das Drücken einer Tastenkombination hat denselben Effekt wie das Klicken auf die Schaltfläche. 
  
Der **ulPRControl-Member** beschreibt eine Objekteigenschaft, die beim Öffnen mit der **IMAPIProp::OpenProperty-Methode** einen Zeiger auf ein Steuerelementobjekt zurückgibt. Das Implementieren eines Steuerelementobjekts, das die **IMAPIControl-Schnittstelle** unterstützt, ist eine Möglichkeit, den MAPI-Featuresatz zu erweitern und den Vorgang oder die Aufgabe zu definieren, die beim Klicken auf die Schaltfläche auftritt. **IMAPIControl** stellt zwei Methoden zum Bearbeiten von Schaltflächen bereit: [GetState](imapicontrol-getstate.md) zum Deaktivieren oder Aktivieren von Schaltflächen und [Aktivieren](imapicontrol-activate.md) zum Verarbeiten von Schaltflächenklicks. 
  
Eine Übersicht über Anzeigetabellen finden Sie unter ["Anzeigetabellen".](display-tables.md) Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle.](display-table-implementation.md)
  
## <a name="see-also"></a>Siehe auch



[DTCTL](dtctl.md)


[MAPI-Strukturen](mapi-structures.md)

