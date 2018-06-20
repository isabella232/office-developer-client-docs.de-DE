---
title: Lesen und Nonread von Berichten bereitstellen für Nachrichtenspeicher Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9644b8c5-ecc0-4ea3-972a-2169c78b99e5
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b082d063cc77be46fcd3d4e07ec6753f78f8f335
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795361"
---
# <a name="providing-read-and-nonread-reports-for-message-store-providers"></a><span data-ttu-id="94a1e-103">Lesen und Nonread von Berichten bereitstellen für Nachrichtenspeicher Anbieter</span><span class="sxs-lookup"><span data-stu-id="94a1e-103">Providing Read and Nonread Reports for Message Store Providers</span></span>

  
  
<span data-ttu-id="94a1e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="94a1e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="94a1e-105">Wenn eine Nachricht Speicheranbieter Nachrichten empfangen kann, ist es erforderlich, wenn lesen und nonread Berichte von Nachrichten, die vom Anbieter Store Nachricht empfangen.</span><span class="sxs-lookup"><span data-stu-id="94a1e-105">If a message store provider can receive messages, it is required to support read reports and nonread reports of messages received by the message store provider.</span></span> <span data-ttu-id="94a1e-106">Wenn eine empfangene Nachricht die **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))-Eigenschaft enthält und der Wert dieser Eigenschaft TRUE ist, sollte der Nachrichtenspeicher eine Benachrichtigung an den Absender senden, wenn der Benutzer die Nachricht öffnet, Gibt an, dass die Nachricht gelesen wurde.</span><span class="sxs-lookup"><span data-stu-id="94a1e-106">If a received message contains the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property and that property's value is TRUE, the message store should send a notification message to the sender when the user opens the message, indicating that the message has been read.</span></span> <span data-ttu-id="94a1e-107">Auf ähnliche Weise, wenn der Benutzer die Nachricht vor dem Öffnen löscht, sollte der Nachrichtenspeicher Problem eine Antwort an den Absender, was bedeutet, dass die Nachricht nicht gelesen wurde.</span><span class="sxs-lookup"><span data-stu-id="94a1e-107">Similarly, if the user deletes the message before opening it, the message store should issue a reply to the sender indicating that the message was not read.</span></span>
  
<span data-ttu-id="94a1e-108">Diese Berichte ausstellen ist eine Frage über das Erstellen einer [IMessage: IMAPIProp](imessageimapiprop.md) -Objekt, die relevanten Eigenschaften für die Nachricht ausfüllen und an die MAPI-Warteschlange senden, als ob die Nachricht mit dem Benutzer stammen.</span><span class="sxs-lookup"><span data-stu-id="94a1e-108">Issuing these reports is a matter of creating an [IMessage : IMAPIProp](imessageimapiprop.md) object, filling out the relevant properties on the message, and submitting it to the MAPI spooler as if the message had originated with the user.</span></span> <span data-ttu-id="94a1e-109">Die [IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) -Methode kann für diese verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="94a1e-109">The [IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) method can be used for this.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="94a1e-110">Spezielle muss darauf geachtet werden bei ein Nachrichtenspeicher Kopien einer ungelesenen Nachricht mit ausstehenden gelesen oder nonread Berichte.</span><span class="sxs-lookup"><span data-stu-id="94a1e-110">Special care must be taken when a message store makes copies of an unread message with pending read or nonread reports.</span></span> <span data-ttu-id="94a1e-111">Diese Berichte sollten nicht generiert werden, wenn Benutzer alle Kopien einer Nachricht lesen für die Berichte angefordert wurden.</span><span class="sxs-lookup"><span data-stu-id="94a1e-111">Such reports should not be generated when users read any copies of a message for which reports have been requested.</span></span> <span data-ttu-id="94a1e-112">Wenn Sie eine Kopie einer solchen Nachricht zu erstellen, sollte der Nachricht Speicheranbieter die Flags CLEAR_RN_PENDING und CLEAR_NRN_PENDING in seiner Aufrufen von [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) und [IMessage::SetReadFlag](imessage-setreadflag.md)enthalten.</span><span class="sxs-lookup"><span data-stu-id="94a1e-112">When making a copy of such a message, the message store provider should include the CLEAR_RN_PENDING and CLEAR_NRN_PENDING flags in its calls to [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) and [IMessage::SetReadFlag](imessage-setreadflag.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="94a1e-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94a1e-113">See also</span></span>



[<span data-ttu-id="94a1e-114">Nachrichtenspeicher-Features</span><span class="sxs-lookup"><span data-stu-id="94a1e-114">Message Store Features</span></span>](message-store-features.md)
