---
title: FestlegenEigenschaft-Makroaktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1e97dd95-23f6-4f49-b3b9-2c7261b3a70d
description: Die FestlegenEigenschaft-Aktion können Sie eine Eigenschaft für ein Steuerelement in einer Ansicht festgelegt.
ms.openlocfilehash: 89ac2b10715d707d3b6ee09ee8ab915384c5acf5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790352"
---
# <a name="setproperty-macro-action-access-custom-web-app"></a><span data-ttu-id="7fffd-103">FestlegenEigenschaft-Makroaktion (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="7fffd-103">SetProperty Macro Action (Access custom web app)</span></span>

<span data-ttu-id="7fffd-104">Die **FestlegenEigenschaft** -Aktion können Sie eine Eigenschaft für ein Steuerelement in einer Ansicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7fffd-104">You can use the **SetProperty** action to set a property for a control on a view.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="7fffd-p101">[!WICHTIG] Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="7fffd-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="7fffd-107">Einstellung</span><span class="sxs-lookup"><span data-stu-id="7fffd-107">Setting</span></span>

<span data-ttu-id="7fffd-108">Die **FestlegenEigenschaft** -Aktion hat die Argumente in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="7fffd-108">The **SetProperty** action has the arguments listed in the following table.</span></span> 
  
|<span data-ttu-id="7fffd-109">**Aktionsargument**</span><span class="sxs-lookup"><span data-stu-id="7fffd-109">**Action argument**</span></span>|<span data-ttu-id="7fffd-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7fffd-110">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="7fffd-111">_Steuerelementname_</span><span class="sxs-lookup"><span data-stu-id="7fffd-111">_Control Name_</span></span> <br/> |<span data-ttu-id="7fffd-112">Geben Sie den Namen des Felds oder der Steuerung für den Wert der Eigenschaft festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7fffd-112">Type the name of the field or control for which you want to set the property value.</span></span> <span data-ttu-id="7fffd-113">Lassen Sie dieses Argument leer, um die-Eigenschaft für die Ansicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7fffd-113">Leave this argument blank to set the property for the view.</span></span>  <br/> |
| <span data-ttu-id="7fffd-114">_Eigenschaft_</span><span class="sxs-lookup"><span data-stu-id="7fffd-114">_Property_</span></span> <br/> |<span data-ttu-id="7fffd-115">Wählen Sie die Eigenschaft, die Sie festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="7fffd-115">Select the property that you want to set.</span></span> <span data-ttu-id="7fffd-116">Finden Sie im Abschnitt **"Hinweise"** in diesem Artikel finden Sie eine Liste der Eigenschaften, die mithilfe dieser Aktion festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="7fffd-116">See the **Remarks** section in this article for a list of the properties that can be set by using this action.</span></span>  <br/> |
| <span data-ttu-id="7fffd-117">_Wert_</span><span class="sxs-lookup"><span data-stu-id="7fffd-117">_Value_</span></span> <br/> |<span data-ttu-id="7fffd-118">Geben Sie den Wert, der die Eigenschaft festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7fffd-118">Type the value that the property is to be set to.</span></span> <span data-ttu-id="7fffd-119">Für Eigenschaften, deren Werte sind entweder Ja oder Nein, verwenden Sie **-1** für Ja, und **0** für Nein.</span><span class="sxs-lookup"><span data-stu-id="7fffd-119">For properties whose values are either Yes or No, use **-1** for Yes and **0** for No.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7fffd-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7fffd-120">Remarks</span></span>

<span data-ttu-id="7fffd-121">Die **FestlegenEigenschaft** -Aktion können Sie die folgenden Eigenschaften eines Steuerelements festlegen:</span><span class="sxs-lookup"><span data-stu-id="7fffd-121">You can use the **SetProperty** action to set the following properties of a control:</span></span> 
  
- <span data-ttu-id="7fffd-122">Caption</span><span class="sxs-lookup"><span data-stu-id="7fffd-122">Caption</span></span>
    
- <span data-ttu-id="7fffd-123">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="7fffd-123">Enabled</span></span>
    
- <span data-ttu-id="7fffd-124">ForeColor-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7fffd-124">ForeColor</span></span>
    
- <span data-ttu-id="7fffd-125">Wert</span><span class="sxs-lookup"><span data-stu-id="7fffd-125">Value</span></span>
    
- <span data-ttu-id="7fffd-126">Visible</span><span class="sxs-lookup"><span data-stu-id="7fffd-126">Visible</span></span>
    
<span data-ttu-id="7fffd-127">Wenn Sie einen ungültigen Wert für das Argument ** *Wert* ** eingeben, tritt kein Fehler auf. Allerdings kann es passieren, dass Access die Eigenschaft in einen anderen Wert ändert. Dies hängt davon ab, wie das Argument interpretiert wird.</span><span class="sxs-lookup"><span data-stu-id="7fffd-127">If you enter an invalid value for the ** *Value* ** argument, no error occurs, but Access might change the property to a different value, depending on how it interprets the argument.</span></span> 
  

