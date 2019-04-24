---
title: RunMacro-Makroaktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 59ba365d-cff5-4126-bc22-4d5a37578aab
description: Sie können die RunMacro-Aktion verwenden, um ein Benutzeroberflächen Makro auszuführen.
ms.openlocfilehash: 98e3b17a6c64fa12ac37e4551d45714c873f5ccb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307966"
---
# <a name="runmacro-macro-action-access-custom-web-app"></a><span data-ttu-id="994bd-103">RunMacro-Makroaktion (benutzerdefinierte Access-Web-App)</span><span class="sxs-lookup"><span data-stu-id="994bd-103">RunMacro Macro Action (Access custom web app)</span></span>

<span data-ttu-id="994bd-104">Sie können die **RunMacro** -Aktion verwenden, um ein Benutzeroberflächen Makro auszuführen.</span><span class="sxs-lookup"><span data-stu-id="994bd-104">You can use the **RunMacro** action to run a user interface (UI) macro.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="994bd-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="994bd-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="994bd-107">Einstellung</span><span class="sxs-lookup"><span data-stu-id="994bd-107">Setting</span></span>

<span data-ttu-id="994bd-108">Die **AusführenMakro**-Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="994bd-108">The **RunMacro** action has the following arguments.</span></span> 
  
|<span data-ttu-id="994bd-109">**Aktionsargument**</span><span class="sxs-lookup"><span data-stu-id="994bd-109">**Action argument**</span></span>|<span data-ttu-id="994bd-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="994bd-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="994bd-111">**Makroname**</span><span class="sxs-lookup"><span data-stu-id="994bd-111">**Macro Name**</span></span> <br/> |<span data-ttu-id="994bd-112">Der Name des auszuführenden Benutzeroberflächen Makros.</span><span class="sxs-lookup"><span data-stu-id="994bd-112">The name of the UI macro to run.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="994bd-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="994bd-113">Remarks</span></span>

<span data-ttu-id="994bd-114">Wenn Sie ein Benutzeroberflächen Makro ausführen, das die **RunMacro** -Aktion enthält, und es die **RunMacro** -Aktion erreicht, wird das aufgerufene Benutzeroberflächen Makro von Access ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="994bd-114">When you run a UI macro containing the **RunMacro** action, and it reaches the **RunMacro** action, Access runs the called UI macro.</span></span> <span data-ttu-id="994bd-115">Wenn das aufgerufene Benutzeroberflächen Makro beendet wurde, kehrt Access zum ursprünglichen Benutzeroberflächen Makro zurück und führt die nächste Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="994bd-115">When the called UI macro has finished, Access returns to the original UI macro and runs the next action.</span></span> 
  

