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
# <a name="adding-a-message-service"></a><span data-ttu-id="0401f-103">Hinzufügen eines Nachrichtendiensts</span><span class="sxs-lookup"><span data-stu-id="0401f-103">Adding a Message Service</span></span>

  
  
<span data-ttu-id="0401f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0401f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="0401f-105">**So fügen Sie einem Profil einen neuen Nachrichtendienst hinzu und greifen auf den neuen Nachrichtendienst zu**</span><span class="sxs-lookup"><span data-stu-id="0401f-105">**To add a new message service to a profile and access the new message service**</span></span>
  
<span data-ttu-id="0401f-106">Rufen [Sie IMsgServiceAdmin2::CreateMsgServiceEx auf.](imsgserviceadmin2-createmsgserviceex.md)</span><span class="sxs-lookup"><span data-stu-id="0401f-106">Call [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md).</span></span> <span data-ttu-id="0401f-107">**CreateMsgServiceEx** führt die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="0401f-107">**CreateMsgServiceEx** performs the following tasks:</span></span> 
  
1. <span data-ttu-id="0401f-108">Kopiert alle relevanten Informationen für den Nachrichtendienst, der sich im MAPISVC befindet. INF-Datei, erstellen Sie einen Profilabschnitt für jeden Anbieterabschnitt.</span><span class="sxs-lookup"><span data-stu-id="0401f-108">Copies all of the relevant information for the message service that is in the MAPISVC.INF file, creating a profile section for every provider section.</span></span>
    
2. <span data-ttu-id="0401f-109">Ruft die Einstiegspunktfunktion des Nachrichtendiensts **MSGSERVICEENTRY** auf, und der  _ulContext-Parameter_ ist auf MSG_SERVICE_CREATE.</span><span class="sxs-lookup"><span data-stu-id="0401f-109">Calls the message service's entry point function, **MSGSERVICEENTRY**, with the  _ulContext_ parameter set to MSG_SERVICE_CREATE.</span></span> 
    
3. <span data-ttu-id="0401f-110">Legt die #A0 des Nachrichtendiensts **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) fest und ruft sie ab.</span><span class="sxs-lookup"><span data-stu-id="0401f-110">Sets and retrieves the message service's **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="0401f-111">**So greifen Sie auf einen neu hinzugefügten Nachrichtendienst zu**</span><span class="sxs-lookup"><span data-stu-id="0401f-111">**To access any newly added message service**</span></span>
  
1. <span data-ttu-id="0401f-112">Rufen [Sie IMsgServiceAdmin::GetMsgServiceTable auf,](imsgserviceadmin-getmsgservicetable.md) um die Nachrichtendiensttabelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0401f-112">Call [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) to retrieve the message service table.</span></span> 
    
2. <span data-ttu-id="0401f-113">Rufen Sie die [IMAPITable::Advise-Methode](imapitable-advise.md) der Nachrichtendiensttabelle auf, um sich für Tabellenbenachrichtigungen zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="0401f-113">Call the message service table's [IMAPITable::Advise](imapitable-advise.md) method to register for table notifications.</span></span> 
    
3. <span data-ttu-id="0401f-114">Wenn MAPI eine TABLE_ROW_ADDED sendet, suchen Sie den Eintragsbezeichner des neu hinzugefügten Nachrichtendiensts in der [SRow-Struktur,](srow.md) die in der TABLE_NOTIFICATION [ist.](table_notification.md)</span><span class="sxs-lookup"><span data-stu-id="0401f-114">When MAPI sends a TABLE_ROW_ADDED notification, locate the entry identifier of the newly added message service in the [SRow](srow.md) structure included in the [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> 
    

