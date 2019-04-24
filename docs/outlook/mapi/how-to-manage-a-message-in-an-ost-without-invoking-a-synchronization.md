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
# <a name="manage-messages-in-ost-without-invoking-a-synchronization-in-cached-exchange-mode"></a><span data-ttu-id="00620-103">Verwalten von Nachrichten in OST ohne Aufrufen einer Synchronisierung im Exchange-Cache-Modus</span><span class="sxs-lookup"><span data-stu-id="00620-103">Manage messages in OST without invoking a synchronization in Cached Exchange mode</span></span>

<span data-ttu-id="00620-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00620-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00620-105">Dieses Thema enthält ein Codebeispiel in C++, in dem gezeigt wird `IID_IMessageRaw` , wie Sie in **[IMsgStore:: OpenEntry](imsgstore-openentry.md)** eine **[IMessage](imessageimapiprop.md)** -Schnittstelle abrufen können, die eine Nachricht in einer Offlineordnerdatei (Ost) verwaltet, ohne einen Download der gesamten Nachricht zu erzwingen, wenn der Client befindet sich im Exchange-Cache-Modus.</span><span class="sxs-lookup"><span data-stu-id="00620-105">This topic contains a code sample in C++ that shows how to use `IID_IMessageRaw` in **[IMsgStore::OpenEntry](imsgstore-openentry.md)** to obtain an **[IMessage](imessageimapiprop.md)** interface that manages a message in an offline folders file (OST) without forcing a download of the whole message when the client is in Cached Exchange Mode.</span></span> 
  
<span data-ttu-id="00620-106">Wenn sich ein Client im Exchange-Cache-Modus befindet, können sich Nachrichten in der OST in einem von zwei Status befinden:</span><span class="sxs-lookup"><span data-stu-id="00620-106">When a client is in Cached Exchange Mode, messages in the OST can be in one of two states:</span></span>
  
- <span data-ttu-id="00620-107">Die gesamte Nachricht, die den Header enthält, und der Text wird heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="00620-107">The whole message that contains the header and the body is downloaded.</span></span>
    
- <span data-ttu-id="00620-108">Die Nachricht mit der Kopfzeile wird heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="00620-108">The message with only its header is downloaded.</span></span>
    
<span data-ttu-id="00620-109">Wenn Sie eine **IMessage** -Schnittstelle für eine Nachricht in einem Ost anfordern und sich der Client im Exchange-Cache `IID_IMessageRaw`-Modus befindet, verwenden Sie.</span><span class="sxs-lookup"><span data-stu-id="00620-109">When you request an **IMessage** interface for a message in an OST and the client is in Cached Exchange Mode, use  `IID_IMessageRaw`.</span></span> <span data-ttu-id="00620-110">Wenn Sie `IID_IMessage` eine **IMessage** -Schnittstelle anfordern und in der OST-Datei nur die Kopfzeile heruntergeladen wurde, rufen Sie eine Synchronisierung auf, die versucht, die gesamte Nachricht herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="00620-110">If you use  `IID_IMessage` to request an **IMessage** interface, and if the message has only its header downloaded in the OST, you invoke a synchronization that attempts to download the whole message.</span></span> 
  
<span data-ttu-id="00620-111">Wenn Sie eine `IID_IMessageRaw` IMessage `IID_IMessage` -Schnittstelle \*\*\*\* verwenden oder anfordern, werden die zurückgegebenen Schnittstellen identisch verwendet.</span><span class="sxs-lookup"><span data-stu-id="00620-111">If you use  `IID_IMessageRaw` or  `IID_IMessage` to request an **IMessage** interface, the interfaces that are returned are identical in use.</span></span> <span data-ttu-id="00620-112">Die **IMessage** -Schnittstelle, die von `IID_IMessageRaw` using angefordert wurde, gibt eine e-Mail-Nachricht zurück, wie Sie in der Ost vorhanden ist, und die Synchronisierung wird nicht erzwungen.</span><span class="sxs-lookup"><span data-stu-id="00620-112">The **IMessage** interface that was requested by using  `IID_IMessageRaw` returns an email message as it exists in the OST, and synchronization is not forced.</span></span> 
  
<span data-ttu-id="00620-113">Das folgende Beispiel zeigt, wie die openEntry-Methode aufgerufen wird `IID_IMessageRaw` , wobei `IID_IMessage`anstelle von übergeben wird. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="00620-113">The following example shows how to call the **OpenEntry** method, passing  `IID_IMessageRaw` instead of  `IID_IMessage`.</span></span>
  
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

<span data-ttu-id="00620-114">Wenn die **OpenEntry** -Methode den **MAPI_E_INTERFACE_NOT_SUPPORTED** -Fehlercode zurückgibt, gibt er an, dass der Nachrichtenspeicher keinen Zugriff auf die Nachricht im RAW-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="00620-114">If the **OpenEntry** method returns the **MAPI_E_INTERFACE_NOT_SUPPORTED** error code, it indicates that the message store does not support accessing the message in raw mode.</span></span> <span data-ttu-id="00620-115">Testen Sie in dieser Situation erneut \*\*\*\* die OpenEntry-Methode, `IID_IMessage`indem Sie übergeben.</span><span class="sxs-lookup"><span data-stu-id="00620-115">In this situation, try the **OpenEntry** method again by passing  `IID_IMessage`.</span></span>

> [!IMPORTANT]
>  <span data-ttu-id="00620-116">`IID_IMessageRaw`möglicherweise nicht in der herunterladbaren Headerdatei definiert, die Sie derzeit haben.</span><span class="sxs-lookup"><span data-stu-id="00620-116">`IID_IMessageRaw` might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="00620-117">In diesem Fall können Sie Sie dem Code hinzufügen, indem Sie die folgende Definition verwenden.</span><span class="sxs-lookup"><span data-stu-id="00620-117">In this case, you can add it to your code by using the following definition.</span></span> <span data-ttu-id="00620-118">Verwenden Sie das DEFINE_OLEGUID-Makro, das in der Microsoft Windows Software Development Kit (SDK)-Headerdatei guiddef. h definiert ist, um den symbolischen GUID-Namen mit seinem Wert zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="00620-118">Use the DEFINE_OLEGUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate the GUID symbolic name with its value.</span></span> >  `#if !defined(INITGUID) || defined(USES_IID_IMessageRaw)`>  `DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0);`>  `#endif`
  
## <a name="see-also"></a><span data-ttu-id="00620-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00620-119">See also</span></span>

- [<span data-ttu-id="00620-120">Informationen zu MAPI-Ergänzungen</span><span class="sxs-lookup"><span data-stu-id="00620-120">About MAPI Additions</span></span>](about-mapi-additions.md) 
- [<span data-ttu-id="00620-121">Zugreifen auf einen Speicher auf dem Remoteserver, wenn Outlook sich im Exchange-Cache-Modus befindet</span><span class="sxs-lookup"><span data-stu-id="00620-121">Access a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="00620-122">Öffnen eines Speichers auf dem Remoteserver, wenn Outlook sich im Exchange-Cache-Modus befindet</span><span class="sxs-lookup"><span data-stu-id="00620-122">Open a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)

