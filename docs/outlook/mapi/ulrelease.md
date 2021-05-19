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
  
Bietet eine alternative Möglichkeit zum Aufrufen der OLE-Methode **IUnknown::Release**. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
ULONG UlRelease(
  LPVOID punk
);
```

## <a name="parameters"></a>Parameter

 _punk_
  
> [in] Zeiger auf eine Schnittstelle, die von der **IUnknown-Schnittstelle** abgeleitet ist, d. h. auf eine beliebige MAPI-Schnittstelle. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_E_CALL_FAILED 
  
> Ein Fehler mit unerwartetem oder unbekanntem Ursprung verhinderte den Abschluss des Vorgangs.
    
## <a name="remarks"></a>Hinweise

Die Referenzanzahl ist die Anzahl vorhandener Zeiger auf das zu freigegebene Objekt. 
  
Wenn der  _Parameter "punk"_ NULL ist, gibt die Funktion sofort ohne Aufruf von **IUnknown::Release zurück.**
  
 **UlRelease** gibt den von der **IUnknown::Release-Methode** zurückgegebenen Wert zurück, der der Referenzanzahl für das losgelassene Objekt entspricht. 
  
Weitere Informationen zu **IUnknown::Release finden** Sie unter [Implementing the IUnknown Interface](implementing-the-iunknown-interface.md). 
  

