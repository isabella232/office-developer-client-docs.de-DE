---
title: SetReturnVar-Makroaktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 57965c84-7a52-4d7c-9c7f-be3d4570576d
description: Mit der SetReturnVar-Aktion wird eine Rückgabevariable erstellt und auf einen bestimmten Wert festgelegt.
ms.openlocfilehash: 29445f5021bed99fe45cee1d34457f1f91ca417d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310946"
---
# <a name="setreturnvar-macro-action-access-custom-web-app"></a><span data-ttu-id="b17cc-103">SetReturnVar-Makroaktion (benutzerdefinierte Access-Web-App)</span><span class="sxs-lookup"><span data-stu-id="b17cc-103">SetReturnVar Macro action (Access custom web app)</span></span>

<span data-ttu-id="b17cc-104">Mit der **SetReturnVar** -Aktion wird eine Rückgabevariable erstellt und auf einen bestimmten Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b17cc-104">The **SetReturnVar** action creates a return variable and sets it to a specific value.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="b17cc-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="b17cc-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b17cc-107">Die **SetReturnVar** -Aktion ist nur in datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b17cc-107">The **SetReturnVar** action is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="b17cc-108">Einstellung</span><span class="sxs-lookup"><span data-stu-id="b17cc-108">Setting</span></span>

<span data-ttu-id="b17cc-109">Die **SetReturnVar** -Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="b17cc-109">The **SetReturnVar** action has the following arguments.</span></span> 
  
|<span data-ttu-id="b17cc-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="b17cc-110">**Argument name**</span></span>|<span data-ttu-id="b17cc-111">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="b17cc-111">**Required**</span></span>|<span data-ttu-id="b17cc-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b17cc-112">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="b17cc-113">_Name_</span><span class="sxs-lookup"><span data-stu-id="b17cc-113">_Name_</span></span> <br/> |<span data-ttu-id="b17cc-114">Ja</span><span class="sxs-lookup"><span data-stu-id="b17cc-114">Yes</span></span>  <br/> |<span data-ttu-id="b17cc-115">Eine Zeichenfolge, die den Namen der Variablen angibt.</span><span class="sxs-lookup"><span data-stu-id="b17cc-115">A string that specifies the name of the variable.</span></span>  <br/> |
| <span data-ttu-id="b17cc-116">_Ausdruck_</span><span class="sxs-lookup"><span data-stu-id="b17cc-116">_Expression_</span></span> <br/> |<span data-ttu-id="b17cc-117">Ja</span><span class="sxs-lookup"><span data-stu-id="b17cc-117">Yes</span></span>  <br/> |<span data-ttu-id="b17cc-118">Ein Ausdruck, mit dem der Wert für diese temporäre Variable festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="b17cc-118">An expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="b17cc-119">Stellen Sie dem Ausdruck kein Gleichheitszeichen (=) voran.</span><span class="sxs-lookup"><span data-stu-id="b17cc-119">Do not precede the expression with the equal sign (=).</span></span> <span data-ttu-id="b17cc-120">Sie können auf die **Generator** -Schaltfläche klicken, um den **Ausdrucks-Generator** zum Festlegen dieses Arguments zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b17cc-120">You can click the **Build** button to use the **Expression Builder** to set this argument.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b17cc-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b17cc-121">Remarks</span></span>

<span data-ttu-id="b17cc-122">Die **SetReturnVar** -Aktion wird verwendet, um eine **ReturnVar**zu erstellen, die von Makros verwendet werden kann, die ein datenmakro mithilfe der **ausführendatenmakro** -Aktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b17cc-122">The **SetReturnVar** action is used to create a **ReturnVar**, which is variable that can be used by macros that call a data macro by using the **RunDataMacro** action.</span></span> 
  
<span data-ttu-id="b17cc-123">Nachdem ein **ReturnVar** durch die **SetReturnVar** -Aktion erstellt wurde, kann es in einem Ausdruck vom aufrufenden Makro verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b17cc-123">After a **ReturnVar** is created by the **SetReturnVar** action, the calling macro can use it in an expression.</span></span> <span data-ttu-id="b17cc-124">Wenn Sie beispielsweise einen **ReturnVar** mit dem Namen **UpdateSuccess**erstellt haben, können Sie die Variable mithilfe der folgenden Syntax verwenden:</span><span class="sxs-lookup"><span data-stu-id="b17cc-124">For example, if you created a **ReturnVar** named **UpdateSuccess**, you could use the variable by using the following syntax:</span></span>
  
`=[ReturnVars]![UpdateSuccess]`

<span data-ttu-id="b17cc-125">Die **SetReturnVar** -Aktion kann nur in benannten datenmakros verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b17cc-125">The **SetReturnVar** action can be used only in named data macros.</span></span> <span data-ttu-id="b17cc-126">Sie ist in datenmakros, die an ein datenmakro Ereignis angefügt sind, nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b17cc-126">It is not available in data macros that are attached to a data macro event.</span></span> 
  

