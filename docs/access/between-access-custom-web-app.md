---
title: BeTWEEN (Access Custom Web App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dcb32c6-ed9b-4a09-9e6a-48cc50063a6f
description: Gibt einen zu testenden Test an.
ms.openlocfilehash: fd67d1163f6a39779e0202b5ca1ba998ba8650a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429299"
---
# <a name="between-access-custom-web-app"></a><span data-ttu-id="f026b-103">BeTWEEN (Access Custom Web App)</span><span class="sxs-lookup"><span data-stu-id="f026b-103">BETWEEN (Access custom web app)</span></span>

<span data-ttu-id="f026b-104">Gibt einen zu testenden Test an.</span><span class="sxs-lookup"><span data-stu-id="f026b-104">Specifies a range to test.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="f026b-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="f026b-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f026b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f026b-107">Syntax</span></span>

 <span data-ttu-id="f026b-108">*test_expression*  NICHT **Zwischen** *begin_expression* **Und** *end_expression*</span><span class="sxs-lookup"><span data-stu-id="f026b-108">*test_expression*  [ NOT ] **BETWEEN** *begin_expression* **AND** *end_expression*</span></span> 
  
<span data-ttu-id="f026b-109">Der \*\*\*\* Operator BETWEEN enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="f026b-109">The **Between** operator contains the following arguments.</span></span> 
  
|<span data-ttu-id="f026b-110">**Argument**</span><span class="sxs-lookup"><span data-stu-id="f026b-110">**Argument**</span></span>|<span data-ttu-id="f026b-111">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="f026b-111">**Required**</span></span>|<span data-ttu-id="f026b-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f026b-112">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="f026b-113">*test_expression*</span><span class="sxs-lookup"><span data-stu-id="f026b-113">*test_expression*</span></span>  <br/> |<span data-ttu-id="f026b-114">Ja</span><span class="sxs-lookup"><span data-stu-id="f026b-114">Yes</span></span>  <br/> |<span data-ttu-id="f026b-115">Der Ausdruck, der in dem durch *begin_expression* und *end_expression* definierten Range getestet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f026b-115">The expression to test for in the range defined by  *begin_expression*  and  *end_expression*  .</span></span> <span data-ttu-id="f026b-116">Muss derselbe Datentyp wie *begin_expression* und *end_expression* sein.</span><span class="sxs-lookup"><span data-stu-id="f026b-116">Must be the same data type as both  *begin_expression*  and  *end_expression*  .</span></span>  <br/> |
| <span data-ttu-id="f026b-117">*NOT*</span><span class="sxs-lookup"><span data-stu-id="f026b-117">*NOT*</span></span>  <br/> |<span data-ttu-id="f026b-118">Nein</span><span class="sxs-lookup"><span data-stu-id="f026b-118">No</span></span>  <br/> |<span data-ttu-id="f026b-119">Gibt an, dass das Ergebnis des Prädikats negiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f026b-119">Specifies that the result of the predicate be negated.</span></span>  <br/> |
| <span data-ttu-id="f026b-120">*begin_expression*</span><span class="sxs-lookup"><span data-stu-id="f026b-120">*begin_expression*</span></span>  <br/> |<span data-ttu-id="f026b-121">Ja</span><span class="sxs-lookup"><span data-stu-id="f026b-121">Yes</span></span>  <br/> |<span data-ttu-id="f026b-122">Ein gültiger Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="f026b-122">A valid expression.</span></span> <span data-ttu-id="f026b-123">Muss derselbe Datentyp wie *test_expression* und *end_expression* sein.</span><span class="sxs-lookup"><span data-stu-id="f026b-123">Must be the same data type as both  *test_expression*  and  *end_expression*  .</span></span>  <br/> |
| <span data-ttu-id="f026b-124">*end_expression*</span><span class="sxs-lookup"><span data-stu-id="f026b-124">*end_expression*</span></span>  <br/> |<span data-ttu-id="f026b-125">Ja</span><span class="sxs-lookup"><span data-stu-id="f026b-125">Yes</span></span>  <br/> |<span data-ttu-id="f026b-126">Ein gültiger Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="f026b-126">A valid expression.</span></span> <span data-ttu-id="f026b-127">Muss derselbe Datentyp wie *test_expression* und *begin_expression* sein.</span><span class="sxs-lookup"><span data-stu-id="f026b-127">Must be the same data type as both  *test_expression*  and  *begin_expression*  .</span></span>  <br/> |
| <span data-ttu-id="f026b-128">*AND*</span><span class="sxs-lookup"><span data-stu-id="f026b-128">*AND*</span></span>  <br/> |<span data-ttu-id="f026b-129">Ja</span><span class="sxs-lookup"><span data-stu-id="f026b-129">Yes</span></span>  <br/> |<span data-ttu-id="f026b-130">Gibt an, dass *test_expression* innerhalb des von *begin_expression* und *end_expression* angegebenen Bereich liegen sollte.</span><span class="sxs-lookup"><span data-stu-id="f026b-130">Indicates  *test_expression*  should be within the range indicated by  *begin_expression*  and  *end_expression*  .</span></span>  <br/> |
   
## <a name="result-type"></a><span data-ttu-id="f026b-131">Ergebnistyp</span><span class="sxs-lookup"><span data-stu-id="f026b-131">Result Type</span></span>

 <span data-ttu-id="f026b-132">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="f026b-132">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f026b-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f026b-133">Remarks</span></span>

 <span data-ttu-id="f026b-134">**Zwischen** gibt **true** zurück, wenn der Wert von *test_expression* größer als oder gleich dem Wert von *begin_expression* und kleiner als oder gleich dem Wert von *end_expression* ist.</span><span class="sxs-lookup"><span data-stu-id="f026b-134">**BETWEEN** returns **TRUE** if the value of  *test_expression*  is greater than or equal to the value of  *begin_expression*  and less than or equal to the value of  *end_expression*  .</span></span> 
  
 <span data-ttu-id="f026b-135">**Nicht zwischen** gibt **true** zurück, wenn der Wert von *test_expression* kleiner als der Wert von *begin_expression* oder größer als der Wert von *end_expression* ist.</span><span class="sxs-lookup"><span data-stu-id="f026b-135">**NOT BETWEEN** returns **TRUE** if the value of  *test_expression*  is less than the value of  *begin_expression*  or greater than the value of  *end_expression*  .</span></span> 
  
<span data-ttu-id="f026b-136">Um einen exklusiven Range anzugeben, verwenden Sie den Wert größer\>als () und kleiner als\<Operatoren ().</span><span class="sxs-lookup"><span data-stu-id="f026b-136">To specify an exclusive range, use the greater than (\>) and less than operators (\<).</span></span>
  

