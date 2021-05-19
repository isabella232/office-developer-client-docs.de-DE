---
title: Verwalten von Nachrichten in OST ohne Aufrufen einer Synchronisierung im Exchange-Cache-Modus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3a1f0aa2-813f-222c-f871-0501de5d9dec
description: Enthält ein Codebeispiel in C++, das zeigt, wie Sie IID_IMessageRaw in IMsgStore::OpenEntry verwenden, um eine IMessage-Schnittstelle zu erhalten, die eine Nachricht in einer Offlineordnerdatei (OST) verwaltet, ohne einen Download der gesamten Nachricht zu erzwingen, wenn sich der Client im Exchange-Cache-Modus befindet.
ms.openlocfilehash: e50637b496ff43daedad2df27d027d8a6d0dc743
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418757"
---
# <a name="manage-messages-in-ost-without-invoking-a-synchronization-in-cached-exchange-mode"></a>Verwalten von Nachrichten in OST ohne Aufrufen einer Synchronisierung im Exchange-Cache-Modus

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dieses Thema enthält ein Codebeispiel in C++, das zeigt, wie Sie `IID_IMessageRaw` in **[IMsgStore::OpenEntry](imsgstore-openentry.md)** eine **[IMessage-Schnittstelle](imessageimapiprop.md)** abrufen, die eine Nachricht in einer Offlineordnerdatei (OST) verwaltet, ohne einen Download der gesamten Nachricht zu erzwingen, wenn sich der Client im Exchange-Cache-Modus befindet. 
  
Wenn sich ein Client im Exchange-Cache-Modus befindet, können sich Nachrichten im OST in einem der beiden Zustände befinden:
  
- Die gesamte Nachricht, die die Kopfzeile und den Textkörper enthält, wird heruntergeladen.
    
- Die Nachricht mit nur ihrem Header wird heruntergeladen.
    
Wenn Sie eine **IMessage-Schnittstelle** für eine Nachricht in einem OST anfordern und sich der Client im Exchange-Cache-Modus befindet, verwenden Sie  `IID_IMessageRaw` . Wenn Sie eine  `IID_IMessage` **IMessage-Schnittstelle** anfordern und nur die Kopfzeile der Nachricht in ost heruntergeladen wurde, rufen Sie eine Synchronisierung auf, die versucht, die gesamte Nachricht herunterzuladen. 
  
Wenn Sie eine  `IID_IMessageRaw`  `IID_IMessage` **IMessage-Schnittstelle** verwenden oder anfordern, werden die zurückgegebenen Schnittstellen identisch verwendet. Die **IMessage-Schnittstelle,** die mithilfe angefordert wurde, gibt eine E-Mail-Nachricht zurück, wie sie im OST vorhanden ist, und die Synchronisierung  `IID_IMessageRaw` wird nicht erzwungen. 
  
Das folgende Beispiel zeigt, wie Sie die **OpenEntry-Methode** aufrufen und anstatt  `IID_IMessageRaw`  `IID_IMessage` übergeben.
  
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

Wenn die **OpenEntry-Methode** den MAPI_E_INTERFACE_NOT_SUPPORTED zurückgibt, gibt sie an, dass der Nachrichtenspeicher den Zugriff auf die Nachricht im Unformatierungsmodus nicht unterstützt.  Versuchen Sie in diesem Fall die **OpenEntry-Methode** erneut, indem Sie  `IID_IMessage` übergeben.

> [!IMPORTANT]
>  `IID_IMessageRaw` möglicherweise nicht in der herunterladbaren Headerdatei definiert, über die Sie derzeit verfügen. In diesem Fall können Sie sie ihrem Code mithilfe der folgenden Definition hinzufügen. Verwenden Sie das DEFINE_OLEGUID, das in der Microsoft Windows Software Development Kit (SDK)-Headerdatei guiddef.h definiert ist, um den symbolischen NAMEN der GUID dem Wert zuzuordnen. >  `#if !defined(INITGUID) || defined(USES_IID_IMessageRaw)`>  `DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0);`>  `#endif`
  
## <a name="see-also"></a>Siehe auch

- [Informationen zu MAPI-Ergänzungen](about-mapi-additions.md) 
- [Zugreifen auf einen Speicher auf dem Remoteserver, wenn Outlook sich im Exchange-Cache-Modus befindet](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [Öffnen eines Speichers auf dem Remoteserver, wenn Outlook sich im Exchange-Cache-Modus befindet](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)

