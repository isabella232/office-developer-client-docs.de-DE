---
title: UlAddRef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlAddRef
api_type:
- COM
ms.assetid: 9b897cbc-90b2-4c60-b5f1-dc78e7e7952d
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: fc6c12d914e581c3f975e94809f0bdea73020099
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795769"
---
# <a name="uladdref"></a>UlAddRef

  
  
**Betrifft**: Outlook 
  
Bietet eine alternative Möglichkeit, die OLE-Methode **IUnknown:: AddRef**aufgerufen werden soll. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
ULONG UlAddRef(
  LPVOID punk
);
```

## <a name="parameters"></a>Parameter

 _pUnk_
  
> [in] Zeiger auf eine Schnittstelle abgeleitet die **IUnknown** -Schnittstelle, mit anderen Worten alle MAPI-Schnittstelle. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_E_CALL_FAILED 
  
> Ein Fehler unerwartete oder unbekannten Ursprungs verhindert den Abschluss des Vorgangs.
    
## <a name="remarks"></a>Hinweise

 **UlAddRef** gibt den Wert von der **IUnknown:: AddRef** -Methode zurückgegeben, die der neue Wert für den Referenzzähler für die Schnittstelle ist. Der Wert ist ungleich NULL. 
  
Weitere Informationen zu **IUnknown:: AddRef**finden Sie unter [die IUnknown-Schnittstelle implementieren](implementing-the-iunknown-interface.md). 
  

