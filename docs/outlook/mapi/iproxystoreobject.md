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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f6566f567c228b6416a64dbd58653561bb592e6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792794"
---
# <a name="iproxystoreobject"></a>IProxyStoreObject

  
  
**Betrifft**: Outlook 
  
Stellt ein Internet Message Access Protocol (IMAP) Store-Objekt, das seit allein stehenden und, die ermöglicht den Zugriff auf Elemente in der Persönliche Ordner-Datei (PST) ohne Synchronisation aufrufen und die Elemente herunterladen.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Vererbte Berechtigungen aus:  <br/> |[IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) <br/> |
|Bereitgestellt von:  <br/> |Nachricht Speicheranbieter  <br/> |
|Schnittstellenbezeichner:  <br/> |**IID_IProxyStoreObject** <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
| *Platzhalter-member*  <br/> | *Nicht unterstützte oder dokumentiert.*  <br/> |
|[IProxyStoreObject::UnwrapNoRef](iproxystoreobject-unwrapnoref.md) <br/> |Ruft einen Zeiger auf ein allein stehenden IMAP-Speicher ab.  <br/> |
| *Platzhalter-member*  <br/> | *Nicht unterstützte oder dokumentiert.*  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Rufen Sie [QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) in der Quelle Nachrichtenspeicher die **IProxyStoreObject** -Schnittstelle abzurufen. Rufen Sie dann **IProxyStoreObject::UnwrapNoRef** , um das allein stehenden Store-Objekt zu erhalten. Wenn **QueryInterface** den Fehler **MAPI_E_INTERFACE_NOT_SUPPORTED**zurückgibt, wurde der Store nicht umgebrochen. 
  
Da **UnwrapNoRef** nicht den Referenzzähler für diese neuen Zeiger auf das allein stehenden Store-Objekt, nach dem erfolgreichen Aufruf von **UnwrapNoRef**erhöht, sollten Sie [IUnknown:: AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) zum Verwalten von des Referenzzähler aufrufen. 
  

