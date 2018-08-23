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
ms.openlocfilehash: d00a2ce3ebec24ca69875bdcb83066d8b891137a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585955"
---
# <a name="gettnefstreamcodepage"></a>GetTnefStreamCodepage

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Bestimmt die Codepage eines Streams Transport-Neutral Encapsulation Format (TNEF).
  
|||
|:-----|:-----|
|Headerdatei  <br/> |TNEF.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter.  <br/> |
   
```cpp
HRESULT GetTnefStreamCodepage(
  LPSTREAM lpStream,
  ULONG FAR * lpulCodepage,
  ULONG FAR * lpulSubCodepage
);
```

## <a name="parameters"></a>Parameter

 _lpStream_
  
> [in] Zeiger auf eine Speicher Stream-Objekt OLE **IStream** Schnittstelle, die beim Bereitstellen einer Datenquelle für eine TNEF-Nachricht Stream. 
    
 _lpulCodepage_
  
> [out] Zeiger auf die Codepage des Stream-Objekts.
    
 _lpulSubCodepage_
  
> [out] Zeiger auf der Seite Subcode des Stream-Objekts.
    
## <a name="return-value"></a>R�ckgabewert

 **S_OK**
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
 **MAPI_E_NOT_ENOUGH_DISK**
  
> Es wurde ein Fehler beim Lesen eines Attributs in der TNEF-Stream.
    
 **MAPI_E_CORRUPT_DATA**
  
> Entweder der Stream war nicht TNEF-Stream, oder es wurde ein Fehler beim Lesen des AttOemCodepage-Attributs.
    
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie die **GetTnefStreamCodepage** -Funktion, um das **AttOemCodepage** -Attribut des Datenstroms TNEF zum Bestimmen der Codepage und Subcode Seite lesen. Wenn **AttOemCodepage** nicht gefunden wird, gibt **GetTnefStreamCodepage** Codepage 437 und einer Seite Subcode 0 zurück. 
  
## <a name="see-also"></a>Siehe auch



[attOemCodepage](http://msdn.microsoft.com/en-us/library/ee158667%28EXCHG.80%29.aspx)

