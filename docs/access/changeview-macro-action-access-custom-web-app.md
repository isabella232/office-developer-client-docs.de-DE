---
title: ChangeView-Makroaktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7eb20f21-0218-4a2c-9bbc-90218a1e87bc
description: Sie können die ChangeView-Aktion verwenden, um zwischen Ansichten zu navigieren.
ms.openlocfilehash: 0c1e27c264a826d38ec2efbd5be9bc6237ad7437
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425358"
---
# <a name="changeview-macro-action-access-custom-web-app"></a><span data-ttu-id="96b38-103">ChangeView-Makroaktion (benutzerdefinierte Access-Web-App)</span><span class="sxs-lookup"><span data-stu-id="96b38-103">ChangeView Macro Action (Access custom web app)</span></span>

<span data-ttu-id="96b38-104">Sie können die **ChangeView** -Aktion verwenden, um zwischen Ansichten zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="96b38-104">You can use the **ChangeView** action to navigate between views in place.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="96b38-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="96b38-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="96b38-107">Einstellung</span><span class="sxs-lookup"><span data-stu-id="96b38-107">Setting</span></span>

<span data-ttu-id="96b38-108">Die **ChangeView** -Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="96b38-108">The **ChangeView** action has the following arguments.</span></span> 
  
|<span data-ttu-id="96b38-109">**Aktionsargument**</span><span class="sxs-lookup"><span data-stu-id="96b38-109">**Action argument**</span></span>|<span data-ttu-id="96b38-110">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="96b38-110">**Required**</span></span>|<span data-ttu-id="96b38-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="96b38-111">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="96b38-112">Tabelle</span><span class="sxs-lookup"><span data-stu-id="96b38-112">Table</span></span>  <br/> |<span data-ttu-id="96b38-113">Ja</span><span class="sxs-lookup"><span data-stu-id="96b38-113">Yes</span></span>  <br/> |<span data-ttu-id="96b38-114">Der Name der zu öffnenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="96b38-114">The name of the table to open.</span></span>  <br/> |
|<span data-ttu-id="96b38-115">Anzeigen</span><span class="sxs-lookup"><span data-stu-id="96b38-115">View</span></span>  <br/> |<span data-ttu-id="96b38-116">Ja</span><span class="sxs-lookup"><span data-stu-id="96b38-116">Yes</span></span>  <br/> |<span data-ttu-id="96b38-117">Der Name der zu öffnenden Ansicht.</span><span class="sxs-lookup"><span data-stu-id="96b38-117">The name of the view to open.</span></span>  <br/> |
|<span data-ttu-id="96b38-118">Dabei gilt:</span><span class="sxs-lookup"><span data-stu-id="96b38-118">Where</span></span>  <br/> |<span data-ttu-id="96b38-119">Nein</span><span class="sxs-lookup"><span data-stu-id="96b38-119">No</span></span>  <br/> |<span data-ttu-id="96b38-120">Ersetzt die WHERE-Bedingung (sofern angegeben) der Objektdatenquelle.</span><span class="sxs-lookup"><span data-stu-id="96b38-120">If specified, replaces the Where condition of the object record source.</span></span>  <br/> |
|<span data-ttu-id="96b38-121">Sortiert nach</span><span class="sxs-lookup"><span data-stu-id="96b38-121">Order By</span></span>  <br/> |<span data-ttu-id="96b38-122">Nein</span><span class="sxs-lookup"><span data-stu-id="96b38-122">No</span></span>  <br/> |<span data-ttu-id="96b38-123">Ein Zeichenfolgenausdruck, der den Namen des Felds oder die Namen der Felder zum Sortieren der Datensätze und die optionalen Schlüsselwörter ASC oder DESC enthält.</span><span class="sxs-lookup"><span data-stu-id="96b38-123">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords.</span></span> <span data-ttu-id="96b38-124">Dieses Argument ist standardmäßig leer.</span><span class="sxs-lookup"><span data-stu-id="96b38-124">By default, this argument is blank.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="96b38-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="96b38-125">Remarks</span></span>

<span data-ttu-id="96b38-126">Alle vom Benutzer angewendeten Sortier-oder Filter Vorgänge werden gelöscht, wenn die **ChangeView** -Aktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="96b38-126">Any sorting or filtering applied by the user is cleared when the **ChangeView** action is called.</span></span> 
  
<span data-ttu-id="96b38-127">Das *OrderBy* -Argument ist der Name der Felder, für die Sie Datensätze sortieren möchten.</span><span class="sxs-lookup"><span data-stu-id="96b38-127">The  *OrderBy*  argument is the name of the field or fields on which you want to sort records.</span></span> <span data-ttu-id="96b38-128">Wenn Sie mehr als einen Feldnamen verwenden, trennen Sie die Namen durch ein Komma (,).</span><span class="sxs-lookup"><span data-stu-id="96b38-128">When you use more than one field name, separate the names with a comma (,).</span></span> 
  
<span data-ttu-id="96b38-129">Wenn Sie das *OrderBy* -Argument festlegen, werden die Datensätze standardmäßig in aufsteigender Reihenfolge sortiert.</span><span class="sxs-lookup"><span data-stu-id="96b38-129">When you set the  *OrderBy*  argument, the records are sorted by default in ascending order.</span></span> 
  

