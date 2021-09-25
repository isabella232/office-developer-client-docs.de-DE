---
title: IPersistMessageGetClassID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPersistMessage.GetClassID
api_type:
- COM
ms.assetid: 77eeb468-3432-4ccd-9c1e-1df9ce605193
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5d8f4283d2cf9e5de7547264de429ef8b17d9667
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561439"
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
  
> [in, out] Ein Zeiger auf den Klassenbezeichner (CLSID) des Formulars.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Klassenbezeichner wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IPersistMessge::GetClassID-Methode** legt den Inhalt des  _lpClassID-Parameters_ auf den Klassenbezeichner des Formularservers fest und gibt S_OK zurück. Wenn ein Formularviewer **GetClassID** aufruft und erfolgreich zurückgegeben wird, wird das Formular in den Status ["Nicht initialisiert"](uninitialized-state.md) versetzt. 
  
Weitere Informationen zur Verwendung von Klassenbezeichnern mit strukturierten Speicherobjekten finden Sie in der Dokumentation für die [IPersist::GetClassID-Methode.](https://msdn.microsoft.com/library/921a3b86-a240-454e-9411-8d653e02b90e.aspx) 
  
## <a name="see-also"></a>Siehe auch



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

