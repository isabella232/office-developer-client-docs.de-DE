---
title: ZWISCHEN (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dcb32c6-ed9b-4a09-9e6a-48cc50063a6f
description: Gibt einen Bereich zu testen.
ms.openlocfilehash: 0ef3384d6a29826968220f8d6cfc0d2f85e1131c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790203"
---
# <a name="between-access-custom-web-app"></a><span data-ttu-id="9c8f2-103">ZWISCHEN (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="9c8f2-103">BETWEEN (Access custom web app)</span></span>

<span data-ttu-id="9c8f2-104">Gibt einen Bereich zu testen.</span><span class="sxs-lookup"><span data-stu-id="9c8f2-104">Specifies a range to test.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="9c8f2-p101">[!WICHTIG] Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="9c8f2-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9c8f2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c8f2-107">Syntax</span></span>

 <span data-ttu-id="9c8f2-108">*test_expression*  [NOT] **BETWEEN** *begin_expression* **Und** *end_expression*</span><span class="sxs-lookup"><span data-stu-id="9c8f2-108">*test_expression*  [ NOT ] **BETWEEN** *begin_expression* **AND** *end_expression*</span></span> 
  
<span data-ttu-id="9c8f2-109">Der Operator **zwischen** enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="9c8f2-109">The **Between** operator contains the following arguments.</span></span> 
  
|<span data-ttu-id="9c8f2-110">**Argument**</span><span class="sxs-lookup"><span data-stu-id="9c8f2-110">**Argument**</span></span>|<span data-ttu-id="9c8f2-111">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="9c8f2-111">**Required**</span></span>|<span data-ttu-id="9c8f2-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9c8f2-112">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="9c8f2-113">*test_expression*</span><span class="sxs-lookup"><span data-stu-id="9c8f2-113">*test_expression*</span></span>  <br/> |<span data-ttu-id="9c8f2-114">Ja</span><span class="sxs-lookup"><span data-stu-id="9c8f2-114">Yes</span></span>  <br/> |<span data-ttu-id="9c8f2-115">Der Ausdruck, der im Bereich von *Begin_expression* und *End_expression* definierten testen.</span><span class="sxs-lookup"><span data-stu-id="9c8f2-115">The expression to test for in the range defined by  *begin_expression*  and  *end_expression*  .</span></span> <span data-ttu-id="9c8f2-116">Muss denselben Datentyp aufweisen wie *Begin_expression* und *End_expression* .</span><span class="sxs-lookup"><span data-stu-id="9c8f2-116">Must be the same data type as both  *begin_expression*  and  *end_expression*  .</span></span>  <br/> |
| <span data-ttu-id="9c8f2-117">*NOT*</span><span class="sxs-lookup"><span data-stu-id="9c8f2-117">*NOT*</span></span>  <br/> |<span data-ttu-id="9c8f2-118">Nein</span><span class="sxs-lookup"><span data-stu-id="9c8f2-118">No</span></span>  <br/> |<span data-ttu-id="9c8f2-119">Gibt an, dass das Ergebnis des Prädikats negiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9c8f2-119">Specifies that the result of the predicate be negated.</span></span>  <br/> |
| <span data-ttu-id="9c8f2-120">*begin_expression*</span><span class="sxs-lookup"><span data-stu-id="9c8f2-120">*begin_expression*</span></span>  <br/> |<span data-ttu-id="9c8f2-121">Ja</span><span class="sxs-lookup"><span data-stu-id="9c8f2-121">Yes</span></span>  <br/> |<span data-ttu-id="9c8f2-122">Ein gültiger Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="9c8f2-122">A valid expression.</span></span> <span data-ttu-id="9c8f2-123">Muss denselben Datentyp aufweisen wie *Test_expression* und *End_expression* .</span><span class="sxs-lookup"><span data-stu-id="9c8f2-123">Must be the same data type as both  *test_expression*  and  *end_expression*  .</span></span>  <br/> |
| <span data-ttu-id="9c8f2-124">*end_expression*</span><span class="sxs-lookup"><span data-stu-id="9c8f2-124">*end_expression*</span></span>  <br/> |<span data-ttu-id="9c8f2-125">Ja</span><span class="sxs-lookup"><span data-stu-id="9c8f2-125">Yes</span></span>  <br/> |<span data-ttu-id="9c8f2-126">Ein gültiger Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="9c8f2-126">A valid expression.</span></span> <span data-ttu-id="9c8f2-127">Denselben Datentyp aufweisen wie *Test_expression* und *Begin_expression* muss sein.</span><span class="sxs-lookup"><span data-stu-id="9c8f2-127">Must be the same data type as both  *test_expression*  and  *begin_expression*  .</span></span>  <br/> |
| <span data-ttu-id="9c8f2-128">*AND*</span><span class="sxs-lookup"><span data-stu-id="9c8f2-128">*AND*</span></span>  <br/> |<span data-ttu-id="9c8f2-129">Ja</span><span class="sxs-lookup"><span data-stu-id="9c8f2-129">Yes</span></span>  <br/> |<span data-ttu-id="9c8f2-130">Gibt an, dass *Test_expression* innerhalb des Bereichs von *Begin_expression* und *End_expression* angegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="9c8f2-130">Indicates  *test_expression*  should be within the range indicated by  *begin_expression*  and  *end_expression*  .</span></span>  <br/> |
   
## <a name="result-type"></a><span data-ttu-id="9c8f2-131">Ergebnistyp</span><span class="sxs-lookup"><span data-stu-id="9c8f2-131">Result Type</span></span>

 <span data-ttu-id="9c8f2-132">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="9c8f2-132">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9c8f2-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9c8f2-133">Remarks</span></span>

 <span data-ttu-id="9c8f2-134">**BETWEEN** gibt **TRUE** zurück, wenn der Wert von *Test_expression* größer als oder gleich dem Wert von *Begin_expression* ist kleiner oder gleich dem Wert von *End_expression* .</span><span class="sxs-lookup"><span data-stu-id="9c8f2-134">**BETWEEN** returns **TRUE** if the value of  *test_expression*  is greater than or equal to the value of  *begin_expression*  and less than or equal to the value of  *end_expression*  .</span></span> 
  
 <span data-ttu-id="9c8f2-135">**Nicht zwischen** zurückgegeben **TRUE** , wenn der Wert von *Test_expression* kleiner als der Wert von *Begin_expression* oder größer als der Wert von *End_expression* ist.</span><span class="sxs-lookup"><span data-stu-id="9c8f2-135">**NOT BETWEEN** returns **TRUE** if the value of  *test_expression*  is less than the value of  *begin_expression*  or greater than the value of  *end_expression*  .</span></span> 
  
<span data-ttu-id="9c8f2-136">Verwenden Sie zum Angeben eines Bereichs, der größer als (\>) und kleiner als Operatoren (\<).</span><span class="sxs-lookup"><span data-stu-id="9c8f2-136">To specify an exclusive range, use the greater than (\>) and less than operators (\<).</span></span>
  

