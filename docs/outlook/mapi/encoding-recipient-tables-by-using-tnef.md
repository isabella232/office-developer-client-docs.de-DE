---
title: Empfänger Tabellen mithilfe von TNEF-Codierung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd2f595f-4dd0-4704-b670-6857d6c843ca
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8110eff9b38c76023621f34396d65714a4316d91
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791637"
---
# <a name="encoding-recipient-tables-by-using-tnef"></a><span data-ttu-id="d16d5-103">Empfänger Tabellen mithilfe von TNEF-Codierung</span><span class="sxs-lookup"><span data-stu-id="d16d5-103">Encoding Recipient Tables by Using TNEF</span></span>

  
  
<span data-ttu-id="d16d5-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d16d5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d16d5-105">Die Codierung einer Tabelle Empfänger in der TNEF-Stream-Objekt ist nur selten erforderlich, da die meisten Messagingsysteme Empfängerlisten direkt unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d16d5-105">The encoding of a recipient table into the TNEF stream is rarely necessary since most messaging systems support recipient lists directly.</span></span> <span data-ttu-id="d16d5-106">Im Allgemeinen werden in der Kopfzeile der Nachricht die Empfängereigenschaften übertragen.</span><span class="sxs-lookup"><span data-stu-id="d16d5-106">In general, the recipient properties are transmitted in the message header.</span></span> <span data-ttu-id="d16d5-107">Wenn die Aufnahme der Empfänger Tabelle erforderlich ist, kann TNEF die Empfänger Tabelle als Teil der normalen Verarbeitung codieren.</span><span class="sxs-lookup"><span data-stu-id="d16d5-107">When inclusion of the recipient table is necessary, TNEF can encode the recipient table as a part of its usual processing.</span></span> <span data-ttu-id="d16d5-108">Dies erfolgt während der Anfangsphase der TNEF-Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="d16d5-108">This is done during the initial phase of TNEF processing.</span></span> <span data-ttu-id="d16d5-109">Der Adressbuchhierarchie kann durch Aufrufen der [ITnef::AddProps](itnef-addprops.md) -Methode mit der **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))-Eigenschaft, die in der Aufnahmeliste angegebenen Empfänger die Nachricht-Tabelle enthalten.</span><span class="sxs-lookup"><span data-stu-id="d16d5-109">The transport provider can include the message's recipient table by calling the [ITnef::AddProps](itnef-addprops.md) method with the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property specified in the inclusion list.</span></span> <span data-ttu-id="d16d5-110">TNEF Ruft die Empfänger Tabelle aus der Nachricht ab, fragt die Spalte festlegen und jede Zeile der Tabelle in die TNEF-Stream verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="d16d5-110">TNEF gets the recipient table from the message, queries the column set, and processes every row of the table into the TNEF stream.</span></span>
  
<span data-ttu-id="d16d5-111">Eine alternative Methode ist verfügbar, wenn der Adressbuchhierarchie muss die Empfänger Tabelle zu ändern, bevor er codiert wird.</span><span class="sxs-lookup"><span data-stu-id="d16d5-111">An alternate method is available if the transport provider needs to modify the recipient table before it is encoded.</span></span> <span data-ttu-id="d16d5-112">Der Adressbuchhierarchie kann die notwendige Tabelle erstellen und dann die [ITnef::EncodeRecips](itnef-encoderecips.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d16d5-112">The transport provider can construct the necessary table and then call the [ITnef::EncodeRecips](itnef-encoderecips.md) method.</span></span> <span data-ttu-id="d16d5-113">Wenn NULL in der _LpRecipTable_ -Parameter übergeben wird, wird die Empfänger Tabelle direkt aus der Nachricht übernommen, wie für **ITnef::AddProps**beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d16d5-113">If NULL is passed in the  _lpRecipTable_ parameter, then the recipient table is taken directly from the message as described for **ITnef::AddProps**.</span></span>
  
