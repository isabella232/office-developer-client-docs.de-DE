---
title: DateDiff-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1c58ee87-0f57-4643-be4d-62da815df705
description: Gibt die Anzahl der angegebenen Datum Teil Grenzen zwischen dem angegebenen Startdatum und Enddatum überschritten.
ms.openlocfilehash: fe898ec5eb59cb341250cb0c0e2e35bc55d37eb3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790215"
---
# <a name="datediff-function-access-custom-web-app"></a><span data-ttu-id="a83e6-103">DateDiff-Funktion (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="a83e6-103">DateDiff function (Access custom web app)</span></span>

<span data-ttu-id="a83e6-104">Gibt die Anzahl der angegebenen Datum Teil Grenzen zwischen dem angegebenen Startdatum und Enddatum überschritten.</span><span class="sxs-lookup"><span data-stu-id="a83e6-104">Returns the count of the specified date part boundaries crossed between the specified start date and end date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a83e6-p101"> Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="a83e6-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a83e6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a83e6-107">Syntax</span></span>

<span data-ttu-id="a83e6-108">**DateDiff** (*DatePart*, *StartDate*, *EndDate*)</span><span class="sxs-lookup"><span data-stu-id="a83e6-108">**DateDiff** (*DatePart*, *StartDate*, *EndDate*)</span></span> 
  
<span data-ttu-id="a83e6-109">Die **DateDiff** -Funktion enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="a83e6-109">The **DateDiff** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="a83e6-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="a83e6-110">**Argument name**</span></span>|<span data-ttu-id="a83e6-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="a83e6-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="a83e6-112">*DatePart*</span><span class="sxs-lookup"><span data-stu-id="a83e6-112">*DatePart*</span></span>  <br/> |<span data-ttu-id="a83e6-113">Ist der Teil des *StartDate* und *EndDate* , der den Typ des Grenze überschritten angibt.</span><span class="sxs-lookup"><span data-stu-id="a83e6-113">Is the part of  *StartDate*  and  *EndDate*  that specifies the type of boundary crossed.</span></span> <span data-ttu-id="a83e6-114">Eine Liste der zulässigen Einstellungen finden Sie im Abschnitt „Hinweise".</span><span class="sxs-lookup"><span data-stu-id="a83e6-114">Refer to the Remarks section for the list of valid settings.</span></span>  <br/> |
| <span data-ttu-id="a83e6-115">*StartDate*</span><span class="sxs-lookup"><span data-stu-id="a83e6-115">*StartDate*</span></span>  <br/> |<span data-ttu-id="a83e6-p103">Ein Ausdruck, der in einen Datums-/Uhrzeitwert aufgelöst werden kann. Der  *Date*  -Argumentausdruck, Spaltenausdruck, benutzerdefinierte Variable oder Zeichenfolgenliteral.  </span><span class="sxs-lookup"><span data-stu-id="a83e6-p103">An expression that can be resolved to a Date/Time value. The  *Date*  argument expression, column expression, user-defined variable or string literal.  </span></span><br/> |
| <span data-ttu-id="a83e6-118">*EndDate*</span><span class="sxs-lookup"><span data-stu-id="a83e6-118">*EndDate*</span></span>  <br/> |<span data-ttu-id="a83e6-p104">Ein Ausdruck, der in einen Datums-/Uhrzeitwert aufgelöst werden kann. Der  *Date*  -Argumentausdruck, Spaltenausdruck, benutzerdefinierte Variable oder Zeichenfolgenliteral.  </span><span class="sxs-lookup"><span data-stu-id="a83e6-p104">An expression that can be resolved to a Date/Time value. The  *Date*  argument expression, column expression, user-defined variable or string literal.  </span></span><br/> |
   
## <a name="remarks"></a><span data-ttu-id="a83e6-121">Remarks</span><span class="sxs-lookup"><span data-stu-id="a83e6-121">Remarks</span></span>

<span data-ttu-id="a83e6-122">In der folgenden Tabelle werden alle zulässigen  *DatePart*  -Argumente aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="a83e6-122">The following table lists all valid  *DatePart*  arguments.</span></span> 
  
|<span data-ttu-id="a83e6-123">***DatePart***</span><span class="sxs-lookup"><span data-stu-id="a83e6-123">***DatePart***</span></span>|
|:-----|
|<span data-ttu-id="a83e6-124">**year**</span><span class="sxs-lookup"><span data-stu-id="a83e6-124">**year**</span></span> <br/> |
|<span data-ttu-id="a83e6-125">**quarter**</span><span class="sxs-lookup"><span data-stu-id="a83e6-125">**quarter**</span></span> <br/> |
|<span data-ttu-id="a83e6-126">**month**</span><span class="sxs-lookup"><span data-stu-id="a83e6-126">**month**</span></span> <br/> |
|<span data-ttu-id="a83e6-127">**dayofyear**</span><span class="sxs-lookup"><span data-stu-id="a83e6-127">**dayofyear**</span></span> <br/> |
|<span data-ttu-id="a83e6-128">**day**</span><span class="sxs-lookup"><span data-stu-id="a83e6-128">**day**</span></span> <br/> |
|<span data-ttu-id="a83e6-129">**week**</span><span class="sxs-lookup"><span data-stu-id="a83e6-129">**week**</span></span> <br/> |
|<span data-ttu-id="a83e6-130">**hour**</span><span class="sxs-lookup"><span data-stu-id="a83e6-130">**hour**</span></span> <br/> |
|<span data-ttu-id="a83e6-131">**minute**</span><span class="sxs-lookup"><span data-stu-id="a83e6-131">**minute**</span></span> <br/> |
|<span data-ttu-id="a83e6-132">**second**</span><span class="sxs-lookup"><span data-stu-id="a83e6-132">**second**</span></span> <br/> |
|<span data-ttu-id="a83e6-133">**millisecond**</span><span class="sxs-lookup"><span data-stu-id="a83e6-133">**millisecond**</span></span> <br/> |
   

