---
title: Neukonfigurieren eines Transportdienstes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d466bde-b70d-44b6-ba03-6ad8353ec759
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ec5a431d04799e3f19c23dd0437aeac13fbf0968
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795351"
---
# <a name="reconfiguring-a-transport-provider"></a><span data-ttu-id="ff5a6-103">Neukonfigurieren eines Transportdienstes</span><span class="sxs-lookup"><span data-stu-id="ff5a6-103">Reconfiguring a Transport Provider</span></span>

  
  
<span data-ttu-id="ff5a6-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ff5a6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ff5a6-105">Status-Objekt eines Transportdienstes können Sie einige der Eigenschaften des Anbieters ändern.</span><span class="sxs-lookup"><span data-stu-id="ff5a6-105">You can use a transport provider's status object to change some of the properties of the provider.</span></span> <span data-ttu-id="ff5a6-106">Bereich von Eigenschaften, die geändert werden kann, hängt von der Eigenschaften, die mit dem Anbieter Eigenschaftenfenster und wie diese Eigenschaften definiert sind, enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="ff5a6-106">The range of properties that can be changed depends on the properties that are included with the provider's property sheet and how those properties are defined.</span></span> 
  
 <span data-ttu-id="ff5a6-107">**So konfigurieren Sie eine aktive Transportdienst neu**</span><span class="sxs-lookup"><span data-stu-id="ff5a6-107">**To reconfigure an active transport provider**</span></span>
  
1. <span data-ttu-id="ff5a6-108">Rufen Sie [IMAPISession::GetStatusTable](imapisession-getstatustable.md) Zugriff auf die Statustabelle.</span><span class="sxs-lookup"><span data-stu-id="ff5a6-108">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table.</span></span> 
    
2. <span data-ttu-id="ff5a6-109">Suchen Sie die Zeile für den Transportdienst neu konfiguriert werden, indem Sie eine eigenschaftseinschränkung, die entspricht **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) erstellen, mit dem Namen des Zielanbieters.</span><span class="sxs-lookup"><span data-stu-id="ff5a6-109">Locate the row for the transport provider to be reconfigured by creating a property restriction that matches **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) with the name of the target provider.</span></span> 
    
3. <span data-ttu-id="ff5a6-110">Rufen Sie [IMAPITable](imapitable-findrow.md) zum Abrufen der entsprechenden Zeile.</span><span class="sxs-lookup"><span data-stu-id="ff5a6-110">Call [IMAPITable::FindRow](imapitable-findrow.md) to retrieve the appropriate row.</span></span> 
    
4. <span data-ttu-id="ff5a6-111">Überprüfen Sie, dass die Flags STATUS_SETTINGS_DIALOG und STATUS_VALIDATE_STATE in der Adressbuchhierarchie Ziel **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))-Eigenschaft festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ff5a6-111">Check that the STATUS_SETTINGS_DIALOG and STATUS_VALIDATE_STATE flags are set in the target transport provider's **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span> <span data-ttu-id="ff5a6-112">Wenn STATUS_SETTINGS_DIALOG nicht festgelegt ist, wird der Adressbuchhierarchie ein Eigenschaftenblatts Konfiguration nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ff5a6-112">If STATUS_SETTINGS_DIALOG is not set, the transport provider does not display a configuration property sheet.</span></span> <span data-ttu-id="ff5a6-113">Wenn STATUS_VALIDATE_STATE nicht festgelegt ist, nicht Dr möglich.</span><span class="sxs-lookup"><span data-stu-id="ff5a6-113">If STATUS_VALIDATE_STATE is not set, you cannot perform dynamic reconfiguration.</span></span>
    
5. <span data-ttu-id="ff5a6-114">Wenn STATUS_SETTINGS_DIALOG festgelegt ist, rufen Sie [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) zum Anzeigen der Adressbuchhierarchie Eigenschaftenfenster und ermöglicht es dem Benutzer, um Änderungen vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="ff5a6-114">If STATUS_SETTINGS_DIALOG is set, call [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) to display the transport provider's property sheet and allow the user to make changes.</span></span> 
    
6. <span data-ttu-id="ff5a6-115">Nachdem der Benutzer mit der Neukonfiguration abgeschlossen wurde, rufen Sie [IMAPIStatus::ValidateState](imapistatus-validatestate.md) Wenn STATUS_VALIDATE_STATE übergeben CONFIG_CHANGED festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ff5a6-115">After the user has finished with the reconfiguration, call [IMAPIStatus::ValidateState](imapistatus-validatestate.md) if STATUS_VALIDATE_STATE is set, passing CONFIG_CHANGED.</span></span> 
    

