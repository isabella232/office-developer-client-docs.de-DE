---
title: Bereitstellen von Lese- und nicht gelesenen Berichten für Nachrichten Store-Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 9644b8c5-ecc0-4ea3-972a-2169c78b99e5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 15a2868519e5b8a4363e23ccf1cc3037d630f162
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599158"
---
# <a name="providing-read-and-nonread-reports-for-message-store-providers"></a>Bereitstellen von Lese- und nicht gelesenen Berichten für Nachrichten Store-Anbieter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn ein Nachrichtenspeicheranbieter Nachrichten empfangen kann, ist es erforderlich, Leseberichte und nicht gelesene Berichte von Nachrichten zu unterstützen, die vom Nachrichtenspeicheranbieter empfangen wurden. Wenn eine empfangene Nachricht die **eigenschaft PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) enthält und der Wert dieser Eigenschaft TRUE ist, sollte der Nachrichtenspeicher eine Benachrichtigung an den Absender senden, wenn der Benutzer die Nachricht öffnet und angibt, dass die Nachricht gelesen wurde. Wenn der Benutzer die Nachricht vor dem Öffnen löscht, sollte der Nachrichtenspeicher eine Antwort an den Absender ausgeben, die angibt, dass die Nachricht nicht gelesen wurde.
  
Beim Ausgeben dieser Berichte geht es darum, ein [IMessage : IMAPIProp-Objekt](imessageimapiprop.md) zu erstellen, die relevanten Eigenschaften für die Nachricht auszufüllen und an den MAPI-Spooler zu übermitteln, als ob die Nachricht vom Benutzer stammt hätte. Die [IMAPISupport::ReadReceipt-Methode](imapisupport-readreceipt.md) kann dafür verwendet werden. 
  
> [!NOTE]
> Besondere Vorsicht ist geboten, wenn ein Nachrichtenspeicher Kopien einer ungelesenen Nachricht mit ausstehenden oder nicht gelesenen Berichten erstellt. Solche Berichte sollten nicht generiert werden, wenn Benutzer Kopien einer Nachricht lesen, für die Berichte angefordert wurden. Beim Erstellen einer Kopie einer solchen Nachricht sollte der Nachrichtenspeicheranbieter die CLEAR_RN_PENDING und CLEAR_NRN_PENDING Flags in die Aufrufe von [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) und [IMessage::SetReadFlag](imessage-setreadflag.md)einschließen. 
  
## <a name="see-also"></a>Siehe auch



[Nachrichtenspeicher-Features](message-store-features.md)

