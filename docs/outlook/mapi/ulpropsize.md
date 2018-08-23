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
ms.openlocfilehash: 2bfe2841592987c530f6323db94834c1dcb64b2a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576638"
---
# <a name="ulpropsize"></a>UlPropSize

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Gibt die Größe des einen einzelnen Eigenschaftswert zurück. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
ULONG UlPropSize(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a>Parameter

 _lpSPropValue_
  
> [in] Zeiger auf eine [SPropValue](spropvalue.md) -Struktur definieren die Eigenschaft gemessen werden soll. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_E_CALL_FAILED 
  
> Ein Fehler unerwartete oder unbekannten Ursprungs verhindert den Abschluss des Vorgangs.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **UlPropSize** -Funktion gibt die Größe der Wert der Eigenschaft um für die angegebene Eigenschaft in Bytes zurück. Es ignoriert die Größe des den Rest der **SPropValue** Struktur. 
  

