---
title: IProxyStoreObject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProxyStoreObject
api_type:
- COM
ms.assetid: 567bede4-39a3-bfb4-af85-ba678e2cf4a5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 485d3f3cd4b6be4748a2ebf2ba0d0b71f691478f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315519"
---
# <a name="iproxystoreobject"></a>IProxyStoreObject

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt ein IMAP-Speicherobjekt (Internet Message Access Protocol) bereit, das nicht umbrochen wurde und das den Zugriff auf Elemente in der PST-Datei (Personal Folders) ermöglicht, ohne die Synchronisierung aufzurufen und die Elemente herunterzuladen.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Geerbt von:  <br/> |[IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) <br/> |
|Bereitgestellt von:  <br/> |Nachrichtenspeicher Anbieter  <br/> |
|Schnittstellenbezeichner:  <br/> |**IID_IProxyStoreObject** <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
| *Platzhalterelement*  <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
|[IProxyStoreObject::UnwrapNoRef](iproxystoreobject-unwrapnoref.md) <br/> |Ruft einen Zeiger auf einen unverpackten IMAP-Speicher ab.  <br/> |
| *Platzhalterelement*  <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
   
## <a name="remarks"></a>Hinweise

Rufen Sie [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) im Quell Nachrichtenspeicher auf, um die **IProxyStoreObject** -Schnittstelle zu erhalten. Rufen Sie dann **IProxyStoreObject:: UnwrapNoRef** auf, um das nicht verpackte Store-Objekt zu erhalten. Wenn **QueryInterface** den Fehler **MAPI_E_INTERFACE_NOT_SUPPORTED**zurückgibt, wurde der Speicher nicht umbrochen. 
  
Da **UnwrapNoRef** den Verweiszähler für diesen neuen Zeiger nicht auf das Objekt des aufgepackten Speichers erhöht, sollten Sie nach dem erfolgreichen Aufruf von **UnwrapNoRef** [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) aufrufen, um den Verweiszähler beizubehalten. 
  

