---
title: Zugreifen auf einen Speicher auf dem Remoteserver, Outlook sich im Cache-Exchange-Modus befindet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5c6df156-4015-2d0f-26b7-07055a3f7810
description: 'Letzte Änderung: 02. Juli 2012'
ms.openlocfilehash: cfc20c1a9ca4510ffec86bf16666f1fc50822321
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433864"
---
# <a name="access-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a><span data-ttu-id="78561-103">Zugreifen auf einen Speicher auf dem Remoteserver, Outlook sich im Cache-Exchange-Modus befindet</span><span class="sxs-lookup"><span data-stu-id="78561-103">Access a store on the remote server when Outlook is in Cached Exchange Mode</span></span>
 
<span data-ttu-id="78561-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78561-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78561-105">Dieses Thema enthält ein Codebeispiel in C++, in dem gezeigt wird, wie Sie das **MAPI_NO_CACHE-Flag** verwenden, um einen Ordner oder eine Nachricht in einem Nachrichtenspeicher auf dem Remoteserver zu öffnen, wenn Microsoft Office Outlook sich im Cached Exchange Mode befindet.</span><span class="sxs-lookup"><span data-stu-id="78561-105">This topic contains a code sample in C++ that shows how to use the **MAPI_NO_CACHE** flag to open a folder or a message on a message store on the remote server when Microsoft Office Outlook is in Cached Exchange Mode.</span></span> 
  
<span data-ttu-id="78561-106">Im cached Exchange Mode können Outlook eine lokale Kopie des Postfachs eines Benutzers verwenden, während Outlook eine Onlineverbindung mit einer Remotekopie des Postfachs des Benutzers auf dem Remoteserver Exchange verwaltet.</span><span class="sxs-lookup"><span data-stu-id="78561-106">Cached Exchange Mode permits Outlook to use a local copy of a user's mailbox while Outlook maintains an online connection to a remote copy of the user's mailbox on the remote Exchange server.</span></span> <span data-ttu-id="78561-107">Wenn Outlook im Cached Exchange Mode ausgeführt wird, sind standardmäßig alle MAPI-Lösungen, die sich bei derselben Sitzung anmelden, auch mit dem zwischengespeicherten Nachrichtenspeicher verbunden.</span><span class="sxs-lookup"><span data-stu-id="78561-107">When Outlook is running in Cached Exchange Mode, by default, any MAPI solutions that log on to the same session are also connected to the cached message store.</span></span> <span data-ttu-id="78561-108">Alle Daten, auf die zugegriffen wird, und alle vorgenommenen Änderungen werden für die lokale Kopie des Postfachs vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="78561-108">Any data that is accessed and any changes that are made are made against the local copy of the mailbox.</span></span>
  
<span data-ttu-id="78561-109">Ein Client oder Dienstanbieter kann die Verbindung zum lokalen Nachrichtenspeicher überschreiben und eine Nachricht oder einen Ordner im Remotespeicher öffnen, indem er das Bit für **MAPI_NO_CACHE** im  *ulFlags-Parameter*  beim Aufrufen von **[IMsgStore::OpenEntry](imsgstore-openentry.md)** festlegen.</span><span class="sxs-lookup"><span data-stu-id="78561-109">A client or service provider can override the connection to the local message store and open a message or a folder on the remote store by setting the bit for **MAPI_NO_CACHE** in the  *ulFlags*  parameter when calling **[IMsgStore::OpenEntry](imsgstore-openentry.md)**.</span></span> 
  
<span data-ttu-id="78561-110">Im folgenden Codebeispiel wird gezeigt, wie **IMsgStore::OpenEntry** mit dem im *ulFlags-Parameter* festgelegten **MAPI_NO_CACHE-Flag** zum Öffnen des Stammordners im Remotenachrichtenspeicher aufruft.</span><span class="sxs-lookup"><span data-stu-id="78561-110">The following code sample shows how to call **IMsgStore::OpenEntry** with the **MAPI_NO_CACHE** flag set in the  *ulFlags*  parameter to open the root folder on the remote message store.</span></span> 
  
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

<span data-ttu-id="78561-111">Wenn Sie den Nachrichtenspeicher  mit dem MDB_ONLINE auf dem Remoteserver geöffnet haben, müssen Sie das MAPI_NO_CACHE **verwenden.**</span><span class="sxs-lookup"><span data-stu-id="78561-111">If you opened the message store with the **MDB_ONLINE** flag on the remote server, you do not have to use the **MAPI_NO_CACHE** flag.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="78561-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78561-112">See also</span></span>

- [<span data-ttu-id="78561-113">Informationen zu MAPI-Ergänzungen</span><span class="sxs-lookup"><span data-stu-id="78561-113">About MAPI Additions</span></span>](about-mapi-additions.md) 
- [<span data-ttu-id="78561-114">Öffnen eines Speichers auf dem Remoteserver, wenn Outlook sich im Exchange-Cache-Modus befindet</span><span class="sxs-lookup"><span data-stu-id="78561-114">Open a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="78561-115">Verwalten einer Nachricht in einem OST ohne Aufrufen einer Synchronisierung im Exchange-Cache-Modus</span><span class="sxs-lookup"><span data-stu-id="78561-115">Manage a Message in an OST Without Invoking a Synchronization in Cached Exchange Mode</span></span>](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

