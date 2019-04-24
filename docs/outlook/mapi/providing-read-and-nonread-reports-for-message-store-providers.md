---
title: Bereitstellen von Lese-und nonread-Berichten für Nachrichtenspeicher Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9644b8c5-ecc0-4ea3-972a-2169c78b99e5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 96546d3d766af398ff7acb50f4fc3a479b5668b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328511"
---
# <a name="providing-read-and-nonread-reports-for-message-store-providers"></a>Bereitstellen von Lese-und nonread-Berichten für Nachrichtenspeicher Anbieter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn ein Nachrichtenspeicher Anbieter Nachrichten empfangen kann, muss er Lese Berichte und nicht gelesene Berichte über vom Nachrichtenspeicher Anbieter empfangene Nachrichten unterstützen. Wenn eine empfangene Nachricht die **PR_READ_RECEIPT_REQUESTED** ([pidtagreadreceiptrequested (](pidtagreadreceiptrequested-canonical-property.md))-Eigenschaft enthält und der Wert der Eigenschaft auf true festgelegt ist, sollte der Nachrichtenspeicher eine Benachrichtigung an den Absender senden, wenn der Benutzer die Nachricht öffnet. Gibt an, dass die Nachricht gelesen wurde. Entsprechend sollte der Nachrichtenspeicher, wenn der Benutzer die Nachricht vor dem Öffnen löscht, eine Antwort an den Absender ausgeben, der angibt, dass die Nachricht nicht gelesen wurde.
  
Das ausgeben dieser Berichte betrifft das Erstellen eines [IMessage: IMAPIProp](imessageimapiprop.md) -Objekts, das Ausfüllen der relevanten Eigenschaften der Nachricht und die Übermittlung an den MAPI-Spooler, als ob die Nachricht mit dem Benutzer entstanden wäre. Die [IMAPISupport:: ReadReceipt](imapisupport-readreceipt.md) -Methode kann dafür verwendet werden. 
  
> [!NOTE]
> Besondere Vorsicht ist erforderlich, wenn ein Nachrichtenspeicher Kopien einer ungelesenen Nachricht mit ausstehenden Lese-oder nicht gelesenen Berichten erstellt. Solche Berichte sollten nicht generiert werden, wenn Benutzer Kopien einer Nachricht lesen, für die Berichte angefordert wurden. Beim Erstellen einer Kopie einer solchen Nachricht sollte der Nachrichtenspeicher Anbieter die CLEAR_RN_PENDING-und CLEAR_NRN_PENDING-Flags in seine Aufrufe an [IMAPIFolder:: SetReadFlags](imapifolder-setreadflags.md) und [IMessage:: SetReadFlag](imessage-setreadflag.md)aufnehmen. 
  
## <a name="see-also"></a>Siehe auch



[Nachrichtenspeicher-Features](message-store-features.md)

