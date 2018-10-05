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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384066"
---
# <a name="ipersistmessagehandsoffmessage"></a>IPersistMessage::HandsOffMessage

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bewirkt, dass das Formular, um die aktuelle Nachricht freigeben.
  
```cpp
HRESULT HandsOffMessage( void );
```

## <a name="parameters"></a>Parameter

Keine
  
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Nachricht wurde erfolgreich veröffentlicht.
    
## <a name="remarks"></a>Hinweise

Formulare Übergang in zwei HandsOff Zustände:
  
- [HandsOffAfterSave](handsoffaftersave-state.md)
    
- [HandsOffFromNormal](handsofffromnormal-state.md)
    
Wenn ein Formular in einem dieser Zustände ist, ist es gerade dauerhaft gespeichert werden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn ein Formular Viewer die **IPersistMessage::HandsOffMessage** -Methode aufruft, während das Formular im [Normal](normal-state.md) oder [NoScribble](noscribble-state.md) Zustand befindet, rekursiv Anruf **HandsOffMessage** für jede Nachricht in der aktuellen Nachricht und die [eingebettet. IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) -Methode für jedes OLE-Objekt in der aktuellen Nachricht eingebettet. Klicken Sie dann die aktuelle Nachricht freigeben, und alle eingebettete Nachrichten und OLE-Objekte. Wenn das Formular im Normalzustand Übergangs in den Zustand HandsOffFromNormal war. Wenn das Formular im NoScribble Zustand, Übergang in den Zustand HandsOffAfterSave war. Rufen Sie nach einem erfolgreichen Übergang die Nachricht [IUnknown](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) -Methode, und geben Sie S_OK zurück. 
  
Wenn ein Formular Viewer **HandsOffMessage** aufruft, während das Formular in einem der HandsOff Status ist, zurückgeben Sie E_UNEXPECTED. 
  
Weitere Informationen zu den unterschiedlichen Zustände eines Formulars finden Sie unter [Formular Zustände](form-states.md). Weitere Informationen dazu, wie Sie den Status HandsOff Speicherobjekte entwickelt finden Sie unter der [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) -Methode. 
  
## <a name="see-also"></a>Siehe auch



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[Formularstatus](form-states.md)

