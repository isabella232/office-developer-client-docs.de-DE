---
title: Zentralisieren des Empfangs von NDRs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: fbe1f4f6-28f8-40b8-b551-192c0ba48c18
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: af2531076755d1e183409f50fe1a0c97d28063f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405856"
---
# <a name="centralizing-the-receipt-of-ndrs"></a><span data-ttu-id="08779-103">Zentralisieren des Empfangs von NDRs</span><span class="sxs-lookup"><span data-stu-id="08779-103">Centralizing the receipt of NDRs</span></span>

<span data-ttu-id="08779-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08779-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08779-105">**So müssen Nicht-Löschberichte (Nondelivery Reports, NDRs) an einem zentralen Ort eintreffen, wenn mehrere Instanzen Ihres Clients gleichzeitig ausgeführt werden**</span><span class="sxs-lookup"><span data-stu-id="08779-105">**To have nondelivery reports (NDRs) arrive at a central location when multiple instances of your client are running simultaneously**</span></span>
  
1. <span data-ttu-id="08779-106">Legen **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)), **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) und **PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) auf die entsprechenden Werte für das Konto fest, das die Berichte empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="08779-106">Set **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)), **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)), and **PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) to the appropriate values for the account that is to receive the reports.</span></span> <span data-ttu-id="08779-107">Erstellen Sie die Eintrags-ID, indem Sie bei Bedarf [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="08779-107">Create the entry identifier by calling [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) if necessary.</span></span> 
    
2. <span data-ttu-id="08779-108">Verstehen Sie, dass es Messagingsysteme gibt, die das konto ignorieren, das Sie für Berichte angefordert haben, und diese an den Ermittler senden.</span><span class="sxs-lookup"><span data-stu-id="08779-108">Understand that there are messaging systems that will ignore the account you've requested for reports and send them to the originator.</span></span> <span data-ttu-id="08779-109">Verringern Sie die Auswirkungen, die dies auf Administratoren hat, die Berichte verschieben müssen, indem Sie:</span><span class="sxs-lookup"><span data-stu-id="08779-109">Reduce the impact that this will have on administrators that will need to move reports around by:</span></span>
    
- <span data-ttu-id="08779-110">Geben Sie Ihrer ursprünglichen Nachricht eine unterschiedliche Nachrichtenklasse, z. B. IPM. Note.MSNNews.</span><span class="sxs-lookup"><span data-stu-id="08779-110">Giving your original message a distinct message class, such as IPM.Note.MSNNews.</span></span> <span data-ttu-id="08779-111">Suchen Sie nach eingehenden Nachrichten mit der Klasse Report.IPM.Note.MSNNews.NDR, und weiterleiten Sie sie an das Konto, zu dem Berichte kommen sollen.</span><span class="sxs-lookup"><span data-stu-id="08779-111">Look for incoming messages with class Report.IPM.Note.MSNNews.NDR and forward them to the account you intended reports to come to.</span></span> <span data-ttu-id="08779-112">Senden Sie gleichzeitig E-Mails an das Messagingsystem, das Ihr Nicht-Löschbericht-Konto **ignoriert** hat, um zu kommunizieren, dass es die eigenschaft PR_REPORT_ENTRYID sollte.</span><span class="sxs-lookup"><span data-stu-id="08779-112">At the same time, send email to the messaging system that ignored your nondelivery report account to communicate that it should honor the **PR_REPORT_ENTRYID** property.</span></span> 
    
- <span data-ttu-id="08779-113">Die meisten Messagingsysteme, die keine **PR_REPORT_ENTRYID,** werden auch die Konventionen der MAPI-Nachrichtenklasse nicht einhalten.</span><span class="sxs-lookup"><span data-stu-id="08779-113">Most messaging systems which do not honor **PR_REPORT_ENTRYID** will not honor the MAPI message class conventions either.</span></span> <span data-ttu-id="08779-114">Daher erhalten Sie etwas, das wie eine Notiz aussieht.</span><span class="sxs-lookup"><span data-stu-id="08779-114">Therefore, you'll receive something that looks like a note.</span></span> <span data-ttu-id="08779-115">Dies ist etwas schwieriger zu umgehen, da die Eingabe so variabel ist.</span><span class="sxs-lookup"><span data-stu-id="08779-115">This is a little harder to deal with because the input is so variable.</span></span> <span data-ttu-id="08779-116">Sehen Sie sich den Betreff an, und geben Sie ihn weiter, wenn Sie entweder etwas aus einer Liste von Wörtern finden, die "nicht zustellbar" oder etwas von Ihrem ursprünglichen Betreff bedeuten.</span><span class="sxs-lookup"><span data-stu-id="08779-116">Look at the subject and forward it if you find either something from a list of words that mean "undeliverable" or something from your original subject.</span></span> <span data-ttu-id="08779-117">Bereiten Sie sich darauf vor, diese Listen im Laufe der Zeit zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="08779-117">Be prepared to tune these lists over time.</span></span> 
    

