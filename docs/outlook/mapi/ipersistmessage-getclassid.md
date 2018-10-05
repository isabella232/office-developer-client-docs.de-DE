---
title: IPersistMessageGetClassID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.GetClassID
api_type:
- COM
ms.assetid: 77eeb468-3432-4ccd-9c1e-1df9ce605193
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3f0d98b8ffa13fe238fc0fcf8ff0ec76a3a284eb
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390457"
---
# <a name="ipersistmessagegetclassid"></a>IPersistMessage::GetClassID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt einen Bezeichner, der den Formular Server darstellt, der das Formular verwaltet werden können. 
  
```cpp
HRESULT GetClassID(
  LPCLSID lpClassID
);
```

## <a name="parameters"></a>Parameter

 _lpClassID_
  
> [in, out] Ein Zeiger auf die Klassen-ID (CLSID) des Formulars.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Klassen-ID wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>Hinweise

Die **IPersistMessge::GetClassID** -Methode wird die Inhalte des Parameters _LpClassID_ auf dem Formular Server Klassen-ID und gibt S_OK zurück. Wenn ein Formular Viewer **GetClassID** aufruft und erfolgreich zurückgegeben, wird das Formular in den Status [nicht initialisiert](uninitialized-state.md) platziert. 
  
Weitere Informationen darüber, wie Klassenbezeichner mit strukturierten Speicherobjekte verwendet werden finden Sie unter der Dokumentation für die [IPersist:: GetClassID](https://msdn.microsoft.com/library/921a3b86-a240-454e-9411-8d653e02b90e.aspx) -Methode. 
  
## <a name="see-also"></a>Siehe auch



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

