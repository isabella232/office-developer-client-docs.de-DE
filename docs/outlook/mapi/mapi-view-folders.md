---
title: MAPI-Anzeigen von Ordnern
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a1936ec2-bf8a-4242-a41d-64d26b813bd0
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: cb26771e9968175ab67366e35cf019ce23d51b8d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793106"
---
# <a name="mapi-view-folders"></a><span data-ttu-id="2fa4f-103">MAPI-Anzeigen von Ordnern</span><span class="sxs-lookup"><span data-stu-id="2fa4f-103">MAPI View Folders</span></span>

  
  
<span data-ttu-id="2fa4f-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2fa4f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2fa4f-p101">Anzeigen von Ordnern sind Stammordner, die zugeh�rigen Informationen zum Definieren der alternative Anzeigelayouts f�r den Inhalt von Nachrichtenordnern zwischen Personen (IPM) enthalten. Anzeigen von Ordnern befinden sich unter dem Stammverzeichnis f�r den Nachrichtenspeicher und werden daher nicht in der Clientanwendung typische angezeigt. Nicht bei jedem Nachrichtenspeicher umfasst Ordner anzeigen. nur Nachrichtenspeicher, die f�r die Verwendung als Standard-Informationsspeicher f�r die Sitzung konfiguriert sind, m�ssen diese enthalten.</span><span class="sxs-lookup"><span data-stu-id="2fa4f-p101">View folders are root folders that contain associated information to define alternative display layouts for the contents of interpersonal message (IPM) folders. View folders reside under the root for the message store and, therefore, are not visible in the typical client application. Not every message store includes view folders; only message stores that are configured to work as the default message store for the session must include them.</span></span>  
  
<span data-ttu-id="2fa4f-108">MAPI unterst�tzt zwei Anzeigen von Ordnern:</span><span class="sxs-lookup"><span data-stu-id="2fa4f-108">MAPI supports two view folders:</span></span>
  
- <span data-ttu-id="2fa4f-109">Allgemeine � Der allgemeine Ansichtordner enth�lt Ansichten, die f�r den Nachrichtenspeicher standard und k�nnen von jedem Benutzer einen Client, der den Nachrichtenspeicher greift auf verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2fa4f-109">Common — The common view folder contains views that are standard for the message store and can be used by any user of a client that accesses the message store.</span></span> <span data-ttu-id="2fa4f-110">Die Eintrags-ID für den gemeinsamen Ansichtordner wird in den Speicher **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))-Eigenschaft gespeichert.</span><span class="sxs-lookup"><span data-stu-id="2fa4f-110">The entry identifier for the common view folder is stored in the store's **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="2fa4f-111">Privat � Der pers�nlichen Ansichtordner enth�lt Ansichten, die von einem bestimmten Benutzer definiert sind.</span><span class="sxs-lookup"><span data-stu-id="2fa4f-111">Personal — The personal view folder contains views that are defined by a particular user.</span></span> <span data-ttu-id="2fa4f-112">MAPI definiert die **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))-Eigenschaft die Eintrags-ID des Ordners persönliche Ansicht aufgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="2fa4f-112">MAPI defines the **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)) property for holding the entry identifier of the personal view folder.</span></span> <span data-ttu-id="2fa4f-113">Verwendung von pers�nlichen Ansichten, k�nnte ein Benutzer beispielsweise an eine Gruppe von Nachrichten sortiert nach Absender, nur Datum der Nachricht Betreff und des Empfangs auflisten aussehen; ein anderer Benutzer kann die gleiche Gruppe sortiert nach Datum, Betreff, Absender und Nachrichtengr��e auflisten betrachten.</span><span class="sxs-lookup"><span data-stu-id="2fa4f-113">Using personal views, for example, one user could look at a group of messages sorted by sender, listing only the message subject and receipt date; another user could look at the same group sorted by date, listing the subject, sender, and message size.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2fa4f-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2fa4f-114">See also</span></span>



[<span data-ttu-id="2fa4f-115">MAPI-Ordner</span><span class="sxs-lookup"><span data-stu-id="2fa4f-115">MAPI Folders</span></span>](mapi-folders.md)

