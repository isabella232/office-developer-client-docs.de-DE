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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 49634bda487143ddd8d8806b94f6c451ccf57b75
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351317"
---
# <a name="sccountprops"></a>ScCountProps

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bestimmt die Größe eines Eigenschafts Wertarrays in Byte und überprüft den dem Array zugeordneten Arbeitsspeicher. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
SCODE ScCountProps(
  int cprop,
  LPSPropValue rgprop,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Parameter

 _cprop_
  
> in Die Anzahl der Eigenschaften im durch den _rgprop_ -Parameter angegebenen Array. 
    
 _rgprop_
  
> in Zeiger auf einen Bereich in einem Array von [SPropValue](spropvalue.md) -Strukturen, der die Eigenschaften definiert, deren Größe bestimmt werden soll. Dieser Bereich beginnt nicht unbedingt am Anfang des Arrays. 
    
 _PCB_
  
> Out Optionaler Zeiger auf die Größe des Eigenschaften Arrays in Byte.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_E_INVALID_PARAMETER 
  
> Mindestens eine Eigenschaft im Eigenschafts Wertarray hat einen Bezeichner von PROP_ID_NULL oder PROP_ID_INVALID, oder das Eigenschaftenarray enthält eine mehrwertige Eigenschaft ohne Eigenschaftswerte.
    
## <a name="remarks"></a>Bemerkungen

Wenn NULL im _PCB_ -Parameter übergeben wird, überprüft die **ScCountProps** -Funktion das Array der Benachrichtigungen, aber es erfolgt keine Zählung. Wenn ein Wert ungleich NULL in _PCB_übergeben wird, bestimmt die **ScCountNotifications** -Funktion die Größe des Arrays und speichert die Ursache _PCB_. Der _PCB_ -Parameter muss so hoch sein, dass er das gesamte Array enthält. 
  
Wie gezählt, überprüft **ScCountProps** den dem Array zugeordneten Arbeitsspeicher. **ScCountProps** funktioniert nur mit Eigenschaften, deren MAPI-Informationen enthält. 
  
## <a name="see-also"></a>Siehe auch



[PropCopyMore](propcopymore.md)

