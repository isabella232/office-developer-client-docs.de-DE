---
title: Codieren von Empfängertabellen mit TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd2f595f-4dd0-4704-b670-6857d6c843ca
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: aa2120b5d64eece76f8882489de4388b04afa053
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591345"
---
# <a name="encoding-recipient-tables-by-using-tnef"></a><span data-ttu-id="76220-103">Codieren von Empfängertabellen mit TNEF</span><span class="sxs-lookup"><span data-stu-id="76220-103">Encoding Recipient Tables by Using TNEF</span></span>

  
  
<span data-ttu-id="76220-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="76220-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="76220-105">Die Codierung einer Tabelle Empfänger in der TNEF-Stream-Objekt ist nur selten erforderlich, da die meisten Messagingsysteme Empfängerlisten direkt unterstützen.</span><span class="sxs-lookup"><span data-stu-id="76220-105">The encoding of a recipient table into the TNEF stream is rarely necessary since most messaging systems support recipient lists directly.</span></span> <span data-ttu-id="76220-106">Im Allgemeinen werden in der Kopfzeile der Nachricht die Empfängereigenschaften übertragen.</span><span class="sxs-lookup"><span data-stu-id="76220-106">In general, the recipient properties are transmitted in the message header.</span></span> <span data-ttu-id="76220-107">Wenn die Aufnahme der Empfänger Tabelle erforderlich ist, kann TNEF die Empfänger Tabelle als Teil der normalen Verarbeitung codieren.</span><span class="sxs-lookup"><span data-stu-id="76220-107">When inclusion of the recipient table is necessary, TNEF can encode the recipient table as a part of its usual processing.</span></span> <span data-ttu-id="76220-108">Dies erfolgt während der Anfangsphase der TNEF-Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="76220-108">This is done during the initial phase of TNEF processing.</span></span> <span data-ttu-id="76220-109">Der Adressbuchhierarchie kann durch Aufrufen der [ITnef::AddProps](itnef-addprops.md) -Methode mit der **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))-Eigenschaft, die in der Aufnahmeliste angegebenen Empfänger die Nachricht-Tabelle enthalten.</span><span class="sxs-lookup"><span data-stu-id="76220-109">The transport provider can include the message's recipient table by calling the [ITnef::AddProps](itnef-addprops.md) method with the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property specified in the inclusion list.</span></span> <span data-ttu-id="76220-110">TNEF Ruft die Empfänger Tabelle aus der Nachricht ab, fragt die Spalte festlegen und jede Zeile der Tabelle in die TNEF-Stream verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="76220-110">TNEF gets the recipient table from the message, queries the column set, and processes every row of the table into the TNEF stream.</span></span>
  
<span data-ttu-id="76220-111">Eine alternative Methode ist verfügbar, wenn der Adressbuchhierarchie muss die Empfänger Tabelle zu ändern, bevor er codiert wird.</span><span class="sxs-lookup"><span data-stu-id="76220-111">An alternate method is available if the transport provider needs to modify the recipient table before it is encoded.</span></span> <span data-ttu-id="76220-112">Der Adressbuchhierarchie kann die notwendige Tabelle erstellen und dann die [ITnef::EncodeRecips](itnef-encoderecips.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="76220-112">The transport provider can construct the necessary table and then call the [ITnef::EncodeRecips](itnef-encoderecips.md) method.</span></span> <span data-ttu-id="76220-113">Wenn NULL in der _LpRecipTable_ -Parameter übergeben wird, wird die Empfänger Tabelle direkt aus der Nachricht übernommen, wie für **ITnef::AddProps**beschrieben.</span><span class="sxs-lookup"><span data-stu-id="76220-113">If NULL is passed in the  _lpRecipTable_ parameter, then the recipient table is taken directly from the message as described for **ITnef::AddProps**.</span></span>
  

