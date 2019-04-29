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
ms.openlocfilehash: 4c3d30c7111e7b26886cbfb069ec2822d2ee0234
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434508"
---
# <a name="configuring-a-message-service"></a><span data-ttu-id="be42f-103">Konfigurieren eines Nachrichtendiensts</span><span class="sxs-lookup"><span data-stu-id="be42f-103">Configuring a Message Service</span></span>

  
  
<span data-ttu-id="be42f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be42f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="be42f-105">**So konfigurieren Sie alle Dienstanbieter in einem Nachrichtendienst**</span><span class="sxs-lookup"><span data-stu-id="be42f-105">**To configure all the service providers in a message service**</span></span>
  
- <span data-ttu-id="be42f-106">Rufen Sie [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)auf.</span><span class="sxs-lookup"><span data-stu-id="be42f-106">Call [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> <span data-ttu-id="be42f-107">Wenn alle für die Konfiguration erforderlichen Daten programmgesteuert verfügbar sind, können Sie auswählen, ob eine Benutzeroberfläche angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="be42f-107">If all of the data necessary for configuration is available programmatically, you can choose whether or not to display a user interface.</span></span> <span data-ttu-id="be42f-108">Wenn jedoch einige der Informationen für einen oder mehrere Anbieter nicht verfügbar sind, stellen Sie sicher, dass Sie das SERVICE_UI_ALLOWED-oder SERVICE_UI_ALWAYS-Flag festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="be42f-108">However, if some of the information for one or more providers is not available, make sure that you set the SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS flag.</span></span> <span data-ttu-id="be42f-109">Das unterdrücken einer Benutzeroberfläche, wenn erforderliche Konfigurationsdaten nicht verfügbar sind, führt zu einem nicht konfigurierten Nachrichtendienst.</span><span class="sxs-lookup"><span data-stu-id="be42f-109">Suppressing a user interface when required configuration data is unavailable results in an unconfigured message service.</span></span>
    
 <span data-ttu-id="be42f-110">**So konfigurieren Sie einen einzelnen Dienstanbieter in einem Nachrichtendienst**</span><span class="sxs-lookup"><span data-stu-id="be42f-110">**To configure a single service provider in a message service**</span></span>
  
1. <span data-ttu-id="be42f-111">Rufen Sie [IMAPISession::](imapisession-getstatustable.md) getstatusable auf, um auf das Statusobjekt des Dienstanbieters zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="be42f-111">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the service provider's status object.</span></span> 
    
2. <span data-ttu-id="be42f-112">Rufen Sie [IMAPIStatus:: Settingsdialog](imapistatus-settingsdialog.md) auf, um das Eigenschaftenfenster des Dienstanbieters anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="be42f-112">Call [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) to display the service provider's property sheet.</span></span> 
    
<span data-ttu-id="be42f-113">Weitere Informationen zur Verwendung von Status-Objekten finden Sie unter [Status Table-und Status-Objekte](status-table-and-status-objects.md).</span><span class="sxs-lookup"><span data-stu-id="be42f-113">For more information about using status objects, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>
  

