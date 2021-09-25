---
title: Verwalten von Nachrichten in OST ohne Aufrufen einer Synchronisierung im Modus "Zwischengespeicherte Exchange"
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 3a1f0aa2-813f-222c-f871-0501de5d9dec
description: Enthält ein Codebeispiel in C++, das zeigt, wie IID_IMessageRaw in IMsgStore::OpenEntry verwendet werden kann, um eine IMessage-Schnittstelle abzurufen, die eine Nachricht in einer Offlineordnerdatei (OST) verwaltet, ohne einen Download der gesamten Nachricht zu erzwingen, wenn sich der Client im cached Exchange Modus befindet.
ms.openlocfilehash: e78743e6e84293d6507762380ac9b1952e420dd7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614073"
---
# <a name="manage-messages-in-ost-without-invoking-a-synchronization-in-cached-exchange-mode"></a>Verwalten von Nachrichten in OST ohne Aufrufen einer Synchronisierung im Modus "Zwischengespeicherte Exchange"

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dieses Thema enthält ein Codebeispiel in C++, das zeigt, wie `IID_IMessageRaw` Sie in **[IMsgStore::OpenEntry](imsgstore-openentry.md)** eine **[IMessage-Schnittstelle](imessageimapiprop.md)** abrufen, die eine Nachricht in einer Offlineordnerdatei (OST) verwaltet, ohne einen Download der gesamten Nachricht zu erzwingen, wenn sich der Client im Cache Exchange Modus befindet. 
  
Wenn sich ein Client im Modus "Cached Exchange" befindet, können Nachrichten im OST einen von zwei Zuständen aufweisen:
  
- Die gesamte Nachricht, die die Kopfzeile und den Textkörper enthält, wird heruntergeladen.
    
- Die Nachricht mit nur ihrer Kopfzeile wird heruntergeladen.
    
Wenn Sie eine **IMessage-Schnittstelle** für eine Nachricht in einem OST anfordern und sich der Client Exchange Modus zwischengespeichert befindet, verwenden Sie `IID_IMessageRaw` . Wenn Sie  `IID_IMessage` eine **IMessage-Schnittstelle** anfordern und die Nachricht nur den Header in ost heruntergeladen hat, rufen Sie eine Synchronisierung auf, die versucht, die gesamte Nachricht herunterzuladen. 
  
Wenn Sie  `IID_IMessageRaw`  `IID_IMessage` eine **IMessage-Schnittstelle** verwenden oder anfordern, werden die zurückgegebenen Schnittstellen verwendet. Die **IMessage-Schnittstelle,** die mithilfe angefordert wurde,  `IID_IMessageRaw` gibt eine E-Mail-Nachricht zurück, wie sie in ost vorhanden ist, und die Synchronisierung wird nicht erzwungen. 
  
Das folgende Beispiel zeigt, wie sie die **OpenEntry-Methode** aufrufen, anstatt sie zu  `IID_IMessageRaw`  `IID_IMessage` übergeben.
  
```cpp
HRESULT HrOpenRawMessage ( 
    LPMDB lpMSB,  
    ULONG cbEntryID,  
    LPENTRYID lpEntryID,  
    ULONG ulFlags,  
    LPMESSAGE* lpMessage) 
{ 
    ULONG ulObjType = NULL; 
 
    HRESULT hRes = lpMDB->OpenEntry( 
        cbEntryID, 
        lpEntryID, 
        IID_IMessageRaw, 
        ulFlags, 
        &ulObjType, 
        (LPUNKNOWN*) lpMessage)); 
 
   return hRes; 
} 

```

Wenn die **OpenEntry-Methode** den **MAPI_E_INTERFACE_NOT_SUPPORTED** Fehlercode zurückgibt, gibt sie an, dass der Nachrichtenspeicher den Zugriff auf die Nachricht im Rohmodus nicht unterstützt. Versuchen Sie es in diesem Fall erneut mit der **OpenEntry-Methode,** indem Sie  `IID_IMessage` .

> [!IMPORTANT]
>  `IID_IMessageRaw` möglicherweise nicht in der herunterladbaren Headerdatei definiert, über die Sie derzeit verfügen. In diesem Fall können Sie es ihrem Code mithilfe der folgenden Definition hinzufügen. Verwenden Sie das in der Microsoft Windows Software Development Kit (SDK)-Headerdatei guiddef.h definierte DEFINE_OLEGUID Makro, um den symbolischen GUID-Namen dem Wert zuzuordnen. >  `#if !defined(INITGUID) || defined(USES_IID_IMessageRaw)`>  `DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0);`>  `#endif`
  
## <a name="see-also"></a>Siehe auch

- [Informationen zu MAPI-Ergänzungen](about-mapi-additions.md) 
- [Zugreifen auf einen Speicher auf dem Remoteserver, wenn Outlook sich im Exchange-Cache-Modus befindet](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [Öffnen eines Speichers auf dem Remoteserver, wenn Outlook sich im Exchange-Cache-Modus befindet](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)

