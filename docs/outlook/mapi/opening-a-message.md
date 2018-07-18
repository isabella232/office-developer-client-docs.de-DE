---
title: Öffnen einer Nachricht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 142c4975-08df-4501-9996-557aa44eafb3
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4ea75f723a2fcb242d8b9a516498855aa20cfdd4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793303"
---
# <a name="opening-a-message"></a><span data-ttu-id="0786d-103">Öffnen einer Nachricht</span><span class="sxs-lookup"><span data-stu-id="0786d-103">Opening a message</span></span>
 
<span data-ttu-id="0786d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0786d-104">**Applies to**: Outlook</span></span> 
  
### <a name="to-open-a-message"></a><span data-ttu-id="0786d-105">Öffnen eine Nachricht</span><span class="sxs-lookup"><span data-stu-id="0786d-105">To open a message</span></span>
  
1. <span data-ttu-id="0786d-106">Abrufen von Eintrags-ID der Nachricht aus einer der folgenden Quellen:</span><span class="sxs-lookup"><span data-stu-id="0786d-106">Retrieve the message's entry identifier from one of the following sources:</span></span>
    
   - <span data-ttu-id="0786d-107">Die Zeile, die die Nachricht in der Inhaltstabelle des übergeordneten Ordners darstellt.</span><span class="sxs-lookup"><span data-stu-id="0786d-107">The row that represents the message in the contents table of its parent folder.</span></span> <span data-ttu-id="0786d-108">Weitere Informationen zum Arbeiten mit einem Ordner Inhaltstabelle finden Sie unter [Inhalt Tabellen](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="0786d-108">For more information about working with a folder contents table, see [Contents Tables](contents-tables.md).</span></span>
    
   - <span data-ttu-id="0786d-109">Der **LpEntryID** Member der [NEWMAIL_NOTIFICATION](newmail_notification.md) -Struktur, die mit einer neuen e-Mail-Benachrichtigung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="0786d-109">The **lpEntryID** member of the [NEWMAIL_NOTIFICATION](newmail_notification.md) structure that is sent with a new mail notification.</span></span> <span data-ttu-id="0786d-110">Weitere Informationen zu empfangen und Behandlung Benachrichtigungen finden Sie unter [Behandeln von Benachrichtigungen](handling-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="0786d-110">For more information about receiving and handling notifications, see [Handling Notifications](handling-notifications.md).</span></span>
    
   - <span data-ttu-id="0786d-111">Anruf an die Nachricht [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode, die Eigenschaft **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) anfordert.</span><span class="sxs-lookup"><span data-stu-id="0786d-111">A call to the message's [IMAPIProp::GetProps](imapiprop-getprops.md) method requesting the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span> 
    
2. <span data-ttu-id="0786d-112">Rufen Sie eine der folgenden Methoden **OpenEntry** zum Öffnen der Nachricht, die Einstellung _LpEntryID_ an die Nachricht Eintrags-ID:</span><span class="sxs-lookup"><span data-stu-id="0786d-112">Call one of the following **OpenEntry** methods to open the message, setting  _lpEntryID_ to the message's entry identifier:</span></span> 
    
   - [<span data-ttu-id="0786d-113">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="0786d-113">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
    
   - [<span data-ttu-id="0786d-114">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="0786d-114">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
    
   - [<span data-ttu-id="0786d-115">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="0786d-115">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
    
  <span data-ttu-id="0786d-116">Die schnellste Methode kann nur für eingehende Nachrichten verwendet werden und umfasst den Empfangsordner **IMAPIFolder::OpenEntry** -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="0786d-116">The fastest method is usable only for incoming messages and involves calling the receive folder's **IMAPIFolder::OpenEntry** method.</span></span> <span data-ttu-id="0786d-117">Die nächste schnellste Methode aufrufen der Nachrichtenspeicher **IMsgStore::OpenEntry** -Methode kann für alle Nachrichten verwendet werden, wie die langsamste-Methode aufrufen **IMAPISession::OpenEntry**ist.</span><span class="sxs-lookup"><span data-stu-id="0786d-117">The next fastest method, calling the message store's **IMsgStore::OpenEntry** method, is usable for all messages as is the slowest method, calling **IMAPISession::OpenEntry**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="0786d-118">Ordner und deren Inhalt Tabellen können geschlossen werden können Sie jederzeit ohne Beeinträchtigung der keines der Nachrichten, die darin enthaltenen aus geöffnet wurden.</span><span class="sxs-lookup"><span data-stu-id="0786d-118">Folders and their contents tables can be closed at any time without adversely affecting any of the messages that were opened from within them.</span></span> 
  
### <a name="to-open-a-message-that-has-been-saved-on-disk"></a><span data-ttu-id="0786d-119">Um eine Nachricht zu öffnen, die auf dem Datenträger gespeichert wurde</span><span class="sxs-lookup"><span data-stu-id="0786d-119">To open a message that has been saved on disk</span></span>
  
1. <span data-ttu-id="0786d-120">Rufen Sie **StgOpenStorage** zum Abrufen eines **IStorage** Schnittstelle Zeigers, übergeben Sie den Namen der Nachrichtendatei für den Parameter _PwcsName_ .</span><span class="sxs-lookup"><span data-stu-id="0786d-120">Call **StgOpenStorage** to retrieve an **IStorage** interface pointer, passing the name of the message file for the  _pwcsName_ parameter.</span></span> 
    
   ```cpp
    LPSTORAGE pStorage = NULL;
    HRESULT hr = StgOpenStorage (L"MESSAGE.MSG", NULL,
                                STGM_TRANSACTED |
                                STGM_READWRITE |
                                STGM_SHARE_EXCLUSIVE,
                                NULL, 0, &pStorage);
    
   ```

2. <span data-ttu-id="0786d-121">Rufen Sie **OpenIMsgOnIStg** zum Abrufen eines **IMessage** -Schnittstelle Zeigers Zugriff auf die Nachricht.</span><span class="sxs-lookup"><span data-stu-id="0786d-121">Call **OpenIMsgOnIStg** to retrieve an **IMessage** interface pointer to access the message.</span></span> 
    
   ```cpp
    LPMESSAGE pMessage = NULL;
    LPMALLOC pMalloc = MAPIGetDefaultMalloc();
    hr = OpenIMsgOnIStg (NULL, MAPIAllocateBuffer, MAPIAllocateMore,
                        MAPIFreeBuffer, pMalloc, NULL, pStorage,
                        NULL, 0, 0, &pMessage);
    
   ```


