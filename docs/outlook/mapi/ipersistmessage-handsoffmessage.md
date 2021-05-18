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
  
Bewirkt, dass das Formular seine aktuelle Nachricht veröffentlicht.
  
```cpp
HRESULT HandsOffMessage( void );
```

## <a name="parameters"></a>Parameter

Keine
  
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Nachricht wurde erfolgreich freigegeben.
    
## <a name="remarks"></a>Hinweise

Formulare werden in zwei HandsOff-Zustände übergewechselt:
  
- [HandsOffAfterSave](handsoffaftersave-state.md)
    
- [HandsOffFromNormal](handsofffromnormal-state.md)
    
Wenn sich ein Formular in einem dieser Zustände befindet, wird es dauerhaft gespeichert. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn ein Formularbetrachter die **IPersistMessage::HandsOffMessage-Methode** aufruft, während sich Ihr Formular im Normal- oder [NoScribble-Zustand](noscribble-state.md) befindet, rufen Sie für jede in die aktuelle Nachricht eingebettete Nachricht und die [IPersistStorage::HandsOffStorage-Methode](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) für jedes in die aktuelle Nachricht eingebettete OLE-Objekt rekursiv **HandsOffMessage** auf. [](normal-state.md) Geben Sie dann die aktuelle Nachricht und alle eingebetteten Nachrichten und OLE-Objekte frei. Wenn ihr Formular den Status Normal hatte, müssen Sie zum Status HandsOffFromNormal überwechseln. Wenn ihr Formular den Status "NoScribble" hatte, gehen Sie in den Status HandsOffAfterSave. Rufen Sie nach einem erfolgreichen Übergang die [IUnknown::Release-Methode](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) der Nachricht auf, und geben Sie S_OK. 
  
Wenn ein Formularbetrachter **HandsOffMessage aufruft,** während sich Ihr Formular in einem der HandsOff-Zustände befindet, geben Sie E_UNEXPECTED. 
  
Weitere Informationen zu den verschiedenen Zuständen eines Formulars finden Sie unter [Formularzustände](form-states.md). Weitere Informationen zum Arbeiten mit dem HandsOff-Status von Speicherobjekten finden Sie unter [der IPersistStorage::HandsOffStorage-Methode.](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) 
  
## <a name="see-also"></a>Siehe auch



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[Formularzustände](form-states.md)

