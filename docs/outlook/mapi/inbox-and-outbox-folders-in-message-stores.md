---
title: Posteingang und Postausgang-Ordner in Nachrichtenspeicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8e4ce129-137d-4618-80a6-88781a578d01
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2bd71ee4fca53fbf3d309cbaf9d33835b84c0c2d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792684"
---
# <a name="inbox-and-outbox-folders-in-message-stores"></a><span data-ttu-id="fc801-103">Posteingang und Postausgang-Ordner in Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="fc801-103">Inbox and Outbox Folders in Message Stores</span></span>

  
  
<span data-ttu-id="fc801-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fc801-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fc801-p101">Um Standard-Informationsspeicher, muss ein Anbieter f�r Nachricht anmelden Posteingang zu implementieren und Ordner Postausgang. Sie werden in der Regel in der IPM-Unterstruktur eines Speichers Nachricht gespeichert. Diese Ordner sind spezielle darin, dass sie, dass Nachrichten an und von gesendet werden, aber keine besondere Funktionalit�t Ihnen ist als die Ordner eingesetzt werden. Senden und Empfangen von Nachrichten geschieht �ber definierten Aufrufsequenzen zwischen Clientanwendungen, die MAPI-Warteschlange und die Nachricht Speicheranbieter. Der Ordner Posteingang und Postausgang sind einfach Ordner, die verwendet werden, um Nachrichten zu speichern, w�hrend die Sequenzen aufrufen. Wichtig ist nicht, dass die Ordner sind spezielle oder sogar, dass sie den Posteingang und Postausgang benannt werden. die wichtig ist, dass der Nachricht Speicheranbieter im Rahmen des Supports verwendet zum Senden und Empfangen von Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="fc801-p101">To be the default message store, a message store provider must implement Inbox and Outbox folders. They are typically stored in the IPM subtree of a message store. These folders are special in that they are designated as the folders that messages are delivered to and sent from, but no special functionality is required of them. Sending and receiving messages happens by way of defined call sequences between client applications, the MAPI spooler, and the message store provider. The Inbox and Outbox folders are simply folders that are used to hold messages during those call sequences. The important point is not that the folders are special, or even that they are named Inbox and Outbox; the important point is that the message store provider uses them as part of its support for sending and receiving messages.</span></span>
  
<span data-ttu-id="fc801-p102">To support receiving messages, the message store provider must implement the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) and [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) methods. For more information, see [Empfangen von Nachrichten mithilfe von Nachrichtenspeicher Rollenanbietern](receiving-messages-by-using-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="fc801-p102">To support receiving messages, the message store provider must implement the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) and [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) methods. For more information, see [Receiving Messages by Using Message Store Providers](receiving-messages-by-using-message-store-providers.md).</span></span>
  
<span data-ttu-id="fc801-p103">To support sending messages, the message store provider must support the [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md) method, in addition to the other methods used by the MAPI spooler during the message sending process. A message store's outgoing queue does not have to correspond to an actual folder anywhere in the message store's folder tree. However, it is customary for a message store provider to show the contents of the outgoing message queue in the Outbox folder, if there is one. Doing so gives client applications a convenient way to indicate the status of messages that the user has sent, because an Outbox folder can be displayed along with all the other folders in a message store. For more information, see [Senden von Nachrichten mithilfe von Nachrichtenspeicher Rollenanbietern](sending-messages-by-using-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="fc801-p103">To support sending messages, the message store provider must support the [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md) method, in addition to the other methods used by the MAPI spooler during the message sending process. A message store's outgoing queue does not have to correspond to an actual folder anywhere in the message store's folder tree. However, it is customary for a message store provider to show the contents of the outgoing message queue in the Outbox folder, if there is one. Doing so gives client applications a convenient way to indicate the status of messages that the user has sent, because an Outbox folder can be displayed along with all the other folders in a message store. For more information, see [Sending Messages by Using Message Store Providers](sending-messages-by-using-message-store-providers.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fc801-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc801-118">See also</span></span>



[<span data-ttu-id="fc801-119">Implementieren von Ordnern in Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="fc801-119">Implementing Folders in Message Stores</span></span>](implementing-folders-in-message-stores.md)

