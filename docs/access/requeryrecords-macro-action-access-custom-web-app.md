---
title: RequeryRecords-Makroaktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1dab102f-24af-4984-8020-a9fb06355639
description: Sie können die RequeryRecords-Aktion verwenden, aktualisieren, Sortieren und Filtern der Daten in der aktiven Ansicht durch erneutes Abfragen der Quelle der Ansicht.
ms.openlocfilehash: 27c6a4f62f62f6d903de7a23d2aca6db8d316a84
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790347"
---
# <a name="requeryrecords-macro-action-access-custom-web-app"></a><span data-ttu-id="23c78-103">RequeryRecords-Makroaktion (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="23c78-103">RequeryRecords Macro Action (Access custom web app)</span></span>

<span data-ttu-id="23c78-104">Sie können die **RequeryRecords** -Aktion verwenden, aktualisieren, Sortieren und Filtern der Daten in der aktiven Ansicht durch erneutes Abfragen der Quelle der Ansicht.</span><span class="sxs-lookup"><span data-stu-id="23c78-104">You can use the **RequeryRecords** action to refresh, sort, and filter the data in the active view by requerying the source of the view.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="23c78-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="23c78-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="23c78-107">Einstellung</span><span class="sxs-lookup"><span data-stu-id="23c78-107">Setting</span></span>

<span data-ttu-id="23c78-108">Die **RequeryRecords** -Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="23c78-108">The **RequeryRecords** action has the following arguments.</span></span> 
  
|<span data-ttu-id="23c78-109">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="23c78-109">**Parameter**</span></span>|<span data-ttu-id="23c78-110">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="23c78-110">**Required**</span></span>|<span data-ttu-id="23c78-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="23c78-111">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="23c78-112">**Wobei =**</span><span class="sxs-lookup"><span data-stu-id="23c78-112">**Where=**</span></span> <br/> |<span data-ttu-id="23c78-113">Nein</span><span class="sxs-lookup"><span data-stu-id="23c78-113">No</span></span>  <br/> |<span data-ttu-id="23c78-114">Eine SQL WHERE-Klausel, die die Datensätze in der Ansicht beschränkt.</span><span class="sxs-lookup"><span data-stu-id="23c78-114">A SQL WHERE clause that restricts the records in the view.</span></span> <span data-ttu-id="23c78-115">Standardmäßig ist dieses Argument leer.</span><span class="sxs-lookup"><span data-stu-id="23c78-115">By default, this argument is blank.</span></span>  <br/> |
|<span data-ttu-id="23c78-116">**OrderBy**</span><span class="sxs-lookup"><span data-stu-id="23c78-116">**OrderBy**</span></span> <br/> |<span data-ttu-id="23c78-117">Nein</span><span class="sxs-lookup"><span data-stu-id="23c78-117">No</span></span>  <br/> |<span data-ttu-id="23c78-118">Ein Zeichenfolgenausdruck, der den Namen des Felds oder der Felder, nach dem oder denen Datensätze sortiert werden sollen, sowie die optionalen ASC- oder DESC-Schlüsselwörter enthält.</span><span class="sxs-lookup"><span data-stu-id="23c78-118">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords.</span></span> <span data-ttu-id="23c78-119">Standardmäßig ist dieses Argument leer.</span><span class="sxs-lookup"><span data-stu-id="23c78-119">By default, this argument is blank.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="23c78-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="23c78-120">Remarks</span></span>

<span data-ttu-id="23c78-121">Beim Sortieren oder Filtern durch den Benutzer angewendet wird gelöscht, wenn die Aktion **RequeryRecords** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="23c78-121">Any sorting or filtering applied by the user is cleared when the **RequeryRecords** action is called.</span></span> 
  
<span data-ttu-id="23c78-122">Das Argument *OrderBy* ist der Name des Felds oder der Felder, auf denen Datensätze sortiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="23c78-122">The  *OrderBy*  argument is the name of the field or fields on which you want to sort records.</span></span> <span data-ttu-id="23c78-123">Wenn Sie mehr als einen Feldnamen verwenden, trennen Sie die Namen durch ein Komma (,).</span><span class="sxs-lookup"><span data-stu-id="23c78-123">When you use more than one field name, separate the names with a comma (,).</span></span> 
  
<span data-ttu-id="23c78-124">Wenn Sie das Argument *OrderBy* festlegen, werden die Datensätze standardmäßig in aufsteigender Reihenfolge sortiert.</span><span class="sxs-lookup"><span data-stu-id="23c78-124">When you set the  *OrderBy*  argument, the records are sorted by default in ascending order.</span></span> 
  
<span data-ttu-id="23c78-125">Geben Sie DESC am Ende des Ausdrucks-Argument *OrderBy* , um Datensätze in absteigender Reihenfolge zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="23c78-125">To sort records in descending order, enter DESC at the end of the  *OrderBy*  argument expression.</span></span> <span data-ttu-id="23c78-126">Legen Sie beispielsweise Kundendatensätze in absteigender Reihenfolge nach dem Namen des Kontakts, um das Argument *OrderBy* "ContactName DESC".</span><span class="sxs-lookup"><span data-stu-id="23c78-126">For example, to sort customer records in descending order by contact name, set the  *OrderBy*  argument to "ContactName DESC".</span></span> 
  
<span data-ttu-id="23c78-127">Um die Namen von absteigender LastName und FirstName Aufsteigend sortieren, legen Sie das Argument *OrderBy* auf "DESC LastName, FirstName ASC".</span><span class="sxs-lookup"><span data-stu-id="23c78-127">To sort names by LastName descending, and FirstName ascending, set the  *OrderBy*  argument to "LastName DESC, FirstName ASC".</span></span> 
  

