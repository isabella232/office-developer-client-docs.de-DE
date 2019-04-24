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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332662"
---
# <a name="centralizing-the-receipt-of-ndrs"></a><span data-ttu-id="f2116-103">Zentralisieren des Empfangs von NDRs</span><span class="sxs-lookup"><span data-stu-id="f2116-103">Centralizing the receipt of NDRs</span></span>

<span data-ttu-id="f2116-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f2116-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f2116-105">**Wenn mehrere Instanzen des Clients gleichzeitig ausgeführt werden, werden Unzustellbarkeitsberichte an einem zentralen Ort eingetroffen.**</span><span class="sxs-lookup"><span data-stu-id="f2116-105">**To have nondelivery reports (NDRs) arrive at a central location when multiple instances of your client are running simultaneously**</span></span>
  
1. <span data-ttu-id="f2116-106">Legen Sie **PR_REPORT_ENTRYID** ([Pidtagreportentryid (](pidtagreportentryid-canonical-property.md)) **, PR_REPORT_NAME** ([pidtagreportname (](pidtagreportname-canonical-property.md)) und **PR_REPORT_SEARCH_KEY** ([pidtagreportsearchkey (](pidtagreportsearchkey-canonical-property.md)) auf die entsprechenden Werte für das zu empfangende Konto fest. die Berichte.</span><span class="sxs-lookup"><span data-stu-id="f2116-106">Set **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)), **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)), and **PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) to the appropriate values for the account that is to receive the reports.</span></span> <span data-ttu-id="f2116-107">Erstellen Sie die Eintrags-ID, indem Sie [IAddrBook:: CreateOneOff](iaddrbook-createoneoff.md) aufrufen, falls erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f2116-107">Create the entry identifier by calling [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) if necessary.</span></span> 
    
2. <span data-ttu-id="f2116-108">Beachten Sie, dass es Messagingsysteme gibt, die das Konto, das Sie für Berichte angefordert haben, ignorieren und an den Absender senden.</span><span class="sxs-lookup"><span data-stu-id="f2116-108">Understand that there are messaging systems that will ignore the account you've requested for reports and send them to the originator.</span></span> <span data-ttu-id="f2116-109">Reduzieren Sie die Auswirkungen auf Administratoren, die Berichte verschieben müssen:</span><span class="sxs-lookup"><span data-stu-id="f2116-109">Reduce the impact that this will have on administrators that will need to move reports around by:</span></span>
    
- <span data-ttu-id="f2116-110">Geben Sie Ihrer ursprünglichen Nachricht eine unterschiedliche Nachrichtenklasse wie IPM. Hinweis. MSNNews.</span><span class="sxs-lookup"><span data-stu-id="f2116-110">Giving your original message a distinct message class, such as IPM.Note.MSNNews.</span></span> <span data-ttu-id="f2116-111">Suchen Sie nach eingehenden Nachrichten mit der Klasse Report. IPM. Note. MSNNews. NDR, und leiten Sie Sie an das Konto weiter, zu dem Sie Berichte erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="f2116-111">Look for incoming messages with class Report.IPM.Note.MSNNews.NDR and forward them to the account you intended reports to come to.</span></span> <span data-ttu-id="f2116-112">Senden Sie gleichzeitig eine e-Mail an das Messagingsystem, das Ihr Unzustellbarkeitsbericht Konto ignoriert hat, um zu kommunizieren, dass die **PR_REPORT_ENTRYID** -Eigenschaft berücksichtigt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="f2116-112">At the same time, send email to the messaging system that ignored your nondelivery report account to communicate that it should honor the **PR_REPORT_ENTRYID** property.</span></span> 
    
- <span data-ttu-id="f2116-113">Die meisten Messagingsysteme, die **PR_REPORT_ENTRYID** nicht honorieren, werden die MAPI-Nachrichtenklassen Konventionen nicht berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="f2116-113">Most messaging systems which do not honor **PR_REPORT_ENTRYID** will not honor the MAPI message class conventions either.</span></span> <span data-ttu-id="f2116-114">Daher erhalten Sie etwas, das wie eine Notiz aussieht.</span><span class="sxs-lookup"><span data-stu-id="f2116-114">Therefore, you'll receive something that looks like a note.</span></span> <span data-ttu-id="f2116-115">Dies ist ein wenig schwieriger zu bewältigen, da die Eingabe so variabel ist.</span><span class="sxs-lookup"><span data-stu-id="f2116-115">This is a little harder to deal with because the input is so variable.</span></span> <span data-ttu-id="f2116-116">Sehen Sie sich das Thema an, und leiten Sie es weiter, wenn Sie entweder etwas aus einer Liste von Wörtern finden, die "unzustellbar" oder etwas aus Ihrem ursprünglichen Betreff bedeuten.</span><span class="sxs-lookup"><span data-stu-id="f2116-116">Look at the subject and forward it if you find either something from a list of words that mean "undeliverable" or something from your original subject.</span></span> <span data-ttu-id="f2116-117">Sie sollten diese Listen im Laufe der Zeit optimieren.</span><span class="sxs-lookup"><span data-stu-id="f2116-117">Be prepared to tune these lists over time.</span></span> 
    

