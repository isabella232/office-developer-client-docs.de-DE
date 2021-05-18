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
ms.openlocfilehash: ca9e5138d3ded13dfe33037f75e43ef1098f3c2d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412534"
---
# <a name="mapi-view-folders"></a><span data-ttu-id="bbef6-103">MAPI-Anzeigen von Ordnern</span><span class="sxs-lookup"><span data-stu-id="bbef6-103">MAPI View Folders</span></span>

  
  
<span data-ttu-id="bbef6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bbef6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bbef6-p101">Anzeigen von Ordnern sind Stammordner, die zugeh�rigen Informationen zum Definieren der alternative Anzeigelayouts f�r den Inhalt von Nachrichtenordnern zwischen Personen (IPM) enthalten. Anzeigen von Ordnern befinden sich unter dem Stammverzeichnis f�r den Nachrichtenspeicher und werden daher nicht in der Clientanwendung typische angezeigt. Nicht bei jedem Nachrichtenspeicher umfasst Ordner anzeigen. nur Nachrichtenspeicher, die f�r die Verwendung als Standard-Informationsspeicher f�r die Sitzung konfiguriert sind, m�ssen diese enthalten.</span><span class="sxs-lookup"><span data-stu-id="bbef6-p101">View folders are root folders that contain associated information to define alternative display layouts for the contents of interpersonal message (IPM) folders. View folders reside under the root for the message store and, therefore, are not visible in the typical client application. Not every message store includes view folders; only message stores that are configured to work as the default message store for the session must include them.</span></span>  
  
<span data-ttu-id="bbef6-108">MAPI unterst�tzt zwei Anzeigen von Ordnern:</span><span class="sxs-lookup"><span data-stu-id="bbef6-108">MAPI supports two view folders:</span></span>
  
- <span data-ttu-id="bbef6-109">Allgemeine � Der allgemeine Ansichtordner enth�lt Ansichten, die f�r den Nachrichtenspeicher standard und k�nnen von jedem Benutzer einen Client, der den Nachrichtenspeicher greift auf verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bbef6-109">Common — The common view folder contains views that are standard for the message store and can be used by any user of a client that accesses the message store.</span></span> <span data-ttu-id="bbef6-110">Der Eintragsbezeichner für den Ordner "Allgemeine Ansicht" wird in der **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)) -Eigenschaft des Speichers gespeichert.</span><span class="sxs-lookup"><span data-stu-id="bbef6-110">The entry identifier for the common view folder is stored in the store's **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="bbef6-111">Privat � Der pers�nlichen Ansichtordner enth�lt Ansichten, die von einem bestimmten Benutzer definiert sind.</span><span class="sxs-lookup"><span data-stu-id="bbef6-111">Personal — The personal view folder contains views that are defined by a particular user.</span></span> <span data-ttu-id="bbef6-112">MAPI definiert die **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)) -Eigenschaft zum Speichern der Eintrags-ID des persönlichen Ansichtsordners.</span><span class="sxs-lookup"><span data-stu-id="bbef6-112">MAPI defines the **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)) property for holding the entry identifier of the personal view folder.</span></span> <span data-ttu-id="bbef6-113">Verwendung von pers�nlichen Ansichten, k�nnte ein Benutzer beispielsweise an eine Gruppe von Nachrichten sortiert nach Absender, nur Datum der Nachricht Betreff und des Empfangs auflisten aussehen; ein anderer Benutzer kann die gleiche Gruppe sortiert nach Datum, Betreff, Absender und Nachrichtengr��e auflisten betrachten.</span><span class="sxs-lookup"><span data-stu-id="bbef6-113">Using personal views, for example, one user could look at a group of messages sorted by sender, listing only the message subject and receipt date; another user could look at the same group sorted by date, listing the subject, sender, and message size.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bbef6-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bbef6-114">See also</span></span>



[<span data-ttu-id="bbef6-115">MAPI-Ordner</span><span class="sxs-lookup"><span data-stu-id="bbef6-115">MAPI Folders</span></span>](mapi-folders.md)

