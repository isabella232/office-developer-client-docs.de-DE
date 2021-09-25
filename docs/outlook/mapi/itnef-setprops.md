---
title: ITnefSetProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ITnef.SetProps
api_type:
- COM
ms.assetid: 09e4b427-316b-4630-9f3d-81e74f040d7b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: beb4a8357e5170298078ea5f52b8585f28d14486
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561320"
---
# <a name="itnefsetprops"></a>ITnef::SetProps

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt den Wert einer oder mehrerer Eigenschaften für eine gekapselte Nachricht oder Anlage fest, ohne die ursprüngliche Nachricht oder Anlage zu ändern. 
  
```cpp
HRESULT SetProps(
  ULONG ulFlags,
  ULONG ulElemID,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie Eigenschaftswerte festgelegt werden. Das folgende Kennzeichen kann festgelegt werden:
    
TNEF_PROP_CONTAINED 
  
> Codiert nur Eigenschaften aus der Nachricht oder Anlage, die durch den  _ulElemID-Parameter_ angegeben wird. 
    
 _ulElemID_
  
> [in] Die eigenschaft **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) einer Anlage, die eine Zahl enthält, die die Anlage in der übergeordneten Nachricht eindeutig identifiziert.
    
 _cValues_
  
> [in] Die Anzahl der Eigenschaftswerte in der [SPropValue-Struktur,](spropvalue.md) auf die der  _lpProps-Parameter_ verweist. 
    
 _lpProps_
  
> [in] Ein Zeiger auf eine **SPropValue-Struktur,** die die Eigenschaftswerte der festzulegenden Eigenschaften enthält. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben.
    
## <a name="remarks"></a>HinwBemerkungeneise

Transportanbieter, Nachrichtenspeicheranbieter und Gateways rufen die **ITnef::SetProps-Methode** auf, um Eigenschaften festzulegen, die in die Kapselung einer Nachricht oder Anlage eingeschlossen werden sollen, ohne die ursprüngliche Nachricht oder Anlage zu ändern. Mit diesem Aufruf festgelegte Eigenschaften überschreiben vorhandene Eigenschaften in der gekapselten Nachricht. 
  
 **SetProps** wird nur für TNEF-Objekte unterstützt, die mit dem TNEF_ENCODE Flag für die [OpenTnefStream-](opentnefstream.md) oder [OpenTnefStreamEx-Funktion](opentnefstreamex.md) geöffnet werden. Mit diesem Aufruf kann eine beliebige Anzahl von Eigenschaften festgelegt werden. 
  
> [!NOTE]
> Es erfolgt keine tatsächliche TNEF-Codierung für **SetProps,** bis die [ITnef::Finish-Methode](itnef-finish.md) aufgerufen wurde. Diese Funktionalität bedeutet, dass an **SetProps** übergebene Zeiger bis nach dem Aufruf von **"Fertig stellen"** gültig bleiben müssen. An diesem Punkt können alle Objekte und Daten, die an **SetProps-Aufrufe** übergeben werden, freigegeben oder freigegeben werden. 
  
## <a name="see-also"></a>Siehe auch



[ITnef::Finish](itnef-finish.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[PidTagAttachNumber (kanonische Eigenschaft)](pidtagattachnumber-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[ITnef : IUnknown](itnefiunknown.md)

