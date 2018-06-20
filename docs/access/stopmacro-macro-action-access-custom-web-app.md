---
title: StoppMakro-Makroaktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: af28534b-6f0d-43ee-ae89-ee2f85da1af1
description: Die StoppMakro-Aktion können Sie das derzeit ausgeführte Makro anzuhalten.
ms.openlocfilehash: 54501b65eb1847287e810ae43742a2e6e5384264
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790360"
---
# <a name="stopmacro-macro-action-access-custom-web-app"></a><span data-ttu-id="2866f-103">StoppMakro-Makroaktion (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="2866f-103">StopMacro Macro Action (Access custom web app)</span></span>

<span data-ttu-id="2866f-104">Die **StoppMakro** -Aktion können Sie das derzeit ausgeführte Makro anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="2866f-104">You can use the **StopMacro** action to stop the currently running macro.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="2866f-p101">[!WICHTIG] Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="2866f-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="2866f-107">Einstellung</span><span class="sxs-lookup"><span data-stu-id="2866f-107">Setting</span></span>

<span data-ttu-id="2866f-108">Die **StoppMakro** -Aktion verfügt nicht über keine Argumente.</span><span class="sxs-lookup"><span data-stu-id="2866f-108">The **StopMacro** action doesn't have any arguments.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2866f-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2866f-109">Remarks</span></span>

<span data-ttu-id="2866f-110">Normalerweise verwenden Sie diese Aktion, wenn eine Bedingung das Makro anzuhalten vornimmt.</span><span class="sxs-lookup"><span data-stu-id="2866f-110">You typically use this action when a condition makes it necessary to stop the macro.</span></span> <span data-ttu-id="2866f-111">Beispielsweise können Sie ein Benutzer Benutzeroberfläche (UI)-Makro erstellen, das eine Ansicht mit der täglichen Summen Reihenfolge für das Datum in der aktuellen Ansicht geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="2866f-111">For example, you might create a user interface (UI) macro that opens a view showing the daily order totals for the date entered in the current view.</span></span> <span data-ttu-id="2866f-112">Sie können einen bedingten Ausdruck verwenden, um sicherzustellen, dass das Steuerelement Bestelldatum im Dialogfeld ein gültiges Datum enthält.</span><span class="sxs-lookup"><span data-stu-id="2866f-112">You could use a conditional expression to be sure that the Order Date control on the dialog box contains a valid date.</span></span> <span data-ttu-id="2866f-113">Wenn dies nicht der Fall, die **Abfrageergebnis** -Aktion kann eine Fehlermeldung angezeigt, und die **StoppMakro** -Aktion kann das UI-Makro beenden.</span><span class="sxs-lookup"><span data-stu-id="2866f-113">If it doesn't, the **MessageBox** action can display an error message and the **StopMacro** action can stop the UI macro.</span></span> 
  

