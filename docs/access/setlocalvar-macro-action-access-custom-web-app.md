---
title: SetLocalVar-Makroaktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 12444313-1cfa-49ff-89da-3030fe75c13e
description: Mit der FestlegenLokaleVar -Aktion erstellen Sie eine temporäre Variable und legen diese auf einen bestimmten Wert fest.
ms.openlocfilehash: 2493bc5c908c551e171a8fa7d9eaeea699a04f72
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310942"
---
# <a name="setlocalvar-macro-action-access-custom-web-app"></a><span data-ttu-id="6821c-103">SetLocalVar-Makroaktion (benutzerdefinierte Access-Web-App)</span><span class="sxs-lookup"><span data-stu-id="6821c-103">SetLocalVar Macro Action (Access custom web app)</span></span>

<span data-ttu-id="6821c-104">Mit der **FestlegenLokaleVar** -Aktion erstellen Sie eine temporäre Variable und legen diese auf einen bestimmten Wert fest.</span><span class="sxs-lookup"><span data-stu-id="6821c-104">The **SetLocalVar** action creates a temporary variable and set it to a specific value.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="6821c-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="6821c-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6821c-107">Die **SetLocalVar** -Aktion ist nur in datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6821c-107">The **SetLocalVar** action is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="6821c-108">Einstellung</span><span class="sxs-lookup"><span data-stu-id="6821c-108">Setting</span></span>

<span data-ttu-id="6821c-109">Die **FestlegenLokaleVar**-Aktion kann mit den folgenden Argumenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6821c-109">The **SetLocalVar** action has the following arguments.</span></span> 
  
|<span data-ttu-id="6821c-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="6821c-110">**Argument name**</span></span>|<span data-ttu-id="6821c-111">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="6821c-111">**Required**</span></span>|<span data-ttu-id="6821c-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6821c-112">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6821c-113">**Name**</span><span class="sxs-lookup"><span data-stu-id="6821c-113">**Name**</span></span> <br/> |<span data-ttu-id="6821c-114">Ja</span><span class="sxs-lookup"><span data-stu-id="6821c-114">Yes</span></span>  <br/> |<span data-ttu-id="6821c-115">Eine Zeichenfolge, die den Namen der Variablen angibt.</span><span class="sxs-lookup"><span data-stu-id="6821c-115">A string that specifies the name of the variable.</span></span>  <br/> |
|<span data-ttu-id="6821c-116">**Ausdruck**</span><span class="sxs-lookup"><span data-stu-id="6821c-116">**Expression**</span></span> <br/> |<span data-ttu-id="6821c-117">Ja</span><span class="sxs-lookup"><span data-stu-id="6821c-117">Yes</span></span>  <br/> |<span data-ttu-id="6821c-118">Ein Ausdruck, mit dem der Wert für diese temporäre Variable festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="6821c-118">An expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="6821c-119">Stellen Sie dem Ausdruck kein Gleichheitszeichen (=) voran.</span><span class="sxs-lookup"><span data-stu-id="6821c-119">Do not precede the expression with the equal sign (=).</span></span> <span data-ttu-id="6821c-120">Sie können auf die **Generator** -Schaltfläche klicken, um den **Ausdrucks-Generator** zum Festlegen dieses Arguments zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="6821c-120">You can click the **Build** button to use the **Expression Builder** to set this argument.</span></span>  <br/> |
   

