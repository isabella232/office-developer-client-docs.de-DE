---
title: Konfigurieren eines Nachrichtendiensts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d68892e3-7c87-4b3a-a691-bff92f83ed00
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2b170037bc51a7848154c12acbfe700a0142ef8f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564108"
---
# <a name="configuring-a-message-service"></a><span data-ttu-id="2915c-103">Konfigurieren eines Nachrichtendiensts</span><span class="sxs-lookup"><span data-stu-id="2915c-103">Configuring a Message Service</span></span>

  
  
<span data-ttu-id="2915c-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2915c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="2915c-105">**So konfigurieren Sie die-Dienstanbieter in einem Message-Dienst**</span><span class="sxs-lookup"><span data-stu-id="2915c-105">**To configure all the service providers in a message service**</span></span>
  
- <span data-ttu-id="2915c-106">Rufen Sie [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="2915c-106">Call [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> <span data-ttu-id="2915c-107">Wenn alle Daten für die Konfiguration notwendig sind programmgesteuert verfügbar, können Sie, ob eine Benutzeroberfläche angezeigt werden soll oder nicht.</span><span class="sxs-lookup"><span data-stu-id="2915c-107">If all of the data necessary for configuration is available programmatically, you can choose whether or not to display a user interface.</span></span> <span data-ttu-id="2915c-108">Wenn ein Teil der Informationen für einen oder mehrere Anbieter nicht verfügbar ist, stellen Sie jedoch sicher, dass Sie die Kennzeichen SERVICE_UI_ALLOWED oder SERVICE_UI_ALWAYS festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2915c-108">However, if some of the information for one or more providers is not available, make sure that you set the SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS flag.</span></span> <span data-ttu-id="2915c-109">Unterdrücken eine Benutzeroberfläche beim erforderlichen Konfigurationsdaten nicht verfügbar Ergebnisse in einem Nachrichtendienst nicht konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="2915c-109">Suppressing a user interface when required configuration data is unavailable results in an unconfigured message service.</span></span>
    
 <span data-ttu-id="2915c-110">**So konfigurieren Sie einen einzelnen-Dienstanbieter in einem Message-Dienst**</span><span class="sxs-lookup"><span data-stu-id="2915c-110">**To configure a single service provider in a message service**</span></span>
  
1. <span data-ttu-id="2915c-111">Rufen Sie [IMAPISession::GetStatusTable](imapisession-getstatustable.md) Zugriff auf den Dienstanbieter Status-Objekt.</span><span class="sxs-lookup"><span data-stu-id="2915c-111">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the service provider's status object.</span></span> 
    
2. <span data-ttu-id="2915c-112">Rufen Sie [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) , um den Dienstanbieter Eigenschaftenfenster anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="2915c-112">Call [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) to display the service provider's property sheet.</span></span> 
    
<span data-ttu-id="2915c-113">Weitere Informationen zum Status Objekte verwenden finden Sie unter [Statustabelle und Status-Objekte](status-table-and-status-objects.md).</span><span class="sxs-lookup"><span data-stu-id="2915c-113">For more information about using status objects, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>
  

