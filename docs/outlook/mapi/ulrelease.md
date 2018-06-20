---
title: UlRelease
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlRelease
api_type:
- COM
ms.assetid: 95db96ef-f95f-41da-b216-f717c23bffd2
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 5b34e2c21ac967b0874872986c0cf484750f4e72
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795791"
---
# <a name="ulrelease"></a>UlRelease

  
  
**Betrifft**: Outlook 
  
Bietet eine alternative Möglichkeit zum Aufrufen der OLE-Methode **IUnknown**. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
ULONG UlRelease(
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

Die Anzahl der Verweise ist die Anzahl der vorhandenen Zeiger auf das Objekt, das freigegeben werden muss. 
  
Wenn der Parameter _Punk_ NULL ist, gibt die Funktion sofort ohne einen Aufruf **IUnknown**
  
 **UlRelease** gibt den Wert zurückgegeben, die von der **IUnknown** -Methode, die den Referenzzähler für das Objekt, das freigegeben werden muss gleich sein kann. 
  
Weitere Informationen zu **IUnknown**finden Sie unter [die IUnknown-Schnittstelle implementieren](implementing-the-iunknown-interface.md). 
  

