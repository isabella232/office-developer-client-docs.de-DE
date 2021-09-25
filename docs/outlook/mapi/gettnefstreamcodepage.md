---
title: GetTnefStreamCodepage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 0f22ccf2-1004-4731-9d68-f66c01b4588b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e1da4bca0307e69c36b9d8db2ee43be2c664aafc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614101"
---
# <a name="gettnefstreamcodepage"></a>GetTnefStreamCodepage

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bestimmt die Codepage für einen Transport-Neutral TNEF-Datenstrom (Encapsulation Format).
  
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
  
> [in] Zeiger auf eine OLE **IStream-Schnittstelle** eines Speicherdatenstromobjekts, die eine Quelle für eine TNEF-Streamnachricht bereitstellt. 
    
 _lpulCodepage_
  
> [out] Zeiger auf die Codeseite des Datenstroms.
    
 _lpulSubCodepage_
  
> [out] Zeiger auf die Untercodeseite des Datenstroms.
    
## <a name="return-value"></a>Rückgabewert

 **S_OK**
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
 **MAPI_E_NOT_ENOUGH_DISK**
  
> Beim Lesen eines Attributs im TNEF-Stream ist ein Fehler aufgetreten.
    
 **MAPI_E_CORRUPT_DATA**
  
> Entweder war der Datenstrom kein TNEF-Datenstrom, oder beim Lesen des AttOemCodepage-Attributs ist ein Fehler aufgetreten.
    
## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **GetTnefStreamCodepage-Funktion,** um das **attOemCodepage-Attribut** des TNEF-Datenstroms zu lesen, um die Codeseite und die Untercodeseite zu bestimmen. Wenn **attOemCodepage** nicht gefunden wird, gibt **GetTnefStreamCodepage** die Codepage 437 und die Untercodeseite 0 zurück. 
  
## <a name="see-also"></a>Siehe auch



[attOemCodepage](https://msdn.microsoft.com/library/ee158667%28EXCHG.80%29.aspx)

