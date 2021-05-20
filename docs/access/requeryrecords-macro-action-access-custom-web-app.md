---
title: RequeryRecords-Makroaktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1dab102f-24af-4984-8020-a9fb06355639
description: Sie können die RequeryRecords-Aktion verwenden, um die Daten in der aktiven Ansicht zu aktualisieren, zu sortieren und zu filtern, indem Sie die Quelle der Ansicht erneut anzeigen.
ms.openlocfilehash: 69d88401abc0de417f7dc58e275c66f2037212aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439247"
---
# <a name="requeryrecords-macro-action-access-custom-web-app"></a><span data-ttu-id="1647d-103">RequeryRecords-Makroaktion (benutzerdefinierte Access-Web-App)</span><span class="sxs-lookup"><span data-stu-id="1647d-103">RequeryRecords Macro Action (Access custom web app)</span></span>

<span data-ttu-id="1647d-104">Sie können die **RequeryRecords-Aktion** verwenden, um die Daten in der aktiven Ansicht zu aktualisieren, zu sortieren und zu filtern, indem Sie die Quelle der Ansicht erneut anzeigen.</span><span class="sxs-lookup"><span data-stu-id="1647d-104">You can use the **RequeryRecords** action to refresh, sort, and filter the data in the active view by requerying the source of the view.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="1647d-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="1647d-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="1647d-107">Einstellung</span><span class="sxs-lookup"><span data-stu-id="1647d-107">Setting</span></span>

<span data-ttu-id="1647d-108">Die **RequeryRecords-Aktion** hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="1647d-108">The **RequeryRecords** action has the following arguments.</span></span> 
  
|<span data-ttu-id="1647d-109">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="1647d-109">**Parameter**</span></span>|<span data-ttu-id="1647d-110">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="1647d-110">**Required**</span></span>|<span data-ttu-id="1647d-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1647d-111">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1647d-112">**Where=**</span><span class="sxs-lookup"><span data-stu-id="1647d-112">**Where=**</span></span> <br/> |<span data-ttu-id="1647d-113">Nein</span><span class="sxs-lookup"><span data-stu-id="1647d-113">No</span></span>  <br/> |<span data-ttu-id="1647d-114">Eine SQL WHERE-Klausel, die die Datensätze in der Ansicht einschränkt.</span><span class="sxs-lookup"><span data-stu-id="1647d-114">A SQL WHERE clause that restricts the records in the view.</span></span> <span data-ttu-id="1647d-115">Standardmäßig ist dieses Argument leer.</span><span class="sxs-lookup"><span data-stu-id="1647d-115">By default, this argument is blank.</span></span>  <br/> |
|<span data-ttu-id="1647d-116">**OrderBy**</span><span class="sxs-lookup"><span data-stu-id="1647d-116">**OrderBy**</span></span> <br/> |<span data-ttu-id="1647d-117">Nein</span><span class="sxs-lookup"><span data-stu-id="1647d-117">No</span></span>  <br/> |<span data-ttu-id="1647d-118">Ein Zeichenfolgenausdruck, der den Namen des Felds oder die Namen der Felder zum Sortieren der Datensätze und die optionalen Schlüsselwörter ASC oder DESC enthält.</span><span class="sxs-lookup"><span data-stu-id="1647d-118">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords.</span></span> <span data-ttu-id="1647d-119">Standardmäßig ist dieses Argument leer.</span><span class="sxs-lookup"><span data-stu-id="1647d-119">By default, this argument is blank.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1647d-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1647d-120">Remarks</span></span>

<span data-ttu-id="1647d-121">Alle vom Benutzer angewendeten Sortierungen oder Filterungen werden beim Aufgerufen der **RequeryRecords-Aktion** geleert.</span><span class="sxs-lookup"><span data-stu-id="1647d-121">Any sorting or filtering applied by the user is cleared when the **RequeryRecords** action is called.</span></span> 
  
<span data-ttu-id="1647d-122">Das  *OrderBy-Argument*  ist der Name des Felds oder der Felder, nach denen Sie Datensätze sortieren möchten.</span><span class="sxs-lookup"><span data-stu-id="1647d-122">The  *OrderBy*  argument is the name of the field or fields on which you want to sort records.</span></span> <span data-ttu-id="1647d-123">Wenn Sie mehr als einen Feldnamen verwenden, trennen Sie die Namen durch ein Komma (,).</span><span class="sxs-lookup"><span data-stu-id="1647d-123">When you use more than one field name, separate the names with a comma (,).</span></span> 
  
<span data-ttu-id="1647d-124">Wenn Sie das  *Argument OrderBy*  festlegen, werden die Datensätze standardmäßig in aufsteigender Reihenfolge sortiert.</span><span class="sxs-lookup"><span data-stu-id="1647d-124">When you set the  *OrderBy*  argument, the records are sorted by default in ascending order.</span></span> 
  
<span data-ttu-id="1647d-125">Um Datensätze in absteigender Reihenfolge zu sortieren, geben Sie DESC am Ende des  *OrderBy-Argumentausdrucks*  ein.</span><span class="sxs-lookup"><span data-stu-id="1647d-125">To sort records in descending order, enter DESC at the end of the  *OrderBy*  argument expression.</span></span> <span data-ttu-id="1647d-126">Wenn Sie z. B. Kundendatensätze in absteigender Reihenfolge nach Kontaktnamen sortieren möchten, legen Sie das  *Argument OrderBy*  auf "ContactName DESC" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1647d-126">For example, to sort customer records in descending order by contact name, set the  *OrderBy*  argument to "ContactName DESC".</span></span> 
  
<span data-ttu-id="1647d-127">Zum Sortieren von Namen nach dem absteigenden LastName und dem aufsteigenden FirstName-Argument legen Sie  *das OrderBy-Argument*  auf "LastName DESC, FirstName ASC" ein.</span><span class="sxs-lookup"><span data-stu-id="1647d-127">To sort names by LastName descending, and FirstName ascending, set the  *OrderBy*  argument to "LastName DESC, FirstName ASC".</span></span> 
  

