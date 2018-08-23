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
ms.openlocfilehash: 8539f81ed1741063d878da492d925b63c488d1a9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586431"
---
# <a name="iproxystoreobjectunwrapnoref"></a>IProxyStoreObject::UnwrapNoRef

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Ruft einen Zeiger auf ein allein stehenden Internet Message Access Protocol (IMAP) Store-Objekt, das Zugriff auf die zugrunde liegende Persönliche Ordner-Datei (PST) bietet ohne Synchronisation aufrufen und die Elemente herunterladen.
  
```cpp
HRESULT IProxyStoreObject::UnwrapNoRef (     LPVOID *ppvObject ); 
```

## <a name="parameters"></a>Parameter

 _ppvObject_
  
> [out] Zeiger auf eine [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) allein stehenden ist Store-Objekt. 
    
## <a name="return-values"></a>Rückgabewerte

S_OK
  
- Der Aufruf war erfolgreich, und ein Zeiger auf eine allein stehenden-Schnittstelle in _PpvObject_zurückgegeben wurden.
    
## <a name="remarks"></a>HinwBemerkungeneise

Ohne den ersten Entpacken einen IMAP-Speicher, kann den Zugriff auf eine Nachricht im Speicher eine Synchronisierung erzwingen, die versucht, laden Sie die gesamte Nachricht. Ermöglicht den Zugriff auf die Nachricht im aktuellen Zustand ohne Auslösen der Download mit den allein stehenden Speicher.
  
Da **UnwrapNoRef** nicht den Referenzzähler für diese neuen Zeiger auf das allein stehenden Store-Objekt, nach dem erfolgreichen Aufruf von **UnwrapNoRef**erhöht, sollten Sie [IUnknown:: AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) zum Verwalten von des Referenzzähler aufrufen. 
  
## <a name="see-also"></a>Siehe auch



[IProxyStoreObject](iproxystoreobject.md)

