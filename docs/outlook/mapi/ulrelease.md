---
title: UlRelease
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.UlRelease
api_type:
- COM
ms.assetid: 95db96ef-f95f-41da-b216-f717c23bffd2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6411a725ca786f7ae9143d32fc192aa0d721088d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578424"
---
# <a name="ulrelease"></a>UlRelease

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt eine alternative Möglichkeit zum Aufrufen der OLE-Methode **IUnknown::Release** bereit. 
  
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

 _Punk_
  
> [in] Zeiger auf eine von der **IUnknown-Schnittstelle** abgeleitete Schnittstelle, mit anderen Worten, jede MAPI-Schnittstelle. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_E_CALL_FAILED 
  
> Ein Fehler mit unerwartetem oder unbekanntem Ursprung verhinderte, dass der Vorgang abgeschlossen wurde.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die Referenzanzahl ist die Anzahl der vorhandenen Zeiger auf das Objekt, das losgelassen werden soll. 
  
Wenn der _Parameter "pun"_ NULL ist, wird die Funktion sofort zurückgegeben, ohne **IUnknown::Release** aufzurufen.
  
 **UlRelease** gibt den von der **IUnknown::Release-Methode** zurückgegebenen Wert zurück, der der Referenzanzahl für das freizugebende Objekt entsprechen kann. 
  
Weitere Informationen zu **IUnknown::Release** finden Sie unter [Implementieren der IUnknown-Schnittstelle.](implementing-the-iunknown-interface.md) 
  

