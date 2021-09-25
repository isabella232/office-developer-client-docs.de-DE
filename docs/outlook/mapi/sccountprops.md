---
title: ScCountProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.ScCountProps
api_type:
- COM
ms.assetid: 76e4cc52-e1a0-4e0b-a2a6-a17644f6b2e7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8933e0ea62caaaed2ece303fea380e812034724e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609537"
---
# <a name="sccountprops"></a>ScCountProps

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bestimmt die Größe eines Eigenschaftswertarrays in Byte und überprüft den dem Array zugeordneten Speicher. 
  
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
  
> [in] Anzahl der Eigenschaften im Array, die durch den  _rgprop-Parameter_ angegeben werden. 
    
 _rgprop_
  
> [in] Zeiger auf einen Bereich in einem Array von [SPropValue-Strukturen,](spropvalue.md) die die Eigenschaften definieren, deren Größe bestimmt werden soll. Dieser Bereich beginnt nicht unbedingt am Anfang des Arrays. 
    
 _Pcb_
  
> [out] Optionaler Zeiger auf die Größe des Eigenschaftenarrays in Bytes.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_E_INVALID_PARAMETER 
  
> Mindestens eine Eigenschaft im Eigenschaftswertarray weist den Bezeichner PROP_ID_NULL oder PROP_ID_INVALID auf, oder das Eigenschaftenarray enthält eine mehrwertige Eigenschaft ohne Eigenschaftswerte.
    
## <a name="remarks"></a>HinwBemerkungeneise

Wenn NULL im  _Parameter "parameters"_ übergeben wird, überprüft die **ScCountProps-Funktion** das Array von Benachrichtigungen, aber es wird keine Zählung durchgeführt. Wenn ein Nicht-NULL-Wert in _einem Arbeitsblatt_ übergeben wird, bestimmt die **ScCountNotifications-Funktion** die Größe des Arrays und speichert die _Ursache._ Der  _Parameter "parameters"_ muss groß genug sein, um das gesamte Array enthalten zu können. 
  
Bei der Zählung überprüft **ScCountProps** den dem Array zugeordneten Speicher. **ScCountProps** funktioniert nur mit Eigenschaften, zu denen MAPI Informationen enthält. 
  
## <a name="see-also"></a>Siehe auch



[PropCopyMore](propcopymore.md)

