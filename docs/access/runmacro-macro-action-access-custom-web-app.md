---
title: RunMacro-Makroaktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 59ba365d-cff5-4126-bc22-4d5a37578aab
description: Mit der RunMacro-Aktion können Sie ein Benutzeroberflächenmakro ausführen.
ms.openlocfilehash: 98e3b17a6c64fa12ac37e4551d45714c873f5ccb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438442"
---
# <a name="runmacro-macro-action-access-custom-web-app"></a><span data-ttu-id="8fc61-103">RunMacro-Makroaktion (benutzerdefinierte Access-Web-App)</span><span class="sxs-lookup"><span data-stu-id="8fc61-103">RunMacro Macro Action (Access custom web app)</span></span>

<span data-ttu-id="8fc61-104">Mit der **RunMacro-Aktion** können Sie ein Benutzeroberflächenmakro ausführen.</span><span class="sxs-lookup"><span data-stu-id="8fc61-104">You can use the **RunMacro** action to run a user interface (UI) macro.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="8fc61-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="8fc61-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="8fc61-107">Einstellung</span><span class="sxs-lookup"><span data-stu-id="8fc61-107">Setting</span></span>

<span data-ttu-id="8fc61-108">Die **AusführenMakro**-Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="8fc61-108">The **RunMacro** action has the following arguments.</span></span> 
  
|<span data-ttu-id="8fc61-109">**Aktionsargument**</span><span class="sxs-lookup"><span data-stu-id="8fc61-109">**Action argument**</span></span>|<span data-ttu-id="8fc61-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8fc61-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8fc61-111">**Makroname**</span><span class="sxs-lookup"><span data-stu-id="8fc61-111">**Macro Name**</span></span> <br/> |<span data-ttu-id="8fc61-112">Der Name des zu ausführende Benutzeroberflächenmakros.</span><span class="sxs-lookup"><span data-stu-id="8fc61-112">The name of the UI macro to run.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8fc61-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8fc61-113">Remarks</span></span>

<span data-ttu-id="8fc61-114">Wenn Sie ein Benutzeroberflächenmakro ausführen, das die **RunMacro-Aktion** enthält und die **RunMacro-Aktion** erreicht, führt Access das aufgerufene Benutzeroberflächenmakro aus.</span><span class="sxs-lookup"><span data-stu-id="8fc61-114">When you run a UI macro containing the **RunMacro** action, and it reaches the **RunMacro** action, Access runs the called UI macro.</span></span> <span data-ttu-id="8fc61-115">Nach Abschluss des aufgerufenen Benutzeroberflächenmakros kehrt Access zum ursprünglichen Benutzeroberflächenmakro zurück und führt die nächste Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="8fc61-115">When the called UI macro has finished, Access returns to the original UI macro and runs the next action.</span></span> 
  

