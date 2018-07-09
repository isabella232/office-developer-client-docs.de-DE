---
title: AusführenMakro-Makroaktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 59ba365d-cff5-4126-bc22-4d5a37578aab
description: Die AusführenMakro-Aktion können Sie ein Benutzer-Benutzeroberfläche (UI) Makro ausführen.
ms.openlocfilehash: 68a59e246c0af8385a17aedcf3da771c720f8fd7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790354"
---
# <a name="runmacro-macro-action-access-custom-web-app"></a><span data-ttu-id="ffb1d-103">AusführenMakro-Makroaktion (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="ffb1d-103">RunMacro Macro Action (Access custom web app)</span></span>

<span data-ttu-id="ffb1d-104">Die **AusführenMakro** -Aktion können Sie ein Benutzer-Benutzeroberfläche (UI) Makro ausführen.</span><span class="sxs-lookup"><span data-stu-id="ffb1d-104">You can use the **RunMacro** action to run a user interface (UI) macro.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="ffb1d-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="ffb1d-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="ffb1d-107">Einstellung</span><span class="sxs-lookup"><span data-stu-id="ffb1d-107">Setting</span></span>

<span data-ttu-id="ffb1d-108">Die **AusführenMakro** -Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="ffb1d-108">The **RunMacro** action has the following arguments.</span></span> 
  
|<span data-ttu-id="ffb1d-109">**Aktionsargument**</span><span class="sxs-lookup"><span data-stu-id="ffb1d-109">**Action argument**</span></span>|<span data-ttu-id="ffb1d-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ffb1d-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ffb1d-111">**Makroname**</span><span class="sxs-lookup"><span data-stu-id="ffb1d-111">**Macro Name**</span></span> <br/> |<span data-ttu-id="ffb1d-112">Der Name des auszuführenden Makros Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="ffb1d-112">The name of the UI macro to run.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ffb1d-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ffb1d-113">Remarks</span></span>

<span data-ttu-id="ffb1d-114">Wenn Sie eine Benutzeroberflächenmakro ausführen, enthält die **AusführenMakro** -Aktion, und er die **AusführenMakro** -Aktion erreicht, führt Access das gewählte UI-Makro.</span><span class="sxs-lookup"><span data-stu-id="ffb1d-114">When you run a UI macro containing the **RunMacro** action, and it reaches the **RunMacro** action, Access runs the called UI macro.</span></span> <span data-ttu-id="ffb1d-115">Wenn die gewählte Benutzeroberflächenmakro beendet wurde, Access gibt Sie zurück zum ursprünglichen UI-Makro und führt die nächste Aktion.</span><span class="sxs-lookup"><span data-stu-id="ffb1d-115">When the called UI macro has finished, Access returns to the original UI macro and runs the next action.</span></span> 
  

