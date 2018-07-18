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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 480a50bd8c3738ad7d0c178cb4cabfdecd15412e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792861"
---
# <a name="itnefsetprops"></a>ITnef::SetProps

  
  
**Betrifft**: Outlook 
  
Legt den Wert einer oder mehrerer Eigenschaften für eine gekapselte Nachricht oder Anlage ohne Ändern der ursprünglichen Nachricht oder Anlage fest. 
  
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
  
> [in] Eine Bitmaske aus Flags, die steuert, wie die-Eigenschaftswerte festgelegt sind. Das folgende Flag kann festgelegt werden:
    
TNEF_PROP_CONTAINED 
  
> Nur Eigenschaften aus der Nachricht oder einer Anlage, die durch den _UlElemID_ -Parameter angegebenen codiert. 
    
 _ulElemID_
  
> [in] Eine Anlage **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md))-Eigenschaft, die eine Zahl, eindeutig enthält identifiziert die Anlage in der übergeordneten Nachricht.
    
 _cValues_
  
> [in] Durch den Parameter _LpProps_ auf zeigt die Anzahl der Eigenschaftswerte in der Struktur [SPropValue](spropvalue.md) . 
    
 _lpProps_
  
> [in] Ein Zeiger auf eine **SPropValue** -Struktur, die Eigenschaftswerte der Eigenschaften enthält festlegen. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

Transport-Anbieter, Nachricht-Anbieter und Gateways Aufruf der **ITnef::SetProps** -Methode zum Festlegen der Eigenschaften zum Einschließen in die Kapselung einer Nachricht oder einer Anlage, ohne die ursprüngliche Nachricht oder Anlage zu ändern. Mit diesem Anruf festgelegten Eigenschaften außer Kraft setzen vorhandene Eigenschaften in die gekapselte Nachricht. 
  
 **SetProps** wird nur für TNEF-Objekten unterstützt, die mit dem TNEF_ENCODE-Flag für die Funktion [OpenTNEFStream nicht ausgeführt werden](opentnefstream.md) oder [OpenTnefStreamEx](opentnefstreamex.md) geöffnet werden. Mit diesem Anruf kann eine beliebige Anzahl von Eigenschaften festgelegt werden. 
  
> [!NOTE]
> Keine tatsächlichen TNEF-Codierung für **SetProps** geschieht erst, nachdem die [ITnef::Finish](itnef-finish.md) -Methode aufgerufen wird. Dies bedeutet, dass Zeiger in **SetProps** übergeben gültig bis bleiben müssen nach dem Anruf auf **Fertig stellen** . An dieser Stelle können alle Objekte und Daten in **SetProps** Aufrufe übergeben freigegeben oder freigegeben werden. 
  
## <a name="see-also"></a>Siehe auch



[ITnef::Finish](itnef-finish.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[PidTagAttachNumber (kanonische Eigenschaft)](pidtagattachnumber-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[ITnef : IUnknown](itnefiunknown.md)

