---
title: Zugriff auf einen Speicher auf dem Remoteserver, wenn Outlook im Exchange-Cache-Modus befindet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5c6df156-4015-2d0f-26b7-07055a3f7810
description: 'Zuletzt geändert: 02 Juli 2012'
ms.openlocfilehash: 8ab92287b6df5b510558d7adf50a61c17a823d74
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585927"
---
# <a name="access-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a><span data-ttu-id="4c1c6-103">Zugriff auf einen Speicher auf dem Remoteserver, wenn Outlook im Exchange-Cache-Modus befindet</span><span class="sxs-lookup"><span data-stu-id="4c1c6-103">Access a store on the remote server when Outlook is in Cached Exchange Mode</span></span>
 
<span data-ttu-id="4c1c6-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c1c6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c1c6-105">Dieses Thema enthält ein Codebeispiel in C++, das zeigt, wie Sie die Kennzeichen **MAPI_NO_CACHE** zum Öffnen eines Ordners oder einer Nachricht auf einen Nachrichtenspeicher auf dem Remoteserver, wenn Microsoft Office Outlook in der Exchange-Cache-Modus befindet.</span><span class="sxs-lookup"><span data-stu-id="4c1c6-105">This topic contains a code sample in C++ that shows how to use the **MAPI_NO_CACHE** flag to open a folder or a message on a message store on the remote server when Microsoft Office Outlook is in Cached Exchange Mode.</span></span> 
  
<span data-ttu-id="4c1c6-106">Exchange-Cache-Modus ermöglicht Outlook eine lokale Kopie des Postfachs eines Benutzers verwendet, während Outlook eine online-Verbindung zu einer remote-Kopie des Postfachs des Benutzers, auf dem Exchange-Remoteserver verwaltet.</span><span class="sxs-lookup"><span data-stu-id="4c1c6-106">Cached Exchange Mode permits Outlook to use a local copy of a user's mailbox while Outlook maintains an online connection to a remote copy of the user's mailbox on the remote Exchange server.</span></span> <span data-ttu-id="4c1c6-107">Wenn Outlook im Exchange-Cache-Modus, wird standardmäßig ausgeführt wird werden alle MAPI-Lösungen, die auf der gleichen Sitzung anmelden auch mit dem Cache Nachrichtenspeicher verbunden.</span><span class="sxs-lookup"><span data-stu-id="4c1c6-107">When Outlook is running in Cached Exchange Mode, by default, any MAPI solutions that log on to the same session are also connected to the cached message store.</span></span> <span data-ttu-id="4c1c6-108">Anhand der lokalen Kopie des Postfachs werden alle Daten, die zugegriffen werden kann und alle vorgenommenen Änderungen vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="4c1c6-108">Any data that is accessed and any changes that are made are made against the local copy of the mailbox.</span></span>
  
<span data-ttu-id="4c1c6-109">Ein Client oder Dienstanbieter kann die Verbindung mit den lokalen Nachrichtenspeicher überschreiben und öffnen Sie eine Nachricht oder einen Ordner auf dem remote-Speicher durch das Bit beim Aufruf von **[IMsgStore::OpenEntry](imsgstore-openentry.md)** für **MAPI_NO_CACHE** im *UlFlags* -Parameter festlegen.</span><span class="sxs-lookup"><span data-stu-id="4c1c6-109">A client or service provider can override the connection to the local message store and open a message or a folder on the remote store by setting the bit for **MAPI_NO_CACHE** in the  *ulFlags*  parameter when calling **[IMsgStore::OpenEntry](imsgstore-openentry.md)**.</span></span> 
  
<span data-ttu-id="4c1c6-110">Das folgende Codebeispiel zeigt, wie **IMsgStore::OpenEntry** mit dem im Parameter *UlFlags* legen Sie zum Öffnen des Ordners "Root" auf dem remote-Nachrichtenspeicher **MAPI_NO_CACHE** -Flag aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4c1c6-110">The following code sample shows how to call **IMsgStore::OpenEntry** with the **MAPI_NO_CACHE** flag set in the  *ulFlags*  parameter to open the root folder on the remote message store.</span></span> 
  
```cpp
HRESULT HrOpenRootFolder ( 
    LPMDB lpMDB, 
    LPMESSAGE* lpRootFolder) 
{ 
    ULONG ulObjType = NULL; 
    HRESULT hRes = lpMDB-&gt;OpenEntry( 
        0,// size of entry ID       
        NULL,                                   // Pointer to entry ID 
        NULL,                                   // Use default interface (IMAPIFolder) 
        MAPI_BEST_ACCESS | MAPI_NO_CACHE,       // Flags 
        &amp;ulObjType,
// Output parameter indicates the type of object returned 
        (LPUNKNOWN *) lpRootFolder));           // Pointer to put the opened folder in 
    return hRes; 
 
}
```

<span data-ttu-id="4c1c6-111">Wenn Sie mit dem **MDB_ONLINE** -Flag auf dem Remoteserver Nachrichtenspeicher geöffnet haben, müssen Sie keinen **MAPI_NO_CACHE** -Flag verwenden.</span><span class="sxs-lookup"><span data-stu-id="4c1c6-111">If you opened the message store with the **MDB_ONLINE** flag on the remote server, you do not have to use the **MAPI_NO_CACHE** flag.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4c1c6-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4c1c6-112">See also</span></span>

- [<span data-ttu-id="4c1c6-113">Informationen zu MAPI-Ergänzungen</span><span class="sxs-lookup"><span data-stu-id="4c1c6-113">About MAPI Additions</span></span>](about-mapi-additions.md)
- [<span data-ttu-id="4c1c6-114">Öffnen eines Speichers auf dem Remote-Server, wenn Outlook sich im Exchange-Cache-Modus befindet</span><span class="sxs-lookup"><span data-stu-id="4c1c6-114">Open a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="4c1c6-115">Verwalten einer Nachricht in einem OST ohne Aufrufen einer Synchronisierung im Exchange-Cache-Modus</span><span class="sxs-lookup"><span data-stu-id="4c1c6-115">Manage a Message in an OST Without Invoking a Synchronization in Cached Exchange Mode</span></span>](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

