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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: baf45fa33ca085f51a6f9c20f72ec1fd1545ad79
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592373"
---
# <a name="uladdref"></a>UlAddRef

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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
    
## <a name="remarks"></a>HinwBemerkungeneise

 **UlAddRef** gibt den Wert von der **IUnknown:: AddRef** -Methode zurückgegeben, die der neue Wert für den Referenzzähler für die Schnittstelle ist. Der Wert ist ungleich NULL. 
  
Weitere Informationen zu **IUnknown:: AddRef**finden Sie unter [die IUnknown-Schnittstelle implementieren](implementing-the-iunknown-interface.md). 
  

