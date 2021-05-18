---
title: DatePart-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8936f0b6-f9b2-44ef-bf90-e482b64611cd
description: Gibt einen numerischen Wert zurück, der den angegebenen Datumsteil des angegebenen Datums darstellt.
ms.openlocfilehash: 31ac6423614afd61ed943bb7ba375f14696df1ea
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411435"
---
# <a name="datepart-function-access-custom-web-app"></a><span data-ttu-id="2497c-103">DatePart-Funktion (benutzerdefinierte Access-Web-App)</span><span class="sxs-lookup"><span data-stu-id="2497c-103">DatePart function (Access custom web app)</span></span>

<span data-ttu-id="2497c-104">Gibt einen numerischen Wert zurück, der den angegebenen Datumsteil des angegebenen Datums darstellt.</span><span class="sxs-lookup"><span data-stu-id="2497c-104">Returns a numeric value that represents the specified date part of the specified date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="2497c-p101">Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="2497c-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="2497c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2497c-107">Syntax</span></span>

<span data-ttu-id="2497c-108">**DatePart** (*DatePart*, *Date*)</span><span class="sxs-lookup"><span data-stu-id="2497c-108">**DatePart** (*DatePart*, *Date*)</span></span> 
  
<span data-ttu-id="2497c-109">Die **DatePart-Funktion** enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="2497c-109">The **DatePart** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="2497c-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="2497c-110">**Argument name**</span></span>|<span data-ttu-id="2497c-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2497c-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="2497c-112">*DatePart*</span><span class="sxs-lookup"><span data-stu-id="2497c-112">*DatePart*</span></span>  <br/> |<span data-ttu-id="2497c-113">Der Teil von  *Date*  (ein Datums- oder Uhrzeitwert), für den eine ganze Zahl zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2497c-113">The part of  *Date*  (a date or time value) for which an integer will be returned.</span></span> <span data-ttu-id="2497c-114">Die Liste der gültigen Abkürzungen finden Sie im Abschnitt Hinweise.</span><span class="sxs-lookup"><span data-stu-id="2497c-114">Refer to the Remarks section for the list of valid abbreviations.</span></span>  <br/> |
| <span data-ttu-id="2497c-115">*Date*</span><span class="sxs-lookup"><span data-stu-id="2497c-115">*Date*</span></span>  <br/> |<span data-ttu-id="2497c-p103">Ein Ausdruck, der in einen Datums-/Uhrzeitwert aufgelöst werden kann. Der  *Date*  -Argumentausdruck, Spaltenausdruck, benutzerdefinierte Variable oder Zeichenfolgenliteral.  </span><span class="sxs-lookup"><span data-stu-id="2497c-p103">An expression that can be resolved to a Date/Time value. The  *Date*  argument expression, column expression, user-defined variable or string literal.  </span></span><br/> |
   
## <a name="remarks"></a><span data-ttu-id="2497c-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2497c-118">Remarks</span></span>

<span data-ttu-id="2497c-119">In der folgenden Tabelle werden alle zulässigen  *DatePart*  -Argumente aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="2497c-119">The following table lists all valid  *DatePart*  arguments.</span></span> 
  
|<span data-ttu-id="2497c-120">***DatePart***</span><span class="sxs-lookup"><span data-stu-id="2497c-120">***DatePart***</span></span>|
|:-----|
|<span data-ttu-id="2497c-121">**year**</span><span class="sxs-lookup"><span data-stu-id="2497c-121">**year**</span></span> <br/> |
|<span data-ttu-id="2497c-122">**quarter**</span><span class="sxs-lookup"><span data-stu-id="2497c-122">**quarter**</span></span> <br/> |
|<span data-ttu-id="2497c-123">**month**</span><span class="sxs-lookup"><span data-stu-id="2497c-123">**month**</span></span> <br/> |
|<span data-ttu-id="2497c-124">**dayofyear**</span><span class="sxs-lookup"><span data-stu-id="2497c-124">**dayofyear**</span></span> <br/> |
|<span data-ttu-id="2497c-125">**day**</span><span class="sxs-lookup"><span data-stu-id="2497c-125">**day**</span></span> <br/> |
|<span data-ttu-id="2497c-126">**week**</span><span class="sxs-lookup"><span data-stu-id="2497c-126">**week**</span></span> <br/> |
|<span data-ttu-id="2497c-127">**Weekday**</span><span class="sxs-lookup"><span data-stu-id="2497c-127">**weekday**</span></span> <br/> |
|<span data-ttu-id="2497c-128">**hour**</span><span class="sxs-lookup"><span data-stu-id="2497c-128">**hour**</span></span> <br/> |
|<span data-ttu-id="2497c-129">**minute**</span><span class="sxs-lookup"><span data-stu-id="2497c-129">**minute**</span></span> <br/> |
|<span data-ttu-id="2497c-130">**second**</span><span class="sxs-lookup"><span data-stu-id="2497c-130">**second**</span></span> <br/> |
|<span data-ttu-id="2497c-131">**millisecond**</span><span class="sxs-lookup"><span data-stu-id="2497c-131">**millisecond**</span></span> <br/> |
   

