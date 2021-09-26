---
title: IProxyStoreObjectUnwrapNoRef
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProxyStoreObject.UnwrapNoRef
api_type:
- COM
ms.assetid: 1122b6e0-e7e1-e68a-e090-435777343d04
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: db3f247fda5be8f93210215fb83d51114a2165d4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620541"
---
# <a name="iproxystoreobjectunwrapnoref"></a>IProxyStoreObject::UnwrapNoRef

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft einen Zeiger auf ein nicht gepacktes IMAP-Speicherobjekt (Internet Message Access Protocol) ab, das Zugriff auf die zugrunde liegende Persönliche Ordner-Datei (PST) bietet, ohne die Synchronisierung aufzugreifen und die Elemente herunterzuladen.
  
```cpp
HRESULT IProxyStoreObject::UnwrapNoRef (     LPVOID *ppvObject ); 
```

## <a name="parameters"></a>Parameter

 _ppvObject_
  
> [out] Zeiger auf ein [IMsgStore: IMAPIProp-Speicherobjekt,](imsgstoreimapiprop.md) das entpackt wird. 
    
## <a name="return-values"></a>Rückgabewerte

S_OK
  
- Der Aufruf war erfolgreich, und ein Zeiger auf eine nicht gepackte Schnittstelle wurde in  _ppvObject_ zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

Ohne zunächst ein IMAP-Speicher zu entpacken, kann der Zugriff auf eine Nachricht im Speicher eine Synchronisierung erzwingen, die versucht, die gesamte Nachricht herunterzuladen. Die Verwendung des nicht gepackten Speichers ermöglicht den Zugriff auf die Nachricht im aktuellen Zustand, ohne einen Download auszulösen.
  
Da **UnwrapNoRef** die Referenzanzahl für diesen neuen Zeiger nicht auf das unwrappede Speicherobjekt erhöht, sollten Sie nach dem erfolgreichen Aufrufen von **"UnwrapNoRef"** [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) aufrufen, um die Referenzanzahl beizubehalten. 
  
## <a name="see-also"></a>Siehe auch



[IProxyStoreObject](iproxystoreobject.md)

