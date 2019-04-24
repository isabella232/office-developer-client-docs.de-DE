---
title: Codieren von Empfänger Tabellen mithilfe von TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd2f595f-4dd0-4704-b670-6857d6c843ca
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1ed047424e4a6d64c08b511a15769c081a0d8c4e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339403"
---
# <a name="encoding-recipient-tables-by-using-tnef"></a><span data-ttu-id="82cf1-103">Codieren von Empfänger Tabellen mithilfe von TNEF</span><span class="sxs-lookup"><span data-stu-id="82cf1-103">Encoding Recipient Tables by Using TNEF</span></span>

  
  
<span data-ttu-id="82cf1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="82cf1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="82cf1-105">Die Codierung einer Empfängertabelle in den TNEF-Datenstrom ist selten erforderlich, da die meisten Messagingsysteme Empfängerlisten direkt unterstützen.</span><span class="sxs-lookup"><span data-stu-id="82cf1-105">The encoding of a recipient table into the TNEF stream is rarely necessary since most messaging systems support recipient lists directly.</span></span> <span data-ttu-id="82cf1-106">Im Allgemeinen werden die Empfänger Eigenschaften im Nachrichtenkopf übertragen.</span><span class="sxs-lookup"><span data-stu-id="82cf1-106">In general, the recipient properties are transmitted in the message header.</span></span> <span data-ttu-id="82cf1-107">Wenn die Empfängertabelle erforderlich ist, kann TNEF die Empfängertabelle als Teil ihrer üblichen Verarbeitung codieren.</span><span class="sxs-lookup"><span data-stu-id="82cf1-107">When inclusion of the recipient table is necessary, TNEF can encode the recipient table as a part of its usual processing.</span></span> <span data-ttu-id="82cf1-108">Dies erfolgt in der ersten Phase der TNEF-Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="82cf1-108">This is done during the initial phase of TNEF processing.</span></span> <span data-ttu-id="82cf1-109">Der Transportanbieter kann die Empfängertabelle der Nachricht einschließen, indem er die [ITnef::](itnef-addprops.md) AddProps-Methode mit der in der Aufnahmeliste angegebenen **PR_MESSAGE_RECIPIENTS** ([pidtagmessagerecipients (](pidtagmessagerecipients-canonical-property.md))-Eigenschaft aufruft.</span><span class="sxs-lookup"><span data-stu-id="82cf1-109">The transport provider can include the message's recipient table by calling the [ITnef::AddProps](itnef-addprops.md) method with the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property specified in the inclusion list.</span></span> <span data-ttu-id="82cf1-110">TNEF Ruft die Empfängertabelle aus der Nachricht ab, fragt den Spaltensatz ab und verarbeitet jede Zeile der Tabelle im TNEF-Stream.</span><span class="sxs-lookup"><span data-stu-id="82cf1-110">TNEF gets the recipient table from the message, queries the column set, and processes every row of the table into the TNEF stream.</span></span>
  
<span data-ttu-id="82cf1-111">Eine alternative Methode ist verfügbar, wenn der Transportanbieter die Empfängertabelle ändern muss, bevor Sie codiert wird.</span><span class="sxs-lookup"><span data-stu-id="82cf1-111">An alternate method is available if the transport provider needs to modify the recipient table before it is encoded.</span></span> <span data-ttu-id="82cf1-112">Der Transportanbieter kann die erforderliche Tabelle erstellen und dann die [ITnef:: EncodeRecips](itnef-encoderecips.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="82cf1-112">The transport provider can construct the necessary table and then call the [ITnef::EncodeRecips](itnef-encoderecips.md) method.</span></span> <span data-ttu-id="82cf1-113">Wenn NULL im _lpRecipTable_ -Parameter übergeben wird, wird die Empfängertabelle direkt aus der Nachricht übernommen, wie unter **ITnef::** AddProps beschrieben.</span><span class="sxs-lookup"><span data-stu-id="82cf1-113">If NULL is passed in the  _lpRecipTable_ parameter, then the recipient table is taken directly from the message as described for **ITnef::AddProps**.</span></span>
  

