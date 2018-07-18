---
title: ChangeView-Makroaktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7eb20f21-0218-4a2c-9bbc-90218a1e87bc
description: Die ChangeView-Aktion können Sie um zwischen Ansichten direkt zu navigieren.
ms.openlocfilehash: c420846074ef362d3388d40ed8700db0739b7ce0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790208"
---
# <a name="changeview-macro-action-access-custom-web-app"></a><span data-ttu-id="f84f7-103">ChangeView-Makroaktion (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="f84f7-103">ChangeView Macro Action (Access custom web app)</span></span>

<span data-ttu-id="f84f7-104">Die **ChangeView** -Aktion können Sie um zwischen Ansichten direkt zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="f84f7-104">You can use the **ChangeView** action to navigate between views in place.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="f84f7-p101">[!WICHTIG] Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="f84f7-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="f84f7-107">Einstellung</span><span class="sxs-lookup"><span data-stu-id="f84f7-107">Setting</span></span>

<span data-ttu-id="f84f7-108">Die **ChangeView** -Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="f84f7-108">The **ChangeView** action has the following arguments.</span></span> 
  
|<span data-ttu-id="f84f7-109">**Aktionsargument**</span><span class="sxs-lookup"><span data-stu-id="f84f7-109">**Action argument**</span></span>|<span data-ttu-id="f84f7-110">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="f84f7-110">**Required**</span></span>|<span data-ttu-id="f84f7-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f84f7-111">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f84f7-112">Tabelle</span><span class="sxs-lookup"><span data-stu-id="f84f7-112">Table</span></span>  <br/> |<span data-ttu-id="f84f7-113">Ja</span><span class="sxs-lookup"><span data-stu-id="f84f7-113">Yes</span></span>  <br/> |<span data-ttu-id="f84f7-114">Der Name der zu öffnenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="f84f7-114">The name of the table to open.</span></span>  <br/> |
|<span data-ttu-id="f84f7-115">Ansicht</span><span class="sxs-lookup"><span data-stu-id="f84f7-115">View</span></span>  <br/> |<span data-ttu-id="f84f7-116">Ja</span><span class="sxs-lookup"><span data-stu-id="f84f7-116">Yes</span></span>  <br/> |<span data-ttu-id="f84f7-117">Der Name der Ansicht zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f84f7-117">The name of the view to open.</span></span>  <br/> |
|<span data-ttu-id="f84f7-118">Wobei</span><span class="sxs-lookup"><span data-stu-id="f84f7-118">Where</span></span>  <br/> |<span data-ttu-id="f84f7-119">Nein</span><span class="sxs-lookup"><span data-stu-id="f84f7-119">No</span></span>  <br/> |<span data-ttu-id="f84f7-120">Ersetzt, wenn angegeben, die Bedingung der Datensatzquelle des Objekts.</span><span class="sxs-lookup"><span data-stu-id="f84f7-120">If specified, replaces the Where condition of the object record source.</span></span>  <br/> |
|<span data-ttu-id="f84f7-121">Sortiert nach</span><span class="sxs-lookup"><span data-stu-id="f84f7-121">Order By</span></span>  <br/> |<span data-ttu-id="f84f7-122">Nein</span><span class="sxs-lookup"><span data-stu-id="f84f7-122">No</span></span>  <br/> |<span data-ttu-id="f84f7-123">Ein Zeichenfolgenausdruck, der den Namen des Felds oder der Felder, nach dem oder denen Datensätze sortiert werden sollen, sowie die optionalen ASC- oder DESC-Schlüsselwörter enthält.</span><span class="sxs-lookup"><span data-stu-id="f84f7-123">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords.</span></span> <span data-ttu-id="f84f7-124">Standardmäßig ist dieses Argument leer.</span><span class="sxs-lookup"><span data-stu-id="f84f7-124">By default, this argument is blank.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f84f7-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f84f7-125">Remarks</span></span>

<span data-ttu-id="f84f7-126">Beim Sortieren oder Filtern durch den Benutzer angewendet wird gelöscht, wenn die Aktion **ChangeView** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f84f7-126">Any sorting or filtering applied by the user is cleared when the **ChangeView** action is called.</span></span> 
  
<span data-ttu-id="f84f7-127">Das Argument *OrderBy* ist der Name des Felds oder der Felder, auf denen Datensätze sortiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f84f7-127">The  *OrderBy*  argument is the name of the field or fields on which you want to sort records.</span></span> <span data-ttu-id="f84f7-128">Wenn Sie mehr als einen Feldnamen verwenden, trennen Sie die Namen durch ein Komma (,).</span><span class="sxs-lookup"><span data-stu-id="f84f7-128">When you use more than one field name, separate the names with a comma (,).</span></span> 
  
<span data-ttu-id="f84f7-129">Wenn Sie das Argument *OrderBy* festlegen, werden die Datensätze standardmäßig in aufsteigender Reihenfolge sortiert.</span><span class="sxs-lookup"><span data-stu-id="f84f7-129">When you set the  *OrderBy*  argument, the records are sorted by default in ascending order.</span></span> 
  

