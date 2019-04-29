---
title: IMSLogonCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.CompareEntryIDs
api_type:
- COM
ms.assetid: 481812d6-8e94-4510-b288-55501dd5757c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4196ed8b949ecb9e23c4bd34380db9cc5a369e23
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410133"
---
# <a name="imslogoncompareentryids"></a>IMSLogon::CompareEntryIDs

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob Sie auf dasselbe Objekt verweisen. MAPI bezieht diesen Aufruf nur dann an einen Dienstanbieter, wenn die eindeutigen IDs (in beiden Eingabe Bezeichnern), die verglichen werden sollen, von diesem Anbieter verarbeitet werden.
  
```cpp
HRESULT CompareEntryIDs(
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG FAR * lpulResult
);
```

## <a name="parameters"></a>Parameter

 _cbEntryID1_
  
> in Die Größe der Eintrags-ID, auf die durch den _lpEntryID1_ -Parameter verwiesen wird, in Bytes _._
    
 _lpEntryID1_
  
> in Ein Zeiger auf den ersten zu vergleichenden Eintragsbezeichner.
    
 _cbEntryID2_
  
> in Die Größe der Eintrags-ID, auf die durch den _lpEntryID2_ -Parameter verwiesen wird, in Bytes _._
    
 _lpEntryID2_
  
> in Ein Zeiger auf die zweite Eintrags-ID, die verglichen werden soll.
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lpulResult_
  
> Out Ein Zeiger auf das zurückgegebene Ergebnis des Vergleichs. TRUE, wenn die beiden Eintragsbezeichner auf dasselbe Objekt verweisen, andernfalls false. andernfalls FALSE.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Bemerkungen

Nachrichtenspeicher Anbieter implementieren die **IMSLogon:: CompareEntryIDs** -Methode, um zwei Eintragsbezeichner für einen bestimmten Eintrag in einem Nachrichtenspeicher zu vergleichen, um zu bestimmen, ob Sie auf dasselbe Objekt verweisen. Wenn die beiden Eintragsbezeichner auf dasselbe Objekt verweisen, legt **CompareEntryIDs** den _lpulResult_ -Parameter auf true fest; Wenn Sie auf verschiedene Objekte verweisen, **CompareEntryIDs** _lpulResult_ auf false festgelegt. 
  
 **CompareEntryIDs** ist nützlich, da ein Objekt mehrere gültige Eintragsbezeichner aufweisen kann. Dies kann beispielsweise der Fall sein, nachdem eine neue Version eines Nachrichtenspeicher Anbieters installiert wurde. 
  
## <a name="see-also"></a>Siehe auch



[IMSLogon : IUnknown](imslogoniunknown.md)

