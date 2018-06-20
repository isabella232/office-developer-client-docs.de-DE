---
title: Verwalten von Nachrichten in OST-Dateien ohne Aufrufen eine Synchronisierung im Exchange-Cache-Modus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3a1f0aa2-813f-222c-f871-0501de5d9dec
description: Enthält ein Codebeispiel in C++, das zeigt, wie Sie IID_IMessageRaw in IMsgStore::OpenEntry verwenden, um eine IMessage-Schnittstelle zu erhalten, die eine Nachricht in einer offline-Ordner-Datei (OST) verwaltet, ohne einen Download der gesamten Nachricht erzwingen, wenn der Client im Exchange-Cache ist Modus.
ms.openlocfilehash: e32bf4f64bfb91979133ee983e45481b3d5b9732
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791871"
---
# <a name="manage-messages-in-ost-without-invoking-a-synchronization-in-cached-exchange-mode"></a>Verwalten von Nachrichten in OST-Dateien ohne Aufrufen eine Synchronisierung im Exchange-Cache-Modus

**Betrifft**: Outlook 
  
Dieses Thema enthält ein Codebeispiel, das zeigt, wie Sie mit c++ `IID_IMessageRaw` in **[IMsgStore::OpenEntry](imsgstore-openentry.md)** abrufen, eine **[IMessage](imessageimapiprop.md)** -Schnittstelle, die eine Nachricht in einer offline-Ordner-Datei (OST) verwaltet ohne zu erzwingen einen Download des gesamten Meldung an, wenn der Client befindet sich in der Exchange-Cache-Modus. 
  
Wenn ein Client in Exchange-Cache-Modus ist, können Nachrichten in der OST-Dateien in zwei Zuständen sein:
  
- Die gesamte Nachricht, die die Kopfzeile und der Nachrichtentext enthält wird heruntergeladen.
    
- Die Nachricht mit nur die Kopfzeile wird heruntergeladen.
    
Wenn Sie eine **IMessage** -Schnittstelle für eine Nachricht in einer OST anfordern und der Client im Exchange-Cache-Modus ist, verwenden Sie `IID_IMessageRaw`. Bei Verwendung `IID_IMessage` eine Schnittstelle **IMessage** anfordern und weist die Nachricht nur Header in die OST-Dateien heruntergeladen haben, rufen Sie eine Synchronisierung, das versucht, laden Sie die gesamte Nachricht. 
  
Bei Verwendung `IID_IMessageRaw` oder `IID_IMessage` um eine Schnittstelle **IMessage** anzufordern, die Schnittstellen, die zurückgegeben werden derzeit identisch sind. Die **IMessage** -Schnittstelle, die mithilfe von angefordert wurde `IID_IMessageRaw` eine e-Mail-Nachricht wird, wie sie in der OST-Dateien vorhanden ist und Synchronisierung wird nicht erzwungen. 
  
Im folgenden Beispiel wird gezeigt, wie die **OpenEntry** -Methode übergeben Aufrufen `IID_IMessageRaw` anstelle von `IID_IMessage`.
  
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

Wenn die **OpenEntry** -Methode den Fehlercode **MAPI_E_INTERFACE_NOT_SUPPORTED** zurückgibt, bedeutet dies, dass der Nachrichtenspeicher nicht unterstützt den Zugriff auf die Nachricht im unformatierten Modus. In diesem Fall wiederholen Sie die **OpenEntry** -Methode, indem Sie übergeben `IID_IMessage`.

> [!IMPORTANT]
>  `IID_IMessageRaw`möglicherweise nicht in der herunterladbaren Headerdatei definiert werden, die Sie besitzen. In diesem Fall können Sie es dem Code hinzufügen mithilfe der folgenden Definition. Verwenden Sie das DEFINE_OLEGUID-Makro in der Microsoft Windows Software Development Kit (SDK)-Header-Datei guiddef.h definiert, um seinen Wert den GUID symbolischen Namen zuzuordnen. >  `#if !defined(INITGUID) || defined(USES_IID_IMessageRaw)`>  `DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0);`>  `#endif`
  
## <a name="see-also"></a>Siehe auch

- [Informationen zu MAPI-Ergänzungen](about-mapi-additions.md) 
- [Access einen Speicher auf dem Remote Server bei Outlook befindet sich in der Exchange-Cache-Modus](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [Geöffnet ist ein Speichers Remote Server Wenn Outlook im Exchange-Cache-Modus](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)

