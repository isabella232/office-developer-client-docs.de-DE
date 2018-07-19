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
ms.openlocfilehash: a7735be5cfb8ff0716b6bd6eba4951563bb938ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791249"
---
# <a name="adding-a-message-service"></a><span data-ttu-id="0b2c5-103">Hinzufügen eines Nachrichtendiensts</span><span class="sxs-lookup"><span data-stu-id="0b2c5-103">Adding a Message Service</span></span>

  
  
<span data-ttu-id="0b2c5-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0b2c5-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="0b2c5-105">**Zum Hinzufügen eines neuen Nachricht-Diensts zu einem Profil und Zugreifen auf den neuen Dienst**</span><span class="sxs-lookup"><span data-stu-id="0b2c5-105">**To add a new message service to a profile and access the new message service**</span></span>
  
<span data-ttu-id="0b2c5-106">Rufen Sie [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md).</span><span class="sxs-lookup"><span data-stu-id="0b2c5-106">Call [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md).</span></span> <span data-ttu-id="0b2c5-107">**CreateMsgServiceEx** führt die folgenden Aufgaben:</span><span class="sxs-lookup"><span data-stu-id="0b2c5-107">**CreateMsgServiceEx** performs the following tasks:</span></span> 
  
1. <span data-ttu-id="0b2c5-108">Kopiert alle relevanten Informationen für den Dienst, der in die Datei MAPISVC ist. INF-Datei, Erstellen eines Profils Abschnitts für jede Anbieterabschnitt.</span><span class="sxs-lookup"><span data-stu-id="0b2c5-108">Copies all of the relevant information for the message service that is in the MAPISVC.INF file, creating a profile section for every provider section.</span></span>
    
2. <span data-ttu-id="0b2c5-109">Ruft die Messagingdiensts Eintrag Punktfunktion **MSGSERVICEENTRY**, mit dem _UlContext_ -Parameter auf MSG_SERVICE_CREATE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0b2c5-109">Calls the message service's entry point function, **MSGSERVICEENTRY**, with the  _ulContext_ parameter set to MSG_SERVICE_CREATE.</span></span> 
    
3. <span data-ttu-id="0b2c5-110">Legt fest, und die Messagingdiensts **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))-Eigenschaft abruft.</span><span class="sxs-lookup"><span data-stu-id="0b2c5-110">Sets and retrieves the message service's **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="0b2c5-111">**Greifen Sie auf alle Dienste neu hinzugefügte Nachricht**</span><span class="sxs-lookup"><span data-stu-id="0b2c5-111">**To access any newly added message service**</span></span>
  
1. <span data-ttu-id="0b2c5-112">Rufen Sie [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) zum Abrufen der Tabelle der Dienste.</span><span class="sxs-lookup"><span data-stu-id="0b2c5-112">Call [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) to retrieve the message service table.</span></span> 
    
2. <span data-ttu-id="0b2c5-113">Rufen Sie die Nachricht Service Tabelle [IMAPITable::Advise](imapitable-advise.md) -Methode für die Tabelle Benachrichtigungen registriert.</span><span class="sxs-lookup"><span data-stu-id="0b2c5-113">Call the message service table's [IMAPITable::Advise](imapitable-advise.md) method to register for table notifications.</span></span> 
    
3. <span data-ttu-id="0b2c5-114">Wenn MAPI TABLE_ROW_ADDED Benachrichtigung sendet, suchen Sie die Eintrags-ID des neu hinzugefügten Nachricht-Diensts in der [SRow](srow.md) -Struktur, die in der Struktur [TABLE_NOTIFICATION](table_notification.md) enthalten.</span><span class="sxs-lookup"><span data-stu-id="0b2c5-114">When MAPI sends a TABLE_ROW_ADDED notification, locate the entry identifier of the newly added message service in the [SRow](srow.md) structure included in the [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> 
    

