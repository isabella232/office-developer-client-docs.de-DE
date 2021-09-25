---
title: IProxyStoreObject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProxyStoreObject
api_type:
- COM
ms.assetid: 567bede4-39a3-bfb4-af85-ba678e2cf4a5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3dad9c850c4564fd1af206df23dc3cd621ea60ac
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596029"
---
# <a name="iproxystoreobject"></a>IProxyStoreObject

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt ein IMAP-Speicherobjekt (Internet Message Access Protocol) bereit, das entpackt wurde und den Zugriff auf Elemente in der Persönliche Ordner-Datei (PST) ermöglicht, ohne die Synchronisierung aufzugreifen und die Elemente herunterzuladen.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Geerbt von:  <br/> |[IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) <br/> |
|Bereitgestellt von:  <br/> |Nachrichtenspeicheranbieter  <br/> |
|Schnittstellenbezeichner:  <br/> |**IID_IProxyStoreObject** <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
| *Platzhalterelement*  <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
|[IProxyStoreObject::UnwrapNoRef](iproxystoreobject-unwrapnoref.md) <br/> |Ruft einen Zeiger auf einen nicht gepackten IMAP-Speicher ab.  <br/> |
| *Platzhalterelement*  <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Rufen Sie [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) im Quellnachrichtenspeicher auf, um die **IProxyStoreObject-Schnittstelle** abzurufen. Rufen Sie dann **IProxyStoreObject::UnwrapNoRef** auf, um das nicht gepackte Store-Objekt abzurufen. Wenn **QueryInterface** den Fehler **MAPI_E_INTERFACE_NOT_SUPPORTED** zurückgibt, wurde der Speicher nicht umbrochen. 
  
Da **UnwrapNoRef** die Referenzanzahl für diesen neuen Zeiger nicht auf das unwrappede Speicherobjekt erhöht, sollten Sie nach dem erfolgreichen Aufrufen von **"UnwrapNoRef"** [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) aufrufen, um die Referenzanzahl beizubehalten. 
  

