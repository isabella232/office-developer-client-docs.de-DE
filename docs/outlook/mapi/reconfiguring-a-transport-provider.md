---
title: Neukonfigurieren eines Transport Anbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d466bde-b70d-44b6-ba03-6ad8353ec759
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b35ca2bb52439cf2ba1750c6fad2883730c4c3f8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408410"
---
# <a name="reconfiguring-a-transport-provider"></a><span data-ttu-id="17353-103">Neukonfigurieren eines Transport Anbieters</span><span class="sxs-lookup"><span data-stu-id="17353-103">Reconfiguring a Transport Provider</span></span>

  
  
<span data-ttu-id="17353-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="17353-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="17353-105">Mit dem Status-Objekt eines Transportanbieters können Sie einige der Eigenschaften des Anbieters ändern.</span><span class="sxs-lookup"><span data-stu-id="17353-105">You can use a transport provider's status object to change some of the properties of the provider.</span></span> <span data-ttu-id="17353-106">Der Eigenschaftentyp, der geändert werden kann, hängt von den Eigenschaften ab, die im Eigenschaftenfenster des Anbieters enthalten sind, und davon, wie diese Eigenschaften definiert werden.</span><span class="sxs-lookup"><span data-stu-id="17353-106">The range of properties that can be changed depends on the properties that are included with the provider's property sheet and how those properties are defined.</span></span> 
  
 <span data-ttu-id="17353-107">**So konfigurieren Sie einen aktiven Transportanbieter neu**</span><span class="sxs-lookup"><span data-stu-id="17353-107">**To reconfigure an active transport provider**</span></span>
  
1. <span data-ttu-id="17353-108">Rufen Sie [IMAPISession::](imapisession-getstatustable.md) getstatusable auf, um auf die Statustabelle zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="17353-108">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table.</span></span> 
    
2. <span data-ttu-id="17353-109">Suchen Sie die Zeile für den Transportanbieter, die neu konfiguriert werden soll, indem Sie eine Eigenschaftseinschränkung erstellen, die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) mit dem Namen des Zielanbieters entspricht.</span><span class="sxs-lookup"><span data-stu-id="17353-109">Locate the row for the transport provider to be reconfigured by creating a property restriction that matches **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) with the name of the target provider.</span></span> 
    
3. <span data-ttu-id="17353-110">Rufen Sie [IMAPITable:: FindRow](imapitable-findrow.md) auf, um die entsprechende Zeile abzurufen.</span><span class="sxs-lookup"><span data-stu-id="17353-110">Call [IMAPITable::FindRow](imapitable-findrow.md) to retrieve the appropriate row.</span></span> 
    
4. <span data-ttu-id="17353-111">Überprüfen Sie, ob die STATUS_SETTINGS_DIALOG-und STATUS_VALIDATE_STATE-Flags in der **PR_RESOURCE_METHODS** ([pidtagresourcemethods (](pidtagresourcemethods-canonical-property.md))-Eigenschaft des Ziel Transportanbieters festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="17353-111">Check that the STATUS_SETTINGS_DIALOG and STATUS_VALIDATE_STATE flags are set in the target transport provider's **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span> <span data-ttu-id="17353-112">Wenn STATUS_SETTINGS_DIALOG nicht festgelegt ist, wird vom Transportanbieter kein Konfigurationseigenschaften Fenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="17353-112">If STATUS_SETTINGS_DIALOG is not set, the transport provider does not display a configuration property sheet.</span></span> <span data-ttu-id="17353-113">Wenn STATUS_VALIDATE_STATE nicht festgelegt ist, können Sie die dynamische Neukonfiguration nicht ausführen.</span><span class="sxs-lookup"><span data-stu-id="17353-113">If STATUS_VALIDATE_STATE is not set, you cannot perform dynamic reconfiguration.</span></span>
    
5. <span data-ttu-id="17353-114">Wenn STATUS_SETTINGS_DIALOG festgelegt ist, rufen Sie [IMAPIStatus:: Settingsdialog](imapistatus-settingsdialog.md) auf, um das Eigenschaftenfenster des Transportanbieters anzuzeigen und dem Benutzer die Möglichkeit zu geben, Änderungen vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="17353-114">If STATUS_SETTINGS_DIALOG is set, call [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) to display the transport provider's property sheet and allow the user to make changes.</span></span> 
    
6. <span data-ttu-id="17353-115">Nachdem der Benutzer die Neukonfiguration abgeschlossen hat, rufen Sie [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) auf, wenn STATUS_VALIDATE_STATE festgelegt ist, CONFIG_CHANGED übergeben.</span><span class="sxs-lookup"><span data-stu-id="17353-115">After the user has finished with the reconfiguration, call [IMAPIStatus::ValidateState](imapistatus-validatestate.md) if STATUS_VALIDATE_STATE is set, passing CONFIG_CHANGED.</span></span> 
    

