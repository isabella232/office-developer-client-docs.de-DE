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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 288e34a159db48b1344524b87f02b045259f1565
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415845"
---
# <a name="ulrelease"></a>UlRelease

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bietet eine alternative Möglichkeit zum Aufrufen der OLE-Methode **IUnknown:: Release**. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
ULONG UlRelease(
  LPVOID punk
);
```

## <a name="parameters"></a>Parameter

 _Punk_
  
> in Zeiger auf eine von der **IUnknown** -Schnittstelle abgeleitete Schnittstelle, also jede MAPI-Schnittstelle. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_E_CALL_FAILED 
  
> Der Vorgang konnte nicht abgeschlossen werden.
    
## <a name="remarks"></a>Bemerkungen

Der Verweiszähler ist die Anzahl der vorhandenen Zeiger auf das Objekt, das freigegeben werden soll. 
  
Wenn der _Punk_ -Parameter NULL ist, wird die Funktion sofort zurückgegeben, ohne **IUnknown:: Release** zu aufrufen.
  
 **UlRelease** gibt den von der **IUnknown:: Release** -Methode zurückgegebenen Wert zurück, der mit dem Verweiszähler für das freizugebende Objekt übereinstimmen kann. 
  
Weitere Informationen zu **IUnknown:: Release**finden Sie unter [Implementieren der IUnknown-Schnittstelle](implementing-the-iunknown-interface.md). 
  

