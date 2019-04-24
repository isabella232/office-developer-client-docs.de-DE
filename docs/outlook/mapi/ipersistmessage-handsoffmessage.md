---
title: IPersistMessageHandsOffMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.HandsOffMessage
api_type:
- COM
ms.assetid: 0e56b21d-0a2e-4fe6-83f4-c9daab2f3055
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 84f0ca88403980ff9ea1c91821a8a3d7edae74fa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309716"
---
# <a name="ipersistmessagehandsoffmessage"></a>IPersistMessage::HandsOffMessage

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bewirkt, dass das Formular die aktuelle Nachricht freigibt.
  
```cpp
HRESULT HandsOffMessage( void );
```

## <a name="parameters"></a>Parameter

Keine
  
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Nachricht wurde erfolgreich veröffentlicht.
    
## <a name="remarks"></a>Bemerkungen

Formular Übergang in zwei HandsOff-Zustände:
  
- [HandsOffAfterSave](handsoffaftersave-state.md)
    
- [Status "handsofffromnormal](handsofffromnormal-state.md)
    
Wenn sich ein Formular in einem dieser Zustände befindet, wird es permanent gespeichert. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn ein Formular Betrachter die **IPersistMessage:: HandsOffMessage** -Methode aufruft, während sich das Formular im Status " [Normal](normal-state.md) " oder "noscribble" befindet, rufen Sie **HandsOffMessage** für jede in der aktuellen Nachricht eingebettete Nachricht rekursiv auf und [](noscribble-state.md) [ IPersistStorage:: HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) -Methode für jedes OLE-Objekt, das in die aktuelle Nachricht eingebettet ist. Geben Sie dann die aktuelle Nachricht und alle eingebetteten Nachrichten und OLE-Objekte frei. Wenn sich das Formular im Normal Zustand befand, wechseln Sie zum Status "handsofffromnormal-Zustand. Wenn sich das Formular im noScribble-Zustand befand, wechseln Sie zum HandsOffAfterSave-Zustand. Rufen Sie nach erfolgreichem Übergang die [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) -Methode der Nachricht auf, und geben Sie S_OK zurück. 
  
Wenn ein Formular-Viewer **HandsOffMessage** aufruft, während sich Ihr Formular in einem der HandsOff-Zustände befindet, geben Sie E_UNEXPECTED zurück. 
  
Weitere Informationen zu den verschiedenen Status eines Formulars finden Sie unter [Formular Status](form-states.md). Weitere Informationen zum Arbeiten mit dem HandsOff-Status von Speicherobjekten finden Sie unter der [IPersistStorage:: HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) -Methode. 
  
## <a name="see-also"></a>Siehe auch



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[Formular Status](form-states.md)

