---
title: GetTnefStreamCodepage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0f22ccf2-1004-4731-9d68-f66c01b4588b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1e3d384f35726ff28bb47f3d537c8a7a1dda6dce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299433"
---
# <a name="gettnefstreamcodepage"></a>GetTnefStreamCodepage

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bestimmt die Codeseite für einen Transport-Neutral Encapsulation Format (TNEF).
  
|||
|:-----|:-----|
|Headerdatei  <br/> |tnef.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter.  <br/> |
   
```cpp
HRESULT GetTnefStreamCodepage(
  LPSTREAM lpStream,
  ULONG FAR * lpulCodepage,
  ULONG FAR * lpulSubCodepage
);
```

## <a name="parameters"></a>Parameter

 _lpStream_
  
> [in] Zeiger auf eine OLE **IStream-Schnittstelle** des Speicherdatenstromobjekts, die eine Quelle für eine TNEF-Streamnachricht bietet. 
    
 _lpulCodepage_
  
> [out] Zeiger auf die Codeseite des Datenstroms.
    
 _lpulSubCodepage_
  
> [out] Zeiger auf die Untercodeseite des Datenstroms.
    
## <a name="return-value"></a>Rückgabewert

 **S_OK**
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
 **MAPI_E_NOT_ENOUGH_DISK**
  
> Fehler beim Lesen eines Attributs im TNEF-Stream.
    
 **MAPI_E_CORRUPT_DATA**
  
> Entweder war der Datenstrom kein TNEF-Stream, oder es ist ein Fehler beim Lesen des attOemCodepage-Attributs aufgetreten.
    
## <a name="remarks"></a>Hinweise

Verwenden Sie **die GetTnefStreamCodepage-Funktion,** um das **attOemCodepage-Attribut** des TNEF-Datenstroms zu lesen, um die Codeseite und die Untercodeseite zu bestimmen. Wenn **attOemCodepage** nicht gefunden wird, gibt **GetTnefStreamCodepage** eine Codeseite von 437 und eine Untercodeseite von 0 zurück. 
  
## <a name="see-also"></a>Siehe auch



[attOemCodepage](https://msdn.microsoft.com/library/ee158667%28EXCHG.80%29.aspx)

