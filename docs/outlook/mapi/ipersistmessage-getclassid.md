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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309625"
---
# <a name="ipersistmessagegetclassid"></a>IPersistMessage::GetClassID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt einen Bezeichner zurück, der den Formularserver darstellt, der das Formular verwalten kann. 
  
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
  
> Der Klassenbezeichner wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>Hinweise

Die **IPersistMessge::GetClassID-Methode** legt den Inhalt des  _lpClassID-Parameters_ auf den Klassenbezeichner des Formularservers fest und gibt S_OK. Wenn ein Formularbetrachter **GetClassID aufruft** und erfolgreich zurückgibt, wird das Formular in den [Status Nicht initialisiert](uninitialized-state.md) platziert. 
  
Weitere Informationen zur Verwendung von Klassenbezeichnern mit strukturierten Speicherobjekten finden Sie in der Dokumentation zur [IPersist::GetClassID-Methode.](https://msdn.microsoft.com/library/921a3b86-a240-454e-9411-8d653e02b90e.aspx) 
  
## <a name="see-also"></a>Siehe auch



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

