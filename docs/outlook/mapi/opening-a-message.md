---
title: Öffnen einer Nachricht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 142c4975-08df-4501-9996-557aa44eafb3
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bf633a971f7e3077ce2f418021ef183a36db8cc8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348608"
---
# <a name="opening-a-message"></a><span data-ttu-id="7f672-103">Öffnen einer Nachricht</span><span class="sxs-lookup"><span data-stu-id="7f672-103">Opening a message</span></span>
 
<span data-ttu-id="7f672-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f672-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
### <a name="to-open-a-message"></a><span data-ttu-id="7f672-105">So öffnen Sie eine Nachricht</span><span class="sxs-lookup"><span data-stu-id="7f672-105">To open a message</span></span>
  
1. <span data-ttu-id="7f672-106">Rufen Sie die Eintrags-ID der Nachricht aus einer der folgenden Quellen ab:</span><span class="sxs-lookup"><span data-stu-id="7f672-106">Retrieve the message's entry identifier from one of the following sources:</span></span>
    
   - <span data-ttu-id="7f672-107">Die Zeile, die die Nachricht in der Inhaltstabelle des übergeordneten Ordners darstellt.</span><span class="sxs-lookup"><span data-stu-id="7f672-107">The row that represents the message in the contents table of its parent folder.</span></span> <span data-ttu-id="7f672-108">Weitere Informationen zum Arbeiten mit einer Ordnerinhaltstabelle finden Sie unter [Inhaltstabellen](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="7f672-108">For more information about working with a folder contents table, see [Contents Tables](contents-tables.md).</span></span>
    
   - <span data-ttu-id="7f672-109">Das **lpEntryID** -Element der [NEWMAIL_NOTIFICATION](newmail_notification.md) -Struktur, die mit einer neuen e-Mail-Benachrichtigung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="7f672-109">The **lpEntryID** member of the [NEWMAIL_NOTIFICATION](newmail_notification.md) structure that is sent with a new mail notification.</span></span> <span data-ttu-id="7f672-110">Weitere Informationen zum empfangen und Verarbeiten von Benachrichtigungen finden Sie unter [Handling Notifications](handling-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="7f672-110">For more information about receiving and handling notifications, see [Handling Notifications](handling-notifications.md).</span></span>
    
   - <span data-ttu-id="7f672-111">Ein Aufruf der [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode der Nachricht, die die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft anfordert.</span><span class="sxs-lookup"><span data-stu-id="7f672-111">A call to the message's [IMAPIProp::GetProps](imapiprop-getprops.md) method requesting the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span> 
    
2. <span data-ttu-id="7f672-112">Rufen Sie eine der folgenden **OpenEntry** -Methoden auf, um die Nachricht zu öffnen, und legen Sie _lpEntryID_ auf die Eintrags-ID der Nachricht fest:</span><span class="sxs-lookup"><span data-stu-id="7f672-112">Call one of the following **OpenEntry** methods to open the message, setting  _lpEntryID_ to the message's entry identifier:</span></span> 
    
   - [<span data-ttu-id="7f672-113">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="7f672-113">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
    
   - [<span data-ttu-id="7f672-114">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="7f672-114">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
    
   - [<span data-ttu-id="7f672-115">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="7f672-115">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
    
  <span data-ttu-id="7f672-116">Die schnellste Methode ist nur für eingehende Nachrichten nutzbar und umfasst das Aufrufen der **IMAPIFolder:: OpenEntry** -Methode des Empfänger Ordners.</span><span class="sxs-lookup"><span data-stu-id="7f672-116">The fastest method is usable only for incoming messages and involves calling the receive folder's **IMAPIFolder::OpenEntry** method.</span></span> <span data-ttu-id="7f672-117">Die nächste schnellste Methode, die **IMsgStore:: OpenEntry** -Methode des Nachrichtenspeichers aufzurufen, ist für alle Nachrichten verwendbar, ebenso wie die langsamste Methode, indem **IMAPISession:: OpenEntry**aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="7f672-117">The next fastest method, calling the message store's **IMsgStore::OpenEntry** method, is usable for all messages as is the slowest method, calling **IMAPISession::OpenEntry**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="7f672-118">Ordner und deren Inhaltstabellen können jederzeit geschlossen werden, ohne dass sich dies nachteilig auf die Nachrichten auswirkt, die in diesen geöffnet wurden.</span><span class="sxs-lookup"><span data-stu-id="7f672-118">Folders and their contents tables can be closed at any time without adversely affecting any of the messages that were opened from within them.</span></span> 
  
### <a name="to-open-a-message-that-has-been-saved-on-disk"></a><span data-ttu-id="7f672-119">So öffnen Sie eine Nachricht, die auf dem Datenträger gespeichert wurde</span><span class="sxs-lookup"><span data-stu-id="7f672-119">To open a message that has been saved on disk</span></span>
  
1. <span data-ttu-id="7f672-120">Rufen Sie **StgOpenStorage** auf, um einen **IStorage** -Schnittstellenzeiger abzurufen, und übergeben Sie den Namen der Nachrichtendatei für den _pwcsName_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="7f672-120">Call **StgOpenStorage** to retrieve an **IStorage** interface pointer, passing the name of the message file for the  _pwcsName_ parameter.</span></span> 
    
   ```cpp
    LPSTORAGE pStorage = NULL;
    HRESULT hr = StgOpenStorage (L"MESSAGE.MSG", NULL,
                                STGM_TRANSACTED |
                                STGM_READWRITE |
                                STGM_SHARE_EXCLUSIVE,
                                NULL, 0, &pStorage);
    
   ```

2. <span data-ttu-id="7f672-121">Aufrufen von **OpenIMsgOnIStg** zum Abrufen eines **IMessage** -Schnittstellenzeigers für den Zugriff auf die Nachricht.</span><span class="sxs-lookup"><span data-stu-id="7f672-121">Call **OpenIMsgOnIStg** to retrieve an **IMessage** interface pointer to access the message.</span></span> 
    
   ```cpp
    LPMESSAGE pMessage = NULL;
    LPMALLOC pMalloc = MAPIGetDefaultMalloc();
    hr = OpenIMsgOnIStg (NULL, MAPIAllocateBuffer, MAPIAllocateMore,
                        MAPIFreeBuffer, pMalloc, NULL, pStorage,
                        NULL, 0, 0, &pMessage);
    
   ```


