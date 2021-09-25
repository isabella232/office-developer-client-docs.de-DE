---
title: IPersistMessageHandsOffMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPersistMessage.HandsOffMessage
api_type:
- COM
ms.assetid: 0e56b21d-0a2e-4fe6-83f4-c9daab2f3055
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5962da45d4b1cb6d0be53eb1a039657058e3df21
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587930"
---
# <a name="ipersistmessagehandsoffmessage"></a>IPersistMessage::HandsOffMessage

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bewirkt, dass das Formular seine aktuelle Nachricht freigibt.
  
```cpp
HRESULT HandsOffMessage( void );
```

## <a name="parameters"></a>Parameter

Keine
  
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Nachricht wurde erfolgreich freigegeben.
    
## <a name="remarks"></a>HinwBemerkungeneise

Formulare werden in zwei HandsOff-Zustände übergehen:
  
- [HandsOffAfterSave](handsoffaftersave-state.md)
    
- [HandsOffFromNormal](handsofffromnormal-state.md)
    
Wenn sich ein Formular in einem dieser Zustände befindet, wird es permanent gespeichert. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn ein Formularviewer die **IPersistMessage::HandsOffMessage-Methode** aufruft, während sich das Formular im [Normal-](normal-state.md) oder [NoScribble-Zustand](noscribble-state.md) befindet, rufen Sie **handsOffMessage** rekursiv für jede in die aktuelle Nachricht eingebettete Nachricht und die [IPersistStorage::HandsOffStorage-Methode](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) für jedes in die aktuelle Nachricht eingebettete OLE-Objekt auf. Geben Sie dann die aktuelle Nachricht und alle eingebetteten Nachrichten und OLE-Objekte frei. Wenn sich das Formular im Zustand "Normal" befand, wechseln Sie in den Zustand "HandsOffFromNormal". Wenn sich das Formular im NoScribble-Zustand befand, wechseln Sie in den Zustand HandsOffAfterSave. Rufen Sie nach einem erfolgreichen Übergang die [IUnknown::Release-Methode](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) der Nachricht auf, und geben Sie S_OK zurück. 
  
Wenn ein Formularviewer **HandsOffMessage** aufruft, während sich das Formular in einem der HandsOff-Zustände befindet, geben Sie E_UNEXPECTED zurück. 
  
Weitere Informationen zu den verschiedenen Zuständen eines Formulars finden Sie unter ["Formularstatus".](form-states.md) Weitere Informationen zum Arbeiten mit dem HandsOff-Zustand von Speicherobjekten finden Sie unter der [IPersistStorage::HandsOffStorage-Methode.](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) 
  
## <a name="see-also"></a>Siehe auch



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[Formularstatus](form-states.md)

