---
title: StopMacro-Makroaktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: af28534b-6f0d-43ee-ae89-ee2f85da1af1
description: Sie können die StopMacro-Aktion verwenden, um das derzeit ausgeführte Makro zu beenden.
ms.openlocfilehash: 8b80422a297647d556fb4b20cc15fb93e8853466
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429495"
---
# <a name="stopmacro-macro-action-access-custom-web-app"></a><span data-ttu-id="f9232-103">StopMacro-Makroaktion (benutzerdefinierte Access-Web-App)</span><span class="sxs-lookup"><span data-stu-id="f9232-103">StopMacro Macro Action (Access custom web app)</span></span>

<span data-ttu-id="f9232-104">Sie können die **StopMacro-Aktion** verwenden, um das derzeit ausgeführte Makro zu beenden.</span><span class="sxs-lookup"><span data-stu-id="f9232-104">You can use the **StopMacro** action to stop the currently running macro.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="f9232-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="f9232-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="f9232-107">Einstellung</span><span class="sxs-lookup"><span data-stu-id="f9232-107">Setting</span></span>

<span data-ttu-id="f9232-108">Die **StopMacro-Aktion** hat keine Argumente.</span><span class="sxs-lookup"><span data-stu-id="f9232-108">The **StopMacro** action doesn't have any arguments.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f9232-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f9232-109">Remarks</span></span>

<span data-ttu-id="f9232-110">Sie verwenden diese Aktion in der Regel, wenn eine Bedingung es erforderlich macht, das Makro zu beenden.</span><span class="sxs-lookup"><span data-stu-id="f9232-110">You typically use this action when a condition makes it necessary to stop the macro.</span></span> <span data-ttu-id="f9232-111">Sie können z. B. ein Benutzeroberflächenmakro erstellen, das eine Ansicht mit den Täglichen Auftragssummen für das in der aktuellen Ansicht eingegebene Datum öffnet.</span><span class="sxs-lookup"><span data-stu-id="f9232-111">For example, you might create a user interface (UI) macro that opens a view showing the daily order totals for the date entered in the current view.</span></span> <span data-ttu-id="f9232-112">Sie können einen bedingten Ausdruck verwenden, um sicherzustellen, dass das Steuerelement Order Date im Dialogfeld ein gültiges Datum enthält.</span><span class="sxs-lookup"><span data-stu-id="f9232-112">You could use a conditional expression to be sure that the Order Date control on the dialog box contains a valid date.</span></span> <span data-ttu-id="f9232-113">Andern falls nicht, kann die **MessageBox-Aktion** eine Fehlermeldung anzeigen, und die **StopMacro-Aktion** kann das Benutzeroberflächenmakro beenden.</span><span class="sxs-lookup"><span data-stu-id="f9232-113">If it doesn't, the **MessageBox** action can display an error message and the **StopMacro** action can stop the UI macro.</span></span> 
  

