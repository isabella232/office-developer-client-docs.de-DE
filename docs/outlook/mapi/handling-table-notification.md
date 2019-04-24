---
title: Behandeln von Tabellenbenachrichtigungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: edc9bc71-4885-4783-b465-0bafa20eff73
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6e6c24c3836f295054c1880dc506c5051078a9ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299489"
---
# <a name="handling-table-notification"></a><span data-ttu-id="709fe-103">Behandeln von Tabellenbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="709fe-103">Handling table notification</span></span>

<span data-ttu-id="709fe-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="709fe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="709fe-105">Als Alternative zur direkten Registrierung bei einem Advise-Quellobjekt wie einem Ordner oder einem Messagingbenutzer kann ein Client sich für Benachrichtigungen in einer Inhalts-oder Hierarchietabelle registrieren.</span><span class="sxs-lookup"><span data-stu-id="709fe-105">As an alternative to registering directly with an advise source object, such as a folder or a messaging user, a client can register for notifications on a contents or hierarchy table.</span></span> <span data-ttu-id="709fe-106">Das Nachverfolgen von Änderungen an Adressbucheinträgen, Ordnern und Nachrichten über eine Inhalts-oder Hierarchietabelle kann einfacher und geradliniger sein als durch einzelne Objekte.</span><span class="sxs-lookup"><span data-stu-id="709fe-106">Tracking changes to address book entries, folders, and messages through a contents or hierarchy table can be simpler and more straightforward than through individual objects.</span></span> 

<span data-ttu-id="709fe-107">Sie können beispielsweise [IMAPITable:: Advise](imapitable-advise.md) für die Hierarchietabelle eines Ordners aufrufen, um zu ermitteln, wann Änderungen an einem der Unterordner vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="709fe-107">For example, you can call [IMAPITable::Advise](imapitable-advise.md) on a folder's hierarchy table to discover when changes occur to one of its subfolders.</span></span> <span data-ttu-id="709fe-108">Wenn Sie die Anzeige von Remotenachrichten unterstützen, registrieren Sie sich in der Statustabelle, um die Aktivitäten von Transportanbietern und dem MAPI-Spooler zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="709fe-108">If you support the viewing of remote messages, register with the status table to observe activity by transport providers and the MAPI spooler.</span></span> 
  
<span data-ttu-id="709fe-109">Es ist jedoch nicht immer vorzuziehen, Tabellen Benachrichtigungen anstelle von Objekt Benachrichtigungen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="709fe-109">However, it is not always preferable to use table notifications instead of object notifications.</span></span> <span data-ttu-id="709fe-110">Das überWachen von Änderungen an der Anzahl von Nachrichten in einem Ordner ist ein Beispiel dafür, wann Ihr Client sich möglicherweise für Objekt Benachrichtigungen in einem Ordner anstatt in einer vom Ordner implementierten Tabelle registrieren muss.</span><span class="sxs-lookup"><span data-stu-id="709fe-110">Monitoring changes in the number of messages in a folder is an example of when your client might need to register for object notifications on a folder rather than on a table implemented by the folder.</span></span>
  

