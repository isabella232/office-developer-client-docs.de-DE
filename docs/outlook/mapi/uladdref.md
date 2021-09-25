---
title: UlAddRef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.UlAddRef
api_type:
- COM
ms.assetid: 9b897cbc-90b2-4c60-b5f1-dc78e7e7952d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 716be1cdd425b7c8f912d33cda875c20e427ea75
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578431"
---
# <a name="uladdref"></a>UlAddRef

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt eine alternative Möglichkeit zum Aufrufen der OLE-Methode **IUnknown::AddRef** bereit. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
ULONG UlAddRef(
  LPVOID punk
);
```

## <a name="parameters"></a>Parameter

 _Punk_
  
> [in] Zeiger auf eine von der **IUnknown-Schnittstelle** abgeleitete Schnittstelle, mit anderen Worten, jede MAPI-Schnittstelle. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_E_CALL_FAILED 
  
> Ein Fehler mit unerwartetem oder unbekanntem Ursprung verhinderte, dass der Vorgang abgeschlossen wurde.
    
## <a name="remarks"></a>HinwBemerkungeneise

 **UlAddRef** gibt den von der **IUnknown::AddRef-Methode** zurückgegebenen Wert zurück, bei dem es sich um den neuen Wert der Referenzanzahl für die Schnittstelle handelt. Der Wert ist ungleich Null. 
  
Weitere Informationen zu **IUnknown::AddRef** finden Sie unter [Implementieren der IUnknown-Schnittstelle.](implementing-the-iunknown-interface.md) 
  

