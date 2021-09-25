---
title: UlPropSize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.UlPropSize
api_type:
- COM
ms.assetid: 240f1144-0805-4cd1-9e7d-f2a550a2f160
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: faf7ce0488584168ca0a73c13c835b18c5f89472
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566255"
---
# <a name="ulpropsize"></a>UlPropSize

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die Größe eines einzelnen Eigenschaftswerts zurück. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
ULONG UlPropSize(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a>Parameter

 _lpSPropValue_
  
> [in] Zeiger auf eine [SPropValue-Struktur,](spropvalue.md) die die zu messende Eigenschaft definiert. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_E_CALL_FAILED 
  
> Ein Fehler mit unerwartetem oder unbekanntem Ursprung verhinderte, dass der Vorgang abgeschlossen wurde.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **UlPropSize-Funktion** gibt die Größe des Eigenschaftswerts für die angegebene Eigenschaft in Bytes zurück. Die Größe des Rests der **SPropValue-Struktur** wird ignoriert. 
  

