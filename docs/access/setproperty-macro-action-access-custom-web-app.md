---
title: SetProperty-Makroaktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1e97dd95-23f6-4f49-b3b9-2c7261b3a70d
description: Mit der SetProperty-Aktion können Sie eine Eigenschaft für ein Steuerelement in einer Ansicht festlegen.
ms.openlocfilehash: 1876be32606d66e0570c9e69206a508b8888b157
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438029"
---
# <a name="setproperty-macro-action-access-custom-web-app"></a><span data-ttu-id="54610-103">SetProperty-Makroaktion (benutzerdefinierte Access-Web-App)</span><span class="sxs-lookup"><span data-stu-id="54610-103">SetProperty Macro Action (Access custom web app)</span></span>

<span data-ttu-id="54610-104">Mit der **SetProperty-Aktion** können Sie eine Eigenschaft für ein Steuerelement in einer Ansicht festlegen.</span><span class="sxs-lookup"><span data-stu-id="54610-104">You can use the **SetProperty** action to set a property for a control on a view.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="54610-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="54610-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="54610-107">Einstellung</span><span class="sxs-lookup"><span data-stu-id="54610-107">Setting</span></span>

<span data-ttu-id="54610-108">Die **SetProperty-Aktion** enthält die In der folgenden Tabelle aufgeführten Argumente.</span><span class="sxs-lookup"><span data-stu-id="54610-108">The **SetProperty** action has the arguments listed in the following table.</span></span> 
  
|<span data-ttu-id="54610-109">**Aktionsargument**</span><span class="sxs-lookup"><span data-stu-id="54610-109">**Action argument**</span></span>|<span data-ttu-id="54610-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="54610-110">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="54610-111">_Steuerelementname_</span><span class="sxs-lookup"><span data-stu-id="54610-111">_Control Name_</span></span> <br/> |<span data-ttu-id="54610-112">Geben Sie den Namen des Felds oder Steuerelements ein, für das Sie den Eigenschaftswert festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="54610-112">Type the name of the field or control for which you want to set the property value.</span></span> <span data-ttu-id="54610-113">Lassen Sie dieses Argument leer, um die Eigenschaft für die Ansicht festlegen.</span><span class="sxs-lookup"><span data-stu-id="54610-113">Leave this argument blank to set the property for the view.</span></span>  <br/> |
| <span data-ttu-id="54610-114">_Eigenschaft_</span><span class="sxs-lookup"><span data-stu-id="54610-114">_Property_</span></span> <br/> |<span data-ttu-id="54610-p103">Wählen Sie die Eigenschaft aus, die Sie festlegen möchten. Der Abschnitt **Hinweise** in diesem Artikel enthält eine Auflistung der Eigenschaften, die mithilfe dieser Aktion festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="54610-p103">Select the property that you want to set. See the **Remarks** section in this article for a list of the properties that can be set by using this action.  </span></span><br/> |
| <span data-ttu-id="54610-117">_Wert_</span><span class="sxs-lookup"><span data-stu-id="54610-117">_Value_</span></span> <br/> |<span data-ttu-id="54610-118">Geben Sie den Wert ein, auf den die Eigenschaft festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="54610-118">Type the value that the property is to be set to.</span></span> <span data-ttu-id="54610-119">Verwenden Sie für Eigenschaften, deren Werte entweder Ja oder Nein sind, **-1** für Ja und **0 für** Nein.</span><span class="sxs-lookup"><span data-stu-id="54610-119">For properties whose values are either Yes or No, use **-1** for Yes and **0** for No.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="54610-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="54610-120">Remarks</span></span>

<span data-ttu-id="54610-121">Mit der **SetProperty-Aktion** können Sie die folgenden Eigenschaften eines Steuerelements festlegen:</span><span class="sxs-lookup"><span data-stu-id="54610-121">You can use the **SetProperty** action to set the following properties of a control:</span></span> 
  
- <span data-ttu-id="54610-122">Beschriftung</span><span class="sxs-lookup"><span data-stu-id="54610-122">Caption</span></span>
    
- <span data-ttu-id="54610-123">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="54610-123">Enabled</span></span>
    
- <span data-ttu-id="54610-124">ForeColor</span><span class="sxs-lookup"><span data-stu-id="54610-124">ForeColor</span></span>
    
- <span data-ttu-id="54610-125">Wert</span><span class="sxs-lookup"><span data-stu-id="54610-125">Value</span></span>
    
- <span data-ttu-id="54610-126">Visible</span><span class="sxs-lookup"><span data-stu-id="54610-126">Visible</span></span>
    
<span data-ttu-id="54610-127">Wenn Sie einen ungültigen Wert für das Argument \*\* *Wert* \*\* eingeben, tritt kein Fehler auf. Allerdings kann es passieren, dass Access die Eigenschaft in einen anderen Wert ändert. Dies hängt davon ab, wie das Argument interpretiert wird.</span><span class="sxs-lookup"><span data-stu-id="54610-127">If you enter an invalid value for the \*\* *Value* \*\* argument, no error occurs, but Access might change the property to a different value, depending on how it interprets the argument.</span></span> 
  

