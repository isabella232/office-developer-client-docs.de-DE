---
title: ScCountProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCountProps
api_type:
- COM
ms.assetid: 76e4cc52-e1a0-4e0b-a2a6-a17644f6b2e7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 49634bda487143ddd8d8806b94f6c451ccf57b75
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404974"
---
# <a name="sccountprops"></a>ScCountProps

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bestimmt die Größe eines Eigenschaftswertarrays in Bytes und überprüft den dem Array zugeordneten Arbeitsspeicher. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
SCODE ScCountProps(
  int cprop,
  LPSPropValue rgprop,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Parameter

 _cprop_
  
> [in] Anzahl der Eigenschaften im Array, das durch den  _rgprop-Parameter angegeben_ wird. 
    
 _rgprop_
  
> [in] Zeiger auf einen Bereich in einem Array von [SPropValue-Strukturen,](spropvalue.md) der die Eigenschaften definiert, deren Größe bestimmt werden soll. Dieser Bereich beginnt nicht unbedingt am Anfang des Arrays. 
    
 _leiterplatte_
  
> [out] Optionaler Zeiger auf die Größe des Eigenschaftenarrays in Bytes.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_E_INVALID_PARAMETER 
  
> Mindestens eine Eigenschaft im Eigenschaftswertarray hat den Bezeichner PROP_ID_NULL oder PROP_ID_INVALID, oder das Eigenschaftenarray enthält eine mehrwertige Eigenschaft ohne Eigenschaftswerte.
    
## <a name="remarks"></a>Hinweise

Wenn NULL im  _Parameter "pcb"_ übergeben wird, überprüft die **ScCountProps-Funktion** das Array der Benachrichtigungen, es wird jedoch keine Zählung durchgeführt. Wenn ein Nicht-Null-Wert _in_ einer Leiterplatte übergeben wird, bestimmt die **ScCountNotifications-Funktion** die Größe des Arrays und speichert die Ursache _der Leiterplatte._ Der  _Parameter "pcb"_ muss groß genug sein, um das gesamte Array enthalten zu können. 
  
Während der Zählung **überprüft ScCountProps** den dem Array zugeordneten Arbeitsspeicher. **ScCountProps funktioniert** nur mit Eigenschaften, über die MAPI Über Informationen verfügt. 
  
## <a name="see-also"></a>Siehe auch



[PropCopyMore](propcopymore.md)

