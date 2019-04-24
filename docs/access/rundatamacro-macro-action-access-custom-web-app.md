---
title: Ausführendatenmakro-Makroaktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: f6010ac5-6c08-4c1b-a811-ff81b30ed5f0
description: Sie können die Ausführendatenmakro-Aktion verwenden, um ein eigenständiges datenmakro auszuführen.
ms.openlocfilehash: 68c0e5a3837039bdab1165e686adb3bdf2a5b6f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304242"
---
# <a name="rundatamacro-macro-action-access-custom-web-app"></a><span data-ttu-id="f0b8c-103">Ausführendatenmakro-Makroaktion (benutzerdefinierte Access-Web-App)</span><span class="sxs-lookup"><span data-stu-id="f0b8c-103">RunDataMacro Macro Action (Access custom web app)</span></span>

<span data-ttu-id="f0b8c-104">Sie können die **ausführendatenmakro** -Aktion verwenden, um ein eigenständiges datenmakro auszuführen.</span><span class="sxs-lookup"><span data-stu-id="f0b8c-104">You can use the **RunDataMacro** action to run a standalone data macro.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="f0b8c-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="f0b8c-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="f0b8c-107">Einstellung</span><span class="sxs-lookup"><span data-stu-id="f0b8c-107">Setting</span></span>

<span data-ttu-id="f0b8c-108">Die **AusführenDatenmakro**-Aktion kann mit dem folgenden Argument verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f0b8c-108">The **RunDataMacro** action has the following argument.</span></span> 
  
|<span data-ttu-id="f0b8c-109">**Aktionsargument**</span><span class="sxs-lookup"><span data-stu-id="f0b8c-109">**Action argument**</span></span>|<span data-ttu-id="f0b8c-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f0b8c-110">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="f0b8c-111">_Makroname_</span><span class="sxs-lookup"><span data-stu-id="f0b8c-111">_Macro Name_</span></span> <br/> |<span data-ttu-id="f0b8c-112">Der Name des Datenmakros, das ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f0b8c-112">The name of the data macro to run.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f0b8c-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f0b8c-113">Remarks</span></span>

<span data-ttu-id="f0b8c-114">Wenn Sie das auszuführende Datenmakro im Makro-Designer auswählen, wird von Access ermittelt, ob das Datenmakro Parameter erfordert.</span><span class="sxs-lookup"><span data-stu-id="f0b8c-114">When you select the data macro that you want to run in the macro designer, Access determines if the data macro requires parameters.</span></span> <span data-ttu-id="f0b8c-115">Wenn das datenmakro Parameter erfordert, werden Textfelder angezeigt, in denen Sie die Argumente eingeben können.</span><span class="sxs-lookup"><span data-stu-id="f0b8c-115">If the data macro requires parameters, text boxes appear where you can type in the arguments.</span></span>
  
<span data-ttu-id="f0b8c-p103">Wenn Sie ein Makro ausführen, das die **AusführenDatenmakro** -Aktion enthält, und dieses die **AusführenDatenmakro** -Aktion erreicht, wird das aufgerufene Datenmakro in Access ausgeführt. Sobald das aufgerufene Datenmakro beendet wurde, kehrt Access zum ursprünglichen Makro zurück und führt die nächste Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="f0b8c-p103">When you run a macro that contains the **RunDataMacro** action and it reaches the **RunDataMacro** action, Access runs the called data macro. When the called data macro has finished, Access returns to the original macro and runs the next action.</span></span> 
  

