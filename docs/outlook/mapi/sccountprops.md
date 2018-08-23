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
ms.openlocfilehash: ee004bdfb8d13537fd8823225f155223ebc76ca7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583351"
---
# <a name="sccountprops"></a>ScCountProps

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Legt fest, der ein Array der Eigenschaft Wert in Byte, und das Array zugeordneten Arbeitsspeicher überprüft. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
SCODE ScCountProps(
  int cprop,
  LPSPropValue rgprop,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Parameter

 _cprop_
  
> [in] Anzahl der Eigenschaften in das Array, das durch den Parameter _Rgprop_ angegeben. 
    
 _rgprop_
  
> [in] Zeiger auf einen Bereich in einem Array von [SPropValue](spropvalue.md) -Strukturen, die die Eigenschaften definiert, deren Größe bestimmt werden soll. In diesem Bereich wird am Anfang des Arrays nicht notwendigerweise gestartet. 
    
 _PCB_
  
> [out] Optional Zeiger auf die Größe des Arrays der Eigenschaft in Bytes.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_E_INVALID_PARAMETER 
  
> Mindestens eine Eigenschaft im Array-Wert Eigenschaft ist einen Bezeichner vom PROP_ID_NULL oder PROP_ID_INVALID, oder das Array-Eigenschaft enthält eine mehrwertige Eigenschaft keine-Eigenschaft Werte.
    
## <a name="remarks"></a>HinwBemerkungeneise

Wenn NULL in der _pcb_ -Parameter übergeben wird, wird die Funktion **ScCountProps** überprüft das Array von Benachrichtigungen, aber keine zählen erfolgt. Wenn Sie ein nicht-Nullwert _pcb_übergeben wird, wird die **ScCountNotifications** -Funktion bestimmt die Größe des Arrays und speichert die Ursache _pcb_. Der Parameter _pcb_ muss groß genug für das gesamte Array sein. 
  
Wie zählt, überprüft **ScCountProps** das Array zugeordneten Arbeitsspeicher. **ScCountProps** funktioniert nur mit Eigenschaften zu denen MAPI Informationen verfügt. 
  
## <a name="see-also"></a>Siehe auch



[PropCopyMore](propcopymore.md)

