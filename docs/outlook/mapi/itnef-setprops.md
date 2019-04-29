---
title: ITnefSetProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.SetProps
api_type:
- COM
ms.assetid: 09e4b427-316b-4630-9f3d-81e74f040d7b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f7372830624d774fb914ae956e86a9e4476cf487
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430791"
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
  
> in Eine Bitmaske von Flags, die steuert, wie Eigenschaftswerte festgelegt werden. Das folgende Flag kann festgelegt werden:
    
TNEF_PROP_CONTAINED 
  
> Codiert nur Eigenschaften aus der Nachricht oder Anlage, die durch den _ulElemID_ -Parameter angegeben wird. 
    
 _ulElemID_
  
> in Die **PR_ATTACH_NUM** ([pidtagattachnumber (](pidtagattachnumber-canonical-property.md))-Eigenschaft einer Anlage, die eine Zahl enthält, die die Anlage in der übergeordneten Nachricht eindeutig identifiziert.
    
 _cValues_
  
> in Die Anzahl der Eigenschaftswerte in der [SPropValue](spropvalue.md) -Struktur, auf die durch den _lpProps_ -Parameter verwiesen wird. 
    
 _lpProps_
  
> in Ein Zeiger auf eine **SPropValue** -Struktur, die die Eigenschaftswerte der festzulegenden Eigenschaften enthält. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich, und der erwartete Wert oder die Werte wurden zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

Transport Anbieter, Nachrichtenspeicher Anbieter und Gateways rufen die **ITnef::** SetProps-Methode auf, um die Eigenschaften festzulegen, die in die Kapselung einer Nachricht oder Anlage eingeschlossen werden sollen, ohne die ursprüngliche Nachricht oder Anlage zu ändern. Alle Eigenschaften, die mit diesem Aufruf festgelegt wurden, überschreiben vorhandene Eigenschaften in der gekapselte Nachricht. 
  
 **** SetProps wird nur für TNEF-Objekte unterstützt, die mit dem TNEF_ENCODE-Flag für die [OpenTnefStream](opentnefstream.md) -oder [OpenTnefStreamEx](opentnefstreamex.md) -Funktion geöffnet werden. Mit diesem Aufruf kann eine beliebige Anzahl von Eigenschaften festgelegt werden. 
  
> [!NOTE]
> Es erfolgt keine tatsächliche TNEF **** -Codierung für SetProps, bevor die [ITnef:: Finish](itnef-finish.md) -Methode aufgerufen wird. Diese Funktionalität bedeutet, dass Zeiger, **** die an SetProps übergeben werden, gültig bleiben müssen, bis der Aufruf **beendet** wurde. An diesem Punkt können alle Objekte und Daten, die **** an SetProps-Aufrufe übergeben werden, freigegeben oder freigeschaltet werden. 
  
## <a name="see-also"></a>Siehe auch



[ITnef::Finish](itnef-finish.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Kanonische Pidtagattachnumber (-Eigenschaft](pidtagattachnumber-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[ITnef : IUnknown](itnefiunknown.md)

