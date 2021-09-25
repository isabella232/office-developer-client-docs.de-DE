---
title: IMSLogonCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMSLogon.CompareEntryIDs
api_type:
- COM
ms.assetid: 481812d6-8e94-4510-b288-55501dd5757c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 984be94199e5cf5f10c9231d6efaf2d04079f84c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556371"
---
# <a name="imslogoncompareentryids"></a>IMSLogon::CompareEntryIDs

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob sie auf dasselbe Objekt verweisen. MAPI verweist diesen Aufruf nur dann auf einen Dienstanbieter, wenn die eindeutigen Bezeichner (UIDs) in beiden zu vergleichenden Eintragsbezeichnern von diesem Anbieter verarbeitet werden.
  
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
  
> [in] Die Größe (in Byte) des Eintragsbezeichners, auf den der  _lpEntryID1-Parameter_  _verweist._
    
 _lpEntryID1_
  
> [in] Ein Zeiger auf den ersten Eintragsbezeichner, der verglichen werden soll.
    
 _cbEntryID2_
  
> [in] Die Größe (in Byte) des Eintragsbezeichners, auf den der  _lpEntryID2-Parameter_  _verweist._
    
 _lpEntryID2_
  
> [in] Ein Zeiger auf den zweiten Eintragsbezeichner, der verglichen werden soll.
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lpulResult_
  
> [out] Ein Zeiger auf das zurückgegebene Ergebnis des Vergleichs. TRUE, wenn die beiden Eintragsbezeichner auf dasselbe Objekt verweisen; andernfalls FALSE.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>HinwBemerkungeneise

Nachrichtenspeicheranbieter implementieren die **IMSLogon::CompareEntryIDs-Methode,** um zwei Eintragsbezeichner für einen bestimmten Eintrag in einem Nachrichtenspeicher zu vergleichen, um zu bestimmen, ob sie auf dasselbe Objekt verweisen. Wenn die beiden Eintragsbezeichner auf dasselbe Objekt verweisen, legt **CompareEntryIDs** den  _lpulResult-Parameter_ auf TRUE fest. wenn sie auf verschiedene Objekte verweisen, legt **CompareEntryIDs**  _lpulResult_ auf FALSE fest. 
  
 **CompareEntryIDs** ist nützlich, da ein Objekt mehrere gültige Eintragsbezeichner aufweisen kann. Dies kann beispielsweise auftreten, nachdem eine neue Version eines Nachrichtenspeicheranbieters installiert wurde. 
  
## <a name="see-also"></a>Siehe auch



[IMSLogon : IUnknown](imslogoniunknown.md)

