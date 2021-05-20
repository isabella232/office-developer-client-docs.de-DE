---
title: Bereitstellen von Lese- und Ungelesenberichten für Store-Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9644b8c5-ecc0-4ea3-972a-2169c78b99e5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 96546d3d766af398ff7acb50f4fc3a479b5668b2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432338"
---
# <a name="providing-read-and-nonread-reports-for-message-store-providers"></a>Bereitstellen von Lese- und Ungelesenberichten für Store-Anbieter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn ein Nachrichtenspeicheranbieter Nachrichten empfangen kann, muss er Leseberichte und nicht gelesene Berichte von Nachrichten unterstützen, die vom Nachrichtenspeicheranbieter empfangen werden. Wenn eine empfangene Nachricht die **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))-Eigenschaft enthält und der Wert dieser Eigenschaft TRUE ist, sollte der Nachrichtenspeicher eine Benachrichtigung an den Absender senden, wenn der Benutzer die Nachricht öffnet, was angibt, dass die Nachricht gelesen wurde. Wenn der Benutzer die Nachricht vor dem Öffnen löscht, sollte der Nachrichtenspeicher eine Antwort an den Absender senden, die angibt, dass die Nachricht nicht gelesen wurde.
  
Das Ausgeben dieser Berichte besteht in der Erstellung eines [IMessage : IMAPIProp-Objekts,](imessageimapiprop.md) dem Ausfüllen der relevanten Eigenschaften für die Nachricht und dem Übermitteln an den MAPI-Spooler, als ob die Nachricht mit dem Benutzer erstellt worden wäre. Dazu [kann die IMAPISupport::ReadReceipt-Methode](imapisupport-readreceipt.md) verwendet werden. 
  
> [!NOTE]
> Besondere Vorsicht ist zu finden, wenn ein Nachrichtenspeicher Kopien einer ungelesenen Nachricht mit ausstehenden lese- oder nicht gelesenen Berichten macht. Solche Berichte sollten nicht generiert werden, wenn Benutzer Kopien einer Nachricht lesen, für die Berichte angefordert wurden. Beim Erstellen einer Kopie einer solchen Nachricht sollte der Nachrichtenspeicheranbieter die CLEAR_RN_PENDING- und CLEAR_NRN_PENDING-Flags in seine Aufrufe an [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) und [IMessage::SetReadFlag einfügen.](imessage-setreadflag.md) 
  
## <a name="see-also"></a>Siehe auch



[Nachrichtenspeicher-Features](message-store-features.md)

