---
title: Bereitstellen von Gelesen/Ungelesen-Berichten für Nachrichtenspeicheranbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9644b8c5-ecc0-4ea3-972a-2169c78b99e5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8e2552cbeaf528de634c39a5ebd175a2615782b3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594439"
---
# <a name="providing-read-and-nonread-reports-for-message-store-providers"></a>Bereitstellen von Gelesen/Ungelesen-Berichten für Nachrichtenspeicheranbieter

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Wenn eine Nachricht Speicheranbieter Nachrichten empfangen kann, ist es erforderlich, wenn lesen und nonread Berichte von Nachrichten, die vom Anbieter Store Nachricht empfangen. Wenn eine empfangene Nachricht die **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))-Eigenschaft enthält und der Wert dieser Eigenschaft TRUE ist, sollte der Nachrichtenspeicher eine Benachrichtigung an den Absender senden, wenn der Benutzer die Nachricht öffnet, Gibt an, dass die Nachricht gelesen wurde. Auf ähnliche Weise, wenn der Benutzer die Nachricht vor dem Öffnen löscht, sollte der Nachrichtenspeicher Problem eine Antwort an den Absender, was bedeutet, dass die Nachricht nicht gelesen wurde.
  
Diese Berichte ausstellen ist eine Frage über das Erstellen einer [IMessage: IMAPIProp](imessageimapiprop.md) -Objekt, die relevanten Eigenschaften für die Nachricht ausfüllen und an die MAPI-Warteschlange senden, als ob die Nachricht mit dem Benutzer stammen. Die [IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) -Methode kann für diese verwendet werden. 
  
> [!NOTE]
> Spezielle muss darauf geachtet werden bei ein Nachrichtenspeicher Kopien einer ungelesenen Nachricht mit ausstehenden gelesen oder nonread Berichte. Diese Berichte sollten nicht generiert werden, wenn Benutzer alle Kopien einer Nachricht lesen für die Berichte angefordert wurden. Wenn Sie eine Kopie einer solchen Nachricht zu erstellen, sollte der Nachricht Speicheranbieter die Flags CLEAR_RN_PENDING und CLEAR_NRN_PENDING in seiner Aufrufen von [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) und [IMessage::SetReadFlag](imessage-setreadflag.md)enthalten. 
  
## <a name="see-also"></a>Siehe auch



[Nachrichtenspeicher-Features](message-store-features.md)

