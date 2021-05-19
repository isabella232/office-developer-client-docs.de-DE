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
# <a name="manage-messages-in-ost-without-invoking-a-synchronization-in-cached-exchange-mode"></a><span data-ttu-id="a122d-103">Verwalten von Nachrichten in OST ohne Aufrufen einer Synchronisierung im Exchange-Cache-Modus</span><span class="sxs-lookup"><span data-stu-id="a122d-103">Manage messages in OST without invoking a synchronization in Cached Exchange mode</span></span>

<span data-ttu-id="a122d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a122d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a122d-105">Dieses Thema enthält ein Codebeispiel in C++, das zeigt, wie Sie `IID_IMessageRaw` in **[IMsgStore::OpenEntry](imsgstore-openentry.md)** eine **[IMessage-Schnittstelle](imessageimapiprop.md)** abrufen, die eine Nachricht in einer Offlineordnerdatei (OST) verwaltet, ohne einen Download der gesamten Nachricht zu erzwingen, wenn sich der Client im Exchange-Cache-Modus befindet.</span><span class="sxs-lookup"><span data-stu-id="a122d-105">This topic contains a code sample in C++ that shows how to use `IID_IMessageRaw` in **[IMsgStore::OpenEntry](imsgstore-openentry.md)** to obtain an **[IMessage](imessageimapiprop.md)** interface that manages a message in an offline folders file (OST) without forcing a download of the whole message when the client is in Cached Exchange Mode.</span></span> 
  
<span data-ttu-id="a122d-106">Wenn sich ein Client im Exchange-Cache-Modus befindet, können sich Nachrichten im OST in einem der beiden Zustände befinden:</span><span class="sxs-lookup"><span data-stu-id="a122d-106">When a client is in Cached Exchange Mode, messages in the OST can be in one of two states:</span></span>
  
- <span data-ttu-id="a122d-107">Die gesamte Nachricht, die die Kopfzeile und den Textkörper enthält, wird heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="a122d-107">The whole message that contains the header and the body is downloaded.</span></span>
    
- <span data-ttu-id="a122d-108">Die Nachricht mit nur ihrem Header wird heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="a122d-108">The message with only its header is downloaded.</span></span>
    
<span data-ttu-id="a122d-109">Wenn Sie eine **IMessage-Schnittstelle** für eine Nachricht in einem OST anfordern und sich der Client im Exchange-Cache-Modus befindet, verwenden Sie  `IID_IMessageRaw` .</span><span class="sxs-lookup"><span data-stu-id="a122d-109">When you request an **IMessage** interface for a message in an OST and the client is in Cached Exchange Mode, use  `IID_IMessageRaw`.</span></span> <span data-ttu-id="a122d-110">Wenn Sie eine  `IID_IMessage` **IMessage-Schnittstelle** anfordern und nur die Kopfzeile der Nachricht in ost heruntergeladen wurde, rufen Sie eine Synchronisierung auf, die versucht, die gesamte Nachricht herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="a122d-110">If you use  `IID_IMessage` to request an **IMessage** interface, and if the message has only its header downloaded in the OST, you invoke a synchronization that attempts to download the whole message.</span></span> 
  
<span data-ttu-id="a122d-111">Wenn Sie eine  `IID_IMessageRaw`  `IID_IMessage` **IMessage-Schnittstelle** verwenden oder anfordern, werden die zurückgegebenen Schnittstellen identisch verwendet.</span><span class="sxs-lookup"><span data-stu-id="a122d-111">If you use  `IID_IMessageRaw` or  `IID_IMessage` to request an **IMessage** interface, the interfaces that are returned are identical in use.</span></span> <span data-ttu-id="a122d-112">Die **IMessage-Schnittstelle,** die mithilfe angefordert wurde, gibt eine E-Mail-Nachricht zurück, wie sie im OST vorhanden ist, und die Synchronisierung  `IID_IMessageRaw` wird nicht erzwungen.</span><span class="sxs-lookup"><span data-stu-id="a122d-112">The **IMessage** interface that was requested by using  `IID_IMessageRaw` returns an email message as it exists in the OST, and synchronization is not forced.</span></span> 
  
<span data-ttu-id="a122d-113">Das folgende Beispiel zeigt, wie Sie die **OpenEntry-Methode** aufrufen und anstatt  `IID_IMessageRaw`  `IID_IMessage` übergeben.</span><span class="sxs-lookup"><span data-stu-id="a122d-113">The following example shows how to call the **OpenEntry** method, passing  `IID_IMessageRaw` instead of  `IID_IMessage`.</span></span>
  
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

<span data-ttu-id="a122d-114">Wenn die **OpenEntry-Methode** den MAPI_E_INTERFACE_NOT_SUPPORTED zurückgibt, gibt sie an, dass der Nachrichtenspeicher den Zugriff auf die Nachricht im Unformatierungsmodus nicht unterstützt. </span><span class="sxs-lookup"><span data-stu-id="a122d-114">If the **OpenEntry** method returns the **MAPI_E_INTERFACE_NOT_SUPPORTED** error code, it indicates that the message store does not support accessing the message in raw mode.</span></span> <span data-ttu-id="a122d-115">Versuchen Sie in diesem Fall die **OpenEntry-Methode** erneut, indem Sie  `IID_IMessage` übergeben.</span><span class="sxs-lookup"><span data-stu-id="a122d-115">In this situation, try the **OpenEntry** method again by passing  `IID_IMessage`.</span></span>

> [!IMPORTANT]
>  <span data-ttu-id="a122d-116">`IID_IMessageRaw` möglicherweise nicht in der herunterladbaren Headerdatei definiert, über die Sie derzeit verfügen.</span><span class="sxs-lookup"><span data-stu-id="a122d-116">`IID_IMessageRaw` might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="a122d-117">In diesem Fall können Sie sie ihrem Code mithilfe der folgenden Definition hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a122d-117">In this case, you can add it to your code by using the following definition.</span></span> <span data-ttu-id="a122d-118">Verwenden Sie das DEFINE_OLEGUID, das in der Microsoft Windows Software Development Kit (SDK)-Headerdatei guiddef.h definiert ist, um den symbolischen NAMEN der GUID dem Wert zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="a122d-118">Use the DEFINE_OLEGUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate the GUID symbolic name with its value.</span></span> >  `#if !defined(INITGUID) || defined(USES_IID_IMessageRaw)`>  `DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0);`>  `#endif`
  
## <a name="see-also"></a><span data-ttu-id="a122d-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a122d-119">See also</span></span>

- [<span data-ttu-id="a122d-120">Informationen zu MAPI-Ergänzungen</span><span class="sxs-lookup"><span data-stu-id="a122d-120">About MAPI Additions</span></span>](about-mapi-additions.md) 
- [<span data-ttu-id="a122d-121">Zugreifen auf einen Speicher auf dem Remoteserver, wenn Outlook sich im Exchange-Cache-Modus befindet</span><span class="sxs-lookup"><span data-stu-id="a122d-121">Access a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="a122d-122">Öffnen eines Speichers auf dem Remoteserver, wenn Outlook sich im Exchange-Cache-Modus befindet</span><span class="sxs-lookup"><span data-stu-id="a122d-122">Open a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)

