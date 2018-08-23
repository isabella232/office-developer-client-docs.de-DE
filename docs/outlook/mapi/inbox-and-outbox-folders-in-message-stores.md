---
title: Posteingang und Postausgang-Ordner in Nachrichtenspeicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8e4ce129-137d-4618-80a6-88781a578d01
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6781209cd1bf87f4becf1893b7cba5618549fbce
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582889"
---
# <a name="inbox-and-outbox-folders-in-message-stores"></a>Posteingang und Postausgang-Ordner in Nachrichtenspeicher

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Um Standard-Informationsspeicher, muss ein Anbieter f�r Nachricht anmelden Posteingang zu implementieren und Ordner Postausgang. Sie werden in der Regel in der IPM-Unterstruktur eines Speichers Nachricht gespeichert. Diese Ordner sind spezielle darin, dass sie, dass Nachrichten an und von gesendet werden, aber keine besondere Funktionalit�t Ihnen ist als die Ordner eingesetzt werden. Senden und Empfangen von Nachrichten geschieht �ber definierten Aufrufsequenzen zwischen Clientanwendungen, die MAPI-Warteschlange und die Nachricht Speicheranbieter. Der Ordner Posteingang und Postausgang sind einfach Ordner, die verwendet werden, um Nachrichten zu speichern, w�hrend die Sequenzen aufrufen. Wichtig ist nicht, dass die Ordner sind spezielle oder sogar, dass sie den Posteingang und Postausgang benannt werden. die wichtig ist, dass der Nachricht Speicheranbieter im Rahmen des Supports verwendet zum Senden und Empfangen von Nachrichten.
  
To support receiving messages, the message store provider must implement the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) and [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) methods. For more information, see [Empfangen von Nachrichten mithilfe von Nachrichtenspeicher Rollenanbietern](receiving-messages-by-using-message-store-providers.md).
  
To support sending messages, the message store provider must support the [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md) method, in addition to the other methods used by the MAPI spooler during the message sending process. A message store's outgoing queue does not have to correspond to an actual folder anywhere in the message store's folder tree. However, it is customary for a message store provider to show the contents of the outgoing message queue in the Outbox folder, if there is one. Doing so gives client applications a convenient way to indicate the status of messages that the user has sent, because an Outbox folder can be displayed along with all the other folders in a message store. For more information, see [Senden von Nachrichten mithilfe von Nachrichtenspeicher Rollenanbietern](sending-messages-by-using-message-store-providers.md).
  
## <a name="see-also"></a>Siehe auch



[Implementieren von Ordnern in Nachrichtenspeicher](implementing-folders-in-message-stores.md)

