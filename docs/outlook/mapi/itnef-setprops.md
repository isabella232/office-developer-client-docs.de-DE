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
  
Legt den Wert einer oder mehreren Eigenschaften für eine gekapselte Nachricht oder Anlage fest, ohne die ursprüngliche Nachricht oder Anlage zu ändern. 
  
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
  
> [in] Eine Bitmaske mit Flags, die steuert, wie Eigenschaftswerte festgelegt werden. Das folgende Flag kann festgelegt werden:
    
TNEF_PROP_CONTAINED 
  
> Codiert nur Eigenschaften aus der Nachricht oder Anlage, die durch den  _ulElemID-Parameter angegeben_ wird. 
    
 _ulElemID_
  
> [in] Die eigenschaft PR_ATTACH_NUM **(** [PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) einer Anlage, die eine Zahl enthält, die die Anlage in ihrer übergeordneten Nachricht eindeutig identifiziert.
    
 _cValues_
  
> [in] Die Anzahl der Eigenschaftswerte in der [SPropValue-Struktur,](spropvalue.md) auf die der  _lpProps-Parameter_ verweist. 
    
 _lpProps_
  
> [in] Ein Zeiger auf eine **SPropValue-Struktur,** die die Eigenschaftswerte der festgelegten Eigenschaften enthält. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben.
    
## <a name="remarks"></a>Hinweise

Transportanbieter, Nachrichtenspeicheranbieter und Gateways rufen die **ITnef::SetProps-Methode** auf, um Eigenschaften so zu festlegen, dass sie in die Kapselung einer Nachricht oder Anlage ohne Änderung der ursprünglichen Nachricht oder Anlage enthalten sind. Mit diesem Aufruf festgelegte Eigenschaften überschreiben vorhandene Eigenschaften in der gekapselten Nachricht. 
  
 **SetProps wird** nur für TNEF-Objekte unterstützt, die mit dem TNEF_ENCODE für die [OpenTnefStream-](opentnefstream.md) oder [OpenTnefStreamEx-Funktion geöffnet](opentnefstreamex.md) werden. Mit diesem Aufruf kann eine beliebige Anzahl von Eigenschaften festgelegt werden. 
  
> [!NOTE]
> Eine tatsächliche TNEF-Codierung für **SetProps** erfolgt erst, nachdem die [ITnef::Finish-Methode](itnef-finish.md) aufgerufen wurde. Diese Funktionalität bedeutet, dass Zeiger, die an **SetProps** übergeben werden, bis nach dem Aufruf von **Finish** gültig bleiben müssen. An diesem Punkt können alle an **SetProps-Aufrufe** übergebenen Objekte und Daten freigegeben oder freigegeben werden. 
  
## <a name="see-also"></a>Siehe auch



[ITnef::Finish](itnef-finish.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[PidTagAttachNumber (kanonische Eigenschaft)](pidtagattachnumber-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[ITnef : IUnknown](itnefiunknown.md)

