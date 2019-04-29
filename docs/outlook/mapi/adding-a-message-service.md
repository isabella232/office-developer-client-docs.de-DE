---
title: Hinzufügen eines Nachrichtendiensts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1e626714-52dc-4141-9741-4d801f32d294
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 30cbe49eae7b4a232efb544c7a508a36b326c6b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407235"
---
# <a name="adding-a-message-service"></a><span data-ttu-id="e5ee1-103">Hinzufügen eines Nachrichtendiensts</span><span class="sxs-lookup"><span data-stu-id="e5ee1-103">Adding a Message Service</span></span>

  
  
<span data-ttu-id="e5ee1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e5ee1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="e5ee1-105">**So fügen Sie einem Profil einen neuen Nachrichtendienst hinzu und greifen auf den neuen Nachrichtendienst zu**</span><span class="sxs-lookup"><span data-stu-id="e5ee1-105">**To add a new message service to a profile and access the new message service**</span></span>
  
<span data-ttu-id="e5ee1-106">Rufen Sie [IMsgServiceAdmin2:: CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md)auf.</span><span class="sxs-lookup"><span data-stu-id="e5ee1-106">Call [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md).</span></span> <span data-ttu-id="e5ee1-107">**CreateMsgServiceEx** führt die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="e5ee1-107">**CreateMsgServiceEx** performs the following tasks:</span></span> 
  
1. <span data-ttu-id="e5ee1-108">Kopiert alle relevanten Informationen für den Nachrichtendienst, der sich in der MAPISVC befindet. INF-Datei, Erstellen eines Profil Abschnitts für jeden Anbieterabschnitt.</span><span class="sxs-lookup"><span data-stu-id="e5ee1-108">Copies all of the relevant information for the message service that is in the MAPISVC.INF file, creating a profile section for every provider section.</span></span>
    
2. <span data-ttu-id="e5ee1-109">Ruft die Einstiegspunktfunktion des Nachrichtendiensts **MSGSERVICEENTRY**auf, wobei der Parameter _ulContext_ auf MSG_SERVICE_CREATE festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e5ee1-109">Calls the message service's entry point function, **MSGSERVICEENTRY**, with the  _ulContext_ parameter set to MSG_SERVICE_CREATE.</span></span> 
    
3. <span data-ttu-id="e5ee1-110">Legt die **PR_SERVICE_UID** ([pidtagserviceuid (](pidtagserviceuid-canonical-property.md))-Eigenschaft des Nachrichtendiensts fest und ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="e5ee1-110">Sets and retrieves the message service's **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="e5ee1-111">**So greifen Sie auf einen neu hinzugefügten Nachrichtendienst zu**</span><span class="sxs-lookup"><span data-stu-id="e5ee1-111">**To access any newly added message service**</span></span>
  
1. <span data-ttu-id="e5ee1-112">Rufen Sie [IMsgServiceAdmin:: GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) auf, um die Nachrichtendienst Tabelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e5ee1-112">Call [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) to retrieve the message service table.</span></span> 
    
2. <span data-ttu-id="e5ee1-113">Rufen Sie die [IMAPITable:: Advise](imapitable-advise.md) -Methode der Nachrichtendienst Tabelle auf, um Tabellen Benachrichtigungen zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="e5ee1-113">Call the message service table's [IMAPITable::Advise](imapitable-advise.md) method to register for table notifications.</span></span> 
    
3. <span data-ttu-id="e5ee1-114">Wenn MAPI eine TABLE_ROW_ADDED-Benachrichtigung sendet, suchen Sie den Eintragsbezeichner des neu hinzugefügten Nachrichtendiensts in der [SRow](srow.md) -Struktur, die in der [TABLE_NOTIFICATION](table_notification.md) -Struktur enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="e5ee1-114">When MAPI sends a TABLE_ROW_ADDED notification, locate the entry identifier of the newly added message service in the [SRow](srow.md) structure included in the [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> 
    

