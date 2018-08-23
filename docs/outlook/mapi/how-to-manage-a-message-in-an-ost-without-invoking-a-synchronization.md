---
title: Verwalten von Nachrichten in OST-Dateien ohne Aufrufen eine Synchronisierung im Exchange-Cache-Modus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3a1f0aa2-813f-222c-f871-0501de5d9dec
description: Enthält ein Codebeispiel in C++, das zeigt, wie Sie IID_IMessageRaw in IMsgStore::OpenEntry verwenden, um eine IMessage-Schnittstelle zu erhalten, die eine Nachricht in einer offline-Ordner-Datei (OST) verwaltet, ohne einen Download der gesamten Nachricht erzwingen, wenn der Client im Exchange-Cache ist Modus.
ms.openlocfilehash: f094f5a7deae705ed64b912483726aeb409fb107
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568105"
---
# <a name="manage-messages-in-ost-without-invoking-a-synchronization-in-cached-exchange-mode"></a><span data-ttu-id="5781d-103">Verwalten von Nachrichten in OST-Dateien ohne Aufrufen eine Synchronisierung im Exchange-Cache-Modus</span><span class="sxs-lookup"><span data-stu-id="5781d-103">Manage messages in OST without invoking a synchronization in Cached Exchange mode</span></span>

<span data-ttu-id="5781d-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5781d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5781d-105">Dieses Thema enthält ein Codebeispiel, das zeigt, wie Sie mit c++ `IID_IMessageRaw` in **[IMsgStore::OpenEntry](imsgstore-openentry.md)** abrufen, eine **[IMessage](imessageimapiprop.md)** -Schnittstelle, die eine Nachricht in einer offline-Ordner-Datei (OST) verwaltet ohne zu erzwingen einen Download des gesamten Meldung an, wenn der Client befindet sich in der Exchange-Cache-Modus.</span><span class="sxs-lookup"><span data-stu-id="5781d-105">This topic contains a code sample in C++ that shows how to use `IID_IMessageRaw` in **[IMsgStore::OpenEntry](imsgstore-openentry.md)** to obtain an **[IMessage](imessageimapiprop.md)** interface that manages a message in an offline folders file (OST) without forcing a download of the whole message when the client is in Cached Exchange Mode.</span></span> 
  
<span data-ttu-id="5781d-106">Wenn ein Client in Exchange-Cache-Modus ist, können Nachrichten in der OST-Dateien in zwei Zuständen sein:</span><span class="sxs-lookup"><span data-stu-id="5781d-106">When a client is in Cached Exchange Mode, messages in the OST can be in one of two states:</span></span>
  
- <span data-ttu-id="5781d-107">Die gesamte Nachricht, die die Kopfzeile und der Nachrichtentext enthält wird heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="5781d-107">The whole message that contains the header and the body is downloaded.</span></span>
    
- <span data-ttu-id="5781d-108">Die Nachricht mit nur die Kopfzeile wird heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="5781d-108">The message with only its header is downloaded.</span></span>
    
<span data-ttu-id="5781d-109">Wenn Sie eine **IMessage** -Schnittstelle für eine Nachricht in einer OST anfordern und der Client im Exchange-Cache-Modus ist, verwenden Sie `IID_IMessageRaw`.</span><span class="sxs-lookup"><span data-stu-id="5781d-109">When you request an **IMessage** interface for a message in an OST and the client is in Cached Exchange Mode, use  `IID_IMessageRaw`.</span></span> <span data-ttu-id="5781d-110">Bei Verwendung `IID_IMessage` eine Schnittstelle **IMessage** anfordern und weist die Nachricht nur Header in die OST-Dateien heruntergeladen haben, rufen Sie eine Synchronisierung, das versucht, laden Sie die gesamte Nachricht.</span><span class="sxs-lookup"><span data-stu-id="5781d-110">If you use  `IID_IMessage` to request an **IMessage** interface, and if the message has only its header downloaded in the OST, you invoke a synchronization that attempts to download the whole message.</span></span> 
  
