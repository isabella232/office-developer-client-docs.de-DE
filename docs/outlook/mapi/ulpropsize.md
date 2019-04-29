---
title: UlPropSize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlPropSize
api_type:
- COM
ms.assetid: 240f1144-0805-4cd1-9e7d-f2a550a2f160
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: cc1547ad7d881b707825630f96987d4c40ad4863
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416902"
---
# <a name="ulpropsize"></a>UlPropSize

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die Größe eines einzelnen Eigenschaftswerts zurück. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
ULONG UlPropSize(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a>Parameter

 _lpSPropValue_
  
> in Zeiger auf eine [SPropValue](spropvalue.md) -Struktur, die die zu messende Eigenschaft definiert. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_E_CALL_FAILED 
  
> Der Vorgang konnte nicht abgeschlossen werden.
    
## <a name="remarks"></a>Bemerkungen

Die **UlPropSize** -Funktion gibt die Größe des Eigenschaftswerts für die angegebene Eigenschaft in Byte zurück. Die Größe des Rests der **SPropValue** -Struktur wird ignoriert. 
  

