---
title: Löschen eines Nachrichtendiensts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 346608d7-f7de-497e-9852-4d4d7696177e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 27c20242417e51886ab184b1cc87d6ebb185e4bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316863"
---
# <a name="deleting-a-message-service"></a><span data-ttu-id="e8444-103">Löschen eines Nachrichtendiensts</span><span class="sxs-lookup"><span data-stu-id="e8444-103">Deleting a Message Service</span></span>

  
  
<span data-ttu-id="e8444-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8444-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="e8444-105">**So löschen Sie einen Nachrichtendienst aus einem Profil**</span><span class="sxs-lookup"><span data-stu-id="e8444-105">**To delete a message service from a profile**</span></span>
  
1. <span data-ttu-id="e8444-106">Rufen Sie **IMAPISession:: GetMsgServiceTable** auf, um auf die Nachrichtendienst Tabelle zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="e8444-106">Call **IMAPISession::GetMsgServiceTable** to access the message service table.</span></span> 
    
2. <span data-ttu-id="e8444-107">Suchen Sie die Zeile für den Nachrichtendienst, und übergeben Sie die **PR_SERVICE_UID** ([pidtagserviceuid (](pidtagserviceuid-canonical-property.md))-Spalte im _lpuid_ -Parameter an [IMsgServiceAdmin::D eletemsgservice](imsgserviceadmin-deletemsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="e8444-107">Locate the row for the message service and pass its **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) column in the  _lpuid_ parameter to [IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md).</span></span> 
    
 <span data-ttu-id="e8444-108">**DeleteMsgService** Ruft die Einstiegspunktfunktion des Nachrichtendiensts auf, wobei der Parameter _ulContext_ auf MSG_SERVICE_DELETE festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e8444-108">**DeleteMsgService** calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_DELETE.</span></span> <span data-ttu-id="e8444-109">Nachrichtendienste führen zu diesem Zeitpunkt Aufräumvorgänge aus, bevor Sie aus dem Profil entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="e8444-109">Message services perform any clean up tasks at this time before they are removed from the profile.</span></span> 
  

