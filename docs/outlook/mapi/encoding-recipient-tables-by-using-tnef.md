---
title: Codieren von Empfängertabellen mithilfe von TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd2f595f-4dd0-4704-b670-6857d6c843ca
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1ed047424e4a6d64c08b511a15769c081a0d8c4e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417959"
---
# <a name="encoding-recipient-tables-by-using-tnef"></a><span data-ttu-id="33017-103">Codieren von Empfängertabellen mithilfe von TNEF</span><span class="sxs-lookup"><span data-stu-id="33017-103">Encoding Recipient Tables by Using TNEF</span></span>

  
  
<span data-ttu-id="33017-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="33017-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="33017-105">Die Codierung einer Empfängertabelle in den TNEF-Stream ist selten erforderlich, da die meisten Messagingsysteme Empfängerlisten direkt unterstützen.</span><span class="sxs-lookup"><span data-stu-id="33017-105">The encoding of a recipient table into the TNEF stream is rarely necessary since most messaging systems support recipient lists directly.</span></span> <span data-ttu-id="33017-106">Im Allgemeinen werden die Empfängereigenschaften im Nachrichtenkopf übertragen.</span><span class="sxs-lookup"><span data-stu-id="33017-106">In general, the recipient properties are transmitted in the message header.</span></span> <span data-ttu-id="33017-107">Wenn die Aufnahme der Empfängertabelle erforderlich ist, kann TNEF die Empfängertabelle als Teil der üblichen Verarbeitung codieren.</span><span class="sxs-lookup"><span data-stu-id="33017-107">When inclusion of the recipient table is necessary, TNEF can encode the recipient table as a part of its usual processing.</span></span> <span data-ttu-id="33017-108">Dies erfolgt während der ersten Phase der TNEF-Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="33017-108">This is done during the initial phase of TNEF processing.</span></span> <span data-ttu-id="33017-109">Der Transportanbieter kann die Empfängertabelle der Nachricht enthalten, indem die [ITnef::AddProps-Methode](itnef-addprops.md) mit der in der Inklusionsliste angegebenen **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) -Eigenschaft aufruft.</span><span class="sxs-lookup"><span data-stu-id="33017-109">The transport provider can include the message's recipient table by calling the [ITnef::AddProps](itnef-addprops.md) method with the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property specified in the inclusion list.</span></span> <span data-ttu-id="33017-110">TNEF ruft die Empfängertabelle aus der Nachricht ab, fragt den Spaltensatz ab und verarbeitet jede Zeile der Tabelle in den TNEF-Stream.</span><span class="sxs-lookup"><span data-stu-id="33017-110">TNEF gets the recipient table from the message, queries the column set, and processes every row of the table into the TNEF stream.</span></span>
  
<span data-ttu-id="33017-111">Eine alternative Methode ist verfügbar, wenn der Transportanbieter die Empfängertabelle ändern muss, bevor sie codiert wird.</span><span class="sxs-lookup"><span data-stu-id="33017-111">An alternate method is available if the transport provider needs to modify the recipient table before it is encoded.</span></span> <span data-ttu-id="33017-112">Der Transportanbieter kann die erforderliche Tabelle erstellen und dann die [ITnef::EncodeRecips-Methode](itnef-encoderecips.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="33017-112">The transport provider can construct the necessary table and then call the [ITnef::EncodeRecips](itnef-encoderecips.md) method.</span></span> <span data-ttu-id="33017-113">Wenn NULL im  _lpRecipTable-Parameter_ übergeben wird, wird die Empfängertabelle wie für **ITnef::AddProps** beschrieben direkt aus der Nachricht übernommen.</span><span class="sxs-lookup"><span data-stu-id="33017-113">If NULL is passed in the  _lpRecipTable_ parameter, then the recipient table is taken directly from the message as described for **ITnef::AddProps**.</span></span>
  

