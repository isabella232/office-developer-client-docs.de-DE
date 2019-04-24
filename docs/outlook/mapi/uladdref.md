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
ms.openlocfilehash: f9e55153830dbe41a2b4a48454157c900d96cf90
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315372"
---
# <a name="uladdref"></a>UlAddRef

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt eine alternative Möglichkeit zum Aufrufen der OLE-Methode **IUnknown:: AddRef**. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
ULONG UlAddRef(
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

 **UlAddRef** gibt den von der **IUnknown:: AddRef** -Methode zurückgegebenen Wert zurück, bei dem es sich um den neuen Wert des Verweiszählers für die Schnittstelle handelt. Der Wert ist ungleich NULL. 
  
Weitere Informationen zu **IUnknown:: AddRef**finden Sie unter [Implementieren der IUnknown-Schnittstelle](implementing-the-iunknown-interface.md). 
  

