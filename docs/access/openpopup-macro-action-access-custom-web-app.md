---
title: OpenPopup-Makroaktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 850de802-e417-4884-8d14-571de52aa391
description: Öffnet die angegebene Ansicht in einem Popupfenster.
ms.openlocfilehash: 01e0086dc0b54837cf5f095ec6ac5701b5b0b219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790329"
---
# <a name="openpopup-macro-action-access-custom-web-app"></a><span data-ttu-id="3b7d5-103">OpenPopup-Makroaktion (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="3b7d5-103">OpenPopup Macro Action (Access custom web app)</span></span>

<span data-ttu-id="3b7d5-104">Öffnet die angegebene Ansicht in einem Popupfenster.</span><span class="sxs-lookup"><span data-stu-id="3b7d5-104">Opens the specified view in a popup window.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="3b7d5-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/de-de/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="3b7d5-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/de-de/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3b7d5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b7d5-107">Syntax</span></span>

 <span data-ttu-id="3b7d5-108">**OpenPopup** (*Anzeigen*, *, in dem =*, *der Order By*)</span><span class="sxs-lookup"><span data-stu-id="3b7d5-108">**OpenPopup** (*View*, *Where=*, *Order By*)</span></span> 
  
<span data-ttu-id="3b7d5-109">Die **OpenPopup** -Aktion enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="3b7d5-109">The **OpenPopup** action contains the following arguments.</span></span> 
  
|<span data-ttu-id="3b7d5-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="3b7d5-110">**Argument name**</span></span>|<span data-ttu-id="3b7d5-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="3b7d5-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="3b7d5-112">*View*</span><span class="sxs-lookup"><span data-stu-id="3b7d5-112">*View*</span></span>  <br/> |<span data-ttu-id="3b7d5-113">Der Name der Ansicht zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3b7d5-113">The name of the view to open.</span></span>  <br/> |
| <span data-ttu-id="3b7d5-114">*Wobei =*</span><span class="sxs-lookup"><span data-stu-id="3b7d5-114">*Where=*</span></span>  <br/> |<span data-ttu-id="3b7d5-115">Eine gültige SQL WHERE-Klausel (ohne das Wort, in dem), die die Datensätze in der Ansicht beschränkt.</span><span class="sxs-lookup"><span data-stu-id="3b7d5-115">A valid SQL WHERE clause (without the word WHERE) that restricts the records in the view.</span></span>  <br/> |
| <span data-ttu-id="3b7d5-116">*Sortiert nach*</span><span class="sxs-lookup"><span data-stu-id="3b7d5-116">*Order By*</span></span>  <br/> |<span data-ttu-id="3b7d5-117">Ein Zeichenfolgenausdruck, der den Namen des Felds oder der Felder, nach dem oder denen Datensätze sortiert werden sollen, sowie die optionalen ASC- oder DESC-Schlüsselwörter enthält.</span><span class="sxs-lookup"><span data-stu-id="3b7d5-117">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords.</span></span> <span data-ttu-id="3b7d5-118">Standardmäßig ist dieses Argument leer.</span><span class="sxs-lookup"><span data-stu-id="3b7d5-118">By default, this argument is blank.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3b7d5-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3b7d5-119">Remarks</span></span>

<span data-ttu-id="3b7d5-120">Das aktuelle Makro beendet, sobald die Aktion **OpenPopup** verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="3b7d5-120">The current macro ends once the **OpenPopup** action is processed.</span></span> 
  
<span data-ttu-id="3b7d5-121">Beim Sortieren oder Filtern durch den Benutzer angewendet wird gelöscht, wenn die Aktion **OpenPopup** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3b7d5-121">Any sorting or filtering applied by the user is cleared when the **OpenPopup** action is called.</span></span> 
  
<span data-ttu-id="3b7d5-122">Das Argument *OrderBy* ist der Name des Felds oder der Felder, auf denen Datensätze sortiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3b7d5-122">The  *OrderBy*  argument is the name of the field or fields on which you want to sort records.</span></span> <span data-ttu-id="3b7d5-123">Wenn Sie mehr als einen Feldnamen verwenden, trennen Sie die Namen durch ein Komma (,).</span><span class="sxs-lookup"><span data-stu-id="3b7d5-123">When you use more than one field name, separate the names with a comma (,).</span></span> 
  
<span data-ttu-id="3b7d5-124">Wenn Sie das Argument *OrderBy* festlegen, werden die Datensätze standardmäßig in aufsteigender Reihenfolge sortiert.</span><span class="sxs-lookup"><span data-stu-id="3b7d5-124">When you set the  *OrderBy*  argument, the records are sorted by default in ascending order.</span></span> 
  

