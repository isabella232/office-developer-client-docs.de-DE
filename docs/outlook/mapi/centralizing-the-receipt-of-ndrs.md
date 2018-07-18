---
title: Zentral verwalten den Empfang von Unzustellbarkeitsberichten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: fbe1f4f6-28f8-40b8-b551-192c0ba48c18
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0af587bd07de9445f143be316798059eaef402e0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791405"
---
# <a name="centralizing-the-receipt-of-ndrs"></a><span data-ttu-id="e6f25-103">Zentral verwalten den Empfang von Unzustellbarkeitsberichten</span><span class="sxs-lookup"><span data-stu-id="e6f25-103">Centralizing the receipt of NDRs</span></span>

<span data-ttu-id="e6f25-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e6f25-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e6f25-105">**Eintreffen damit Unzustellbarkeitsberichten (NDR) an einem zentralen Speicherort, wenn mehrere Instanzen Ihres Clients gleichzeitig ausgeführt werden**</span><span class="sxs-lookup"><span data-stu-id="e6f25-105">**To have nondelivery reports (NDRs) arrive at a central location when multiple instances of your client are running simultaneously**</span></span>
  
1. <span data-ttu-id="e6f25-106">Legen Sie die entsprechenden Werte für das Konto, das erhalten **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)), **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) und **PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) die Berichte.</span><span class="sxs-lookup"><span data-stu-id="e6f25-106">Set **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)), **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)), and **PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) to the appropriate values for the account that is to receive the reports.</span></span> <span data-ttu-id="e6f25-107">Erstellen Sie die Eintrags-ID durch Aufrufen von [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) bei Bedarf.</span><span class="sxs-lookup"><span data-stu-id="e6f25-107">Create the entry identifier by calling [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) if necessary.</span></span> 
    
2. <span data-ttu-id="e6f25-108">Erkennen Sie, dass die messaging-Systemen, die das Konto für Berichte angefordert haben und diese an den Absender senden ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="e6f25-108">Understand that there are messaging systems that will ignore the account you've requested for reports and send them to the originator.</span></span> <span data-ttu-id="e6f25-109">Reduzieren Sie die Auswirkungen mit dies auf Administratoren, die Berichte durch bewegen müssen:</span><span class="sxs-lookup"><span data-stu-id="e6f25-109">Reduce the impact that this will have on administrators that will need to move reports around by:</span></span>
    
- <span data-ttu-id="e6f25-110">Wenn Sie für Ihre ursprünglichen Nachricht eine unterschiedliche Nachrichtenklasse wie IPM. Note.MSNNews.</span><span class="sxs-lookup"><span data-stu-id="e6f25-110">Giving your original message a distinct message class, such as IPM.Note.MSNNews.</span></span> <span data-ttu-id="e6f25-111">Suchen Sie nach eingehende Nachrichten mit Report.IPM.Note.MSNNews.NDR-Klasse und Notizen an dasselbe Konto wie gewünscht Berichte zu betrachten.</span><span class="sxs-lookup"><span data-stu-id="e6f25-111">Look for incoming messages with class Report.IPM.Note.MSNNews.NDR and forward them to the account you intended reports to come to.</span></span> <span data-ttu-id="e6f25-112">Gleichzeitig senden Sie e-Mail an die messaging-System, das ignoriert Ihr Konto Nondelivery Bericht, um anzuzeigen, ob es die **PR_REPORT_ENTRYID** -Eigenschaft berücksichtigt werden sollten.</span><span class="sxs-lookup"><span data-stu-id="e6f25-112">At the same time, send email to the messaging system that ignored your nondelivery report account to communicate that it should honor the **PR_REPORT_ENTRYID** property.</span></span> 
    
- <span data-ttu-id="e6f25-113">Die meisten Messagingsysteme, die berücksichtigt **PR_REPORT_ENTRYID** nicht berücksichtigt die MAPI-Nachricht Klasse Konventionen nicht entweder.</span><span class="sxs-lookup"><span data-stu-id="e6f25-113">Most messaging systems which do not honor **PR_REPORT_ENTRYID** will not honor the MAPI message class conventions either.</span></span> <span data-ttu-id="e6f25-114">Aus diesem Grund erhalten etwas Sie, die eine Notiz aussieht.</span><span class="sxs-lookup"><span data-stu-id="e6f25-114">Therefore, you'll receive something that looks like a note.</span></span> <span data-ttu-id="e6f25-115">Dies ist etwas schwieriger zu bewältigen, da die Eingabe also Variable ist.</span><span class="sxs-lookup"><span data-stu-id="e6f25-115">This is a little harder to deal with because the input is so variable.</span></span> <span data-ttu-id="e6f25-116">Sehen Sie sich den Betreff und Weiterleiten Sie, wenn Sie entweder etwas aus einer Liste von Wörtern, Mittelwert "unzustellbar" oder etwas aus Ihrer ursprünglichen Betreff finden.</span><span class="sxs-lookup"><span data-stu-id="e6f25-116">Look at the subject and forward it if you find either something from a list of words that mean "undeliverable" or something from your original subject.</span></span> <span data-ttu-id="e6f25-117">Seien Sie diese Listen über einen Zeitraum zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="e6f25-117">Be prepared to tune these lists over time.</span></span> 
    