<span data-ttu-id="5781d-111">Bei Verwendung `IID_IMessageRaw` oder `IID_IMessage` um eine Schnittstelle **IMessage** anzufordern, die Schnittstellen, die zurückgegeben werden derzeit identisch sind.</span><span class="sxs-lookup"><span data-stu-id="5781d-111">If you use  `IID_IMessageRaw` or  `IID_IMessage` to request an **IMessage** interface, the interfaces that are returned are identical in use.</span></span> <span data-ttu-id="5781d-112">Die **IMessage** -Schnittstelle, die mithilfe von angefordert wurde `IID_IMessageRaw` eine e-Mail-Nachricht wird, wie sie in der OST-Dateien vorhanden ist und Synchronisierung wird nicht erzwungen.</span><span class="sxs-lookup"><span data-stu-id="5781d-112">The **IMessage** interface that was requested by using  `IID_IMessageRaw` returns an email message as it exists in the OST, and synchronization is not forced.</span></span> 
  
<span data-ttu-id="5781d-113">Im folgenden Beispiel wird gezeigt, wie die **OpenEntry** -Methode übergeben Aufrufen `IID_IMessageRaw` anstelle von `IID_IMessage`.</span><span class="sxs-lookup"><span data-stu-id="5781d-113">The following example shows how to call the **OpenEntry** method, passing  `IID_IMessageRaw` instead of  `IID_IMessage`.</span></span>
  
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

<span data-ttu-id="5781d-114">Wenn die **OpenEntry** -Methode den Fehlercode **MAPI_E_INTERFACE_NOT_SUPPORTED** zurückgibt, bedeutet dies, dass der Nachrichtenspeicher nicht unterstützt den Zugriff auf die Nachricht im unformatierten Modus.</span><span class="sxs-lookup"><span data-stu-id="5781d-114">If the **OpenEntry** method returns the **MAPI_E_INTERFACE_NOT_SUPPORTED** error code, it indicates that the message store does not support accessing the message in raw mode.</span></span> <span data-ttu-id="5781d-115">In diesem Fall wiederholen Sie die **OpenEntry** -Methode, indem Sie übergeben `IID_IMessage`.</span><span class="sxs-lookup"><span data-stu-id="5781d-115">In this situation, try the **OpenEntry** method again by passing  `IID_IMessage`.</span></span>

> [!IMPORTANT]
>  <span data-ttu-id="5781d-116">`IID_IMessageRaw`möglicherweise nicht in der herunterladbaren Headerdatei definiert werden, die Sie besitzen.</span><span class="sxs-lookup"><span data-stu-id="5781d-116">`IID_IMessageRaw` might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="5781d-117">In diesem Fall können Sie es dem Code hinzufügen mithilfe der folgenden Definition.</span><span class="sxs-lookup"><span data-stu-id="5781d-117">In this case, you can add it to your code by using the following definition.</span></span> <span data-ttu-id="5781d-118">Verwenden Sie das DEFINE_OLEGUID-Makro in der Microsoft Windows Software Development Kit (SDK)-Header-Datei guiddef.h definiert, um seinen Wert den GUID symbolischen Namen zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="5781d-118">Use the DEFINE_OLEGUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate the GUID symbolic name with its value.</span></span> >  `#if !defined(INITGUID) || defined(USES_IID_IMessageRaw)`>  `DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0);`>  `#endif`
  
## <a name="see-also"></a><span data-ttu-id="5781d-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5781d-119">See also</span></span>

- [<span data-ttu-id="5781d-120">Informationen zu MAPI-Ergänzungen</span><span class="sxs-lookup"><span data-stu-id="5781d-120">About MAPI Additions</span></span>](about-mapi-additions.md) 
- [<span data-ttu-id="5781d-121">Zugreifen auf einen Store auf dem Remote-Server, wenn Outlook sich Exchange-Cache-Modus befindet</span><span class="sxs-lookup"><span data-stu-id="5781d-121">Access a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="5781d-122">Öffnen eines Speichers auf dem Remote-Server, wenn Outlook sich im Exchange-Cache-Modus befindet</span><span class="sxs-lookup"><span data-stu-id="5781d-122">Open a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)

