---
title: Verwalten von Nachrichten in OST ohne Aufrufen einer Synchronisierung im Exchange-Cache-Modus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3a1f0aa2-813f-222c-f871-0501de5d9dec
description: 'Enthält ein Codebeispiel in C++, das zeigt, wie Sie IID_IMessageRaw in IMsgStore:: openEntry zum Abrufen einer IMessage-Schnittstelle verwenden, die eine Nachricht in einer Offlineordnerdatei (OST) verwaltet, ohne einen Download der gesamten Nachricht zu erzwingen, wenn sich der Client im Exchange-Cache befindet. Modus.'
ms.openlocfilehash: e50637b496ff43daedad2df27d027d8a6d0dc743
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316394"
---
# <a name="manage-messages-in-ost-without-invoking-a-synchronization-in-cached-exchange-mode"></a>Verwalten von Nachrichten in OST ohne Aufrufen einer Synchronisierung im Exchange-Cache-Modus

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dieses Thema enthält ein Codebeispiel in C++, in dem gezeigt wird `IID_IMessageRaw` , wie Sie in **[IMsgStore:: OpenEntry](imsgstore-openentry.md)** eine **[IMessage](imessageimapiprop.md)** -Schnittstelle abrufen können, die eine Nachricht in einer Offlineordnerdatei (Ost) verwaltet, ohne einen Download der gesamten Nachricht zu erzwingen, wenn der Client befindet sich im Exchange-Cache-Modus. 
  
Wenn sich ein Client im Exchange-Cache-Modus befindet, können sich Nachrichten in der OST in einem von zwei Status befinden:
  
- Die gesamte Nachricht, die den Header enthält, und der Text wird heruntergeladen.
    
- Die Nachricht mit der Kopfzeile wird heruntergeladen.
    
Wenn Sie eine **IMessage** -Schnittstelle für eine Nachricht in einem Ost anfordern und sich der Client im Exchange-Cache `IID_IMessageRaw`-Modus befindet, verwenden Sie. Wenn Sie `IID_IMessage` eine **IMessage** -Schnittstelle anfordern und in der OST-Datei nur die Kopfzeile heruntergeladen wurde, rufen Sie eine Synchronisierung auf, die versucht, die gesamte Nachricht herunterzuladen. 
  
Wenn Sie eine `IID_IMessageRaw` IMessage `IID_IMessage` -Schnittstelle **** verwenden oder anfordern, werden die zurückgegebenen Schnittstellen identisch verwendet. Die **IMessage** -Schnittstelle, die von `IID_IMessageRaw` using angefordert wurde, gibt eine e-Mail-Nachricht zurück, wie Sie in der Ost vorhanden ist, und die Synchronisierung wird nicht erzwungen. 
  
Das folgende Beispiel zeigt, wie die openEntry-Methode aufgerufen wird `IID_IMessageRaw` , wobei `IID_IMessage`anstelle von übergeben wird. ****
  
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

Wenn die **OpenEntry** -Methode den **MAPI_E_INTERFACE_NOT_SUPPORTED** -Fehlercode zurückgibt, gibt er an, dass der Nachrichtenspeicher keinen Zugriff auf die Nachricht im RAW-Modus unterstützt. Testen Sie in dieser Situation erneut **** die OpenEntry-Methode, `IID_IMessage`indem Sie übergeben.

> [!IMPORTANT]
>  `IID_IMessageRaw`möglicherweise nicht in der herunterladbaren Headerdatei definiert, die Sie derzeit haben. In diesem Fall können Sie Sie dem Code hinzufügen, indem Sie die folgende Definition verwenden. Verwenden Sie das DEFINE_OLEGUID-Makro, das in der Microsoft Windows Software Development Kit (SDK)-Headerdatei guiddef. h definiert ist, um den symbolischen GUID-Namen mit seinem Wert zu verknüpfen. >  `#if !defined(INITGUID) || defined(USES_IID_IMessageRaw)`>  `DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0);`>  `#endif`
  
## <a name="see-also"></a>Siehe auch

- [Informationen zu MAPI-Ergänzungen](about-mapi-additions.md) 
- [Zugreifen auf einen Speicher auf dem Remoteserver, wenn Outlook sich im Exchange-Cache-Modus befindet](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [Öffnen eines Speichers auf dem Remoteserver, wenn Outlook sich im Exchange-Cache-Modus befindet](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)

