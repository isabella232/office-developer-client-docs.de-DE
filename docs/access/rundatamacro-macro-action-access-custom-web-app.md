---
title: AusführenDatenmakro-Makroaktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: f6010ac5-6c08-4c1b-a811-ff81b30ed5f0
description: Die AusführenDatenmakro-Aktion können Sie eine eigenständige Datenmakro ausführen.
ms.openlocfilehash: 55a0ff4c731dc517c5d71aa20d8e46c3b4ff4611
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790349"
---
# <a name="rundatamacro-macro-action-access-custom-web-app"></a><span data-ttu-id="2fb83-103">AusführenDatenmakro-Makroaktion (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="2fb83-103">RunDataMacro Macro Action (Access custom web app)</span></span>

<span data-ttu-id="2fb83-104">Die **AusführenDatenmakro** -Aktion können Sie eine eigenständige Datenmakro ausführen.</span><span class="sxs-lookup"><span data-stu-id="2fb83-104">You can use the **RunDataMacro** action to run a standalone data macro.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="2fb83-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/de-de/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="2fb83-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/de-de/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="2fb83-107">Einstellung</span><span class="sxs-lookup"><span data-stu-id="2fb83-107">Setting</span></span>

<span data-ttu-id="2fb83-108">Die **AusführenDatenmakro** -Aktion kann mit dem folgenden Argument verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2fb83-108">The **RunDataMacro** action has the following argument.</span></span> 
  
|<span data-ttu-id="2fb83-109">**Aktionsargument**</span><span class="sxs-lookup"><span data-stu-id="2fb83-109">**Action argument**</span></span>|<span data-ttu-id="2fb83-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2fb83-110">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="2fb83-111">_Makroname_</span><span class="sxs-lookup"><span data-stu-id="2fb83-111">_Macro Name_</span></span> <br/> |<span data-ttu-id="2fb83-112">Der Name des Datenmakros, das ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2fb83-112">The name of the data macro to run.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2fb83-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2fb83-113">Remarks</span></span>

<span data-ttu-id="2fb83-114">Wenn Sie das auszuführende Datenmakro im Makro-Designer auswählen, wird von Access ermittelt, ob das Datenmakro Parameter erfordert.</span><span class="sxs-lookup"><span data-stu-id="2fb83-114">When you select the data macro that you want to run in the macro designer, Access determines if the data macro requires parameters.</span></span> <span data-ttu-id="2fb83-115">Wenn das Datenmakro Parameter erfordert, erscheinen Textfelder, in dem Sie die Argumente eingeben können.</span><span class="sxs-lookup"><span data-stu-id="2fb83-115">If the data macro requires parameters, text boxes appear where you can type in the arguments.</span></span>
  
<span data-ttu-id="2fb83-p103">Wenn Sie ein Makro ausführen, das die **AusführenDatenmakro** -Aktion enthält, und dieses die **AusführenDatenmakro** -Aktion erreicht, wird das aufgerufene Datenmakro in Access ausgeführt. Sobald das aufgerufene Datenmakro beendet wurde, kehrt Access zum ursprünglichen Makro zurück und führt die nächste Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="2fb83-p103">When you run a macro that contains the **RunDataMacro** action and it reaches the **RunDataMacro** action, Access runs the called data macro. When the called data macro has finished, Access returns to the original macro and runs the next action.</span></span> 
  

