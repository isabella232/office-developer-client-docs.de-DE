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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395308"
---
# <a name="iproxystoreobject"></a>IProxyStoreObject

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt ein Internet Message Access Protocol (IMAP) Store-Objekt, das seit allein stehenden und, die ermöglicht den Zugriff auf Elemente in der Persönliche Ordner-Datei (PST) ohne Synchronisation aufrufen und die Elemente herunterladen.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Vererbte Berechtigungen aus:  <br/> |[IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) <br/> |
|Bereitgestellt von:  <br/> |Nachricht Speicheranbieter  <br/> |
|Schnittstellenbezeichner:  <br/> |**IID_IProxyStoreObject** <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
| *Platzhalter-member*  <br/> | *Nicht unterstützte oder dokumentiert.*  <br/> |
|[IProxyStoreObject::UnwrapNoRef](iproxystoreobject-unwrapnoref.md) <br/> |Ruft einen Zeiger auf ein allein stehenden IMAP-Speicher ab.  <br/> |
| *Platzhalter-member*  <br/> | *Nicht unterstützte oder dokumentiert.*  <br/> |
   
## <a name="remarks"></a>Hinweise

Rufen Sie [QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) in der Quelle Nachrichtenspeicher die **IProxyStoreObject** -Schnittstelle abzurufen. Rufen Sie dann **IProxyStoreObject::UnwrapNoRef** , um das allein stehenden Store-Objekt zu erhalten. Wenn **QueryInterface** den Fehler **MAPI_E_INTERFACE_NOT_SUPPORTED**zurückgibt, wurde der Store nicht umgebrochen. 
  
Da **UnwrapNoRef** nicht den Referenzzähler für diese neuen Zeiger auf das allein stehenden Store-Objekt, nach dem erfolgreichen Aufruf von **UnwrapNoRef**erhöht, sollten Sie [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) zum Verwalten von des Referenzzähler aufrufen. 
  

