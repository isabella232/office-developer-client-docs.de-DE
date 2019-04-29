---
title: OpenPopup-Makroaktion (Access Custom Web App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 850de802-e417-4884-8d14-571de52aa391
description: Öffnet die angegebene Ansicht in einem Popupfenster.
ms.openlocfilehash: 2a8b67fcbf31c42f13b36f06d14d9d046be68c68
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427388"
---
# <a name="openpopup-macro-action-access-custom-web-app"></a><span data-ttu-id="6fe47-103">OpenPopup-Makroaktion (Access Custom Web App)</span><span class="sxs-lookup"><span data-stu-id="6fe47-103">OpenPopup Macro Action (Access custom web app)</span></span>

<span data-ttu-id="6fe47-104">Öffnet die angegebene Ansicht in einem Popupfenster.</span><span class="sxs-lookup"><span data-stu-id="6fe47-104">Opens the specified view in a popup window.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="6fe47-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="6fe47-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6fe47-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6fe47-107">Syntax</span></span>

 <span data-ttu-id="6fe47-108">**Openpopup** (*View*, *Where =*, *Order by*)</span><span class="sxs-lookup"><span data-stu-id="6fe47-108">**OpenPopup** (*View*, *Where=*, *Order By*)</span></span> 
  
<span data-ttu-id="6fe47-109">Die **openpopup** -Aktion enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="6fe47-109">The **OpenPopup** action contains the following arguments.</span></span> 
  
|<span data-ttu-id="6fe47-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="6fe47-110">**Argument name**</span></span>|<span data-ttu-id="6fe47-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6fe47-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="6fe47-112">*View*</span><span class="sxs-lookup"><span data-stu-id="6fe47-112">*View*</span></span>  <br/> |<span data-ttu-id="6fe47-113">Der Name der zu öffnenden Ansicht.</span><span class="sxs-lookup"><span data-stu-id="6fe47-113">The name of the view to open.</span></span>  <br/> |
| <span data-ttu-id="6fe47-114">*WHERE =*</span><span class="sxs-lookup"><span data-stu-id="6fe47-114">*Where=*</span></span>  <br/> |<span data-ttu-id="6fe47-115">Eine gültige SQL-WHERE-Klausel (ohne das Wort WHERE), die die Datensätze in der Ansicht einschränkt.</span><span class="sxs-lookup"><span data-stu-id="6fe47-115">A valid SQL WHERE clause (without the word WHERE) that restricts the records in the view.</span></span>  <br/> |
| <span data-ttu-id="6fe47-116">*Sortiert nach*</span><span class="sxs-lookup"><span data-stu-id="6fe47-116">*Order By*</span></span>  <br/> |<span data-ttu-id="6fe47-117">Ein Zeichenfolgenausdruck, der den Namen des Felds oder der Felder, nach dem oder denen Datensätze sortiert werden sollen, sowie die optionalen ASC- oder DESC-Schlüsselwörter enthält.</span><span class="sxs-lookup"><span data-stu-id="6fe47-117">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords.</span></span> <span data-ttu-id="6fe47-118">Dieses Argument ist standardmäßig leer.</span><span class="sxs-lookup"><span data-stu-id="6fe47-118">By default, this argument is blank.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6fe47-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6fe47-119">Remarks</span></span>

<span data-ttu-id="6fe47-120">Das aktuelle Makro endet, nachdem \*\*\*\* die openpopup-Aktion verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="6fe47-120">The current macro ends once the **OpenPopup** action is processed.</span></span> 
  
<span data-ttu-id="6fe47-121">Alle vom Benutzer angewendeten Sortier-oder Filter Vorgänge werden gelöscht \*\*\*\* , wenn die openpopup-Aktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6fe47-121">Any sorting or filtering applied by the user is cleared when the **OpenPopup** action is called.</span></span> 
  
<span data-ttu-id="6fe47-122">Das *OrderBy* -Argument ist der Name der Felder, für die Sie Datensätze sortieren möchten.</span><span class="sxs-lookup"><span data-stu-id="6fe47-122">The  *OrderBy*  argument is the name of the field or fields on which you want to sort records.</span></span> <span data-ttu-id="6fe47-123">Wenn Sie mehr als einen Feldnamen verwenden, trennen Sie die Namen durch ein Komma (,).</span><span class="sxs-lookup"><span data-stu-id="6fe47-123">When you use more than one field name, separate the names with a comma (,).</span></span> 
  
<span data-ttu-id="6fe47-124">Wenn Sie das *OrderBy* -Argument festlegen, werden die Datensätze standardmäßig in aufsteigender Reihenfolge sortiert.</span><span class="sxs-lookup"><span data-stu-id="6fe47-124">When you set the  *OrderBy*  argument, the records are sorted by default in ascending order.</span></span> 
  

