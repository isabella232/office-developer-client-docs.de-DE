---
title: IProxyStoreObjectUnwrapNoRef
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProxyStoreObject.UnwrapNoRef
api_type:
- COM
ms.assetid: 1122b6e0-e7e1-e68a-e090-435777343d04
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ef9f506c1a95fec86c7f092b0299198e6149d3ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320153"
---
# <a name="iproxystoreobjectunwrapnoref"></a>IProxyStoreObject::UnwrapNoRef

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft einen Zeiger auf ein imAP (Unwraped Internet Message Access Protocol) gespeichertes Objekt ab, das Zugriff auf die zugrunde liegende Pst (Personal Folders File) ermöglicht, ohne die Synchronisierung aufrufen und die Elemente herunterladen zu müssen.
  
```cpp
HRESULT IProxyStoreObject::UnwrapNoRef (     LPVOID *ppvObject ); 
```

## <a name="parameters"></a>Parameter

 _ppvObject_
  
> [out] Zeiger auf ein [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) Store-Objekt, das entpackt ist. 
    
## <a name="return-values"></a>Rückgabewerte

S_OK
  
- Der Aufruf war erfolgreich, und ein Zeiger auf eine entpackte Schnittstelle wurde in _ppvObject zurückgegeben._
    
## <a name="remarks"></a>Hinweise

Ohne zunächst ein ImAP-Speicher zu entwrapping, kann der Zugriff auf eine Nachricht im Store eine Synchronisierung erzwingen, die versucht, die gesamte Nachricht herunterzuladen. Die Verwendung des entpackten Speichers ermöglicht den Zugriff auf die Nachricht im aktuellen Status, ohne einen Download auszulösen.
  
Da **UnwrapNoRef** die Referenzanzahl für diesen neuen Zeiger nicht auf das nicht mehr ausgepackte Speicherobjekt erhöht, sollten Sie nach dem erfolgreichen Aufruf von **UnwrapNoRef** [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) aufrufen, um die Referenzanzahl zu verwalten. 
  
## <a name="see-also"></a>Siehe auch



[IProxyStoreObject](iproxystoreobject.md)

