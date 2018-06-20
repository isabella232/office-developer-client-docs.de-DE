---
title: DatePart-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8936f0b6-f9b2-44ef-bf90-e482b64611cd
description: Gibt einen numerischen Wert, der den angegebenen Datumsteil des angegebenen Datums darstellt.
ms.openlocfilehash: 81aa1880e5b38c33f75018418a44ed82e5e7e8c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790173"
---
# <a name="datepart-function-access-custom-web-app"></a><span data-ttu-id="d2f41-103">DatePart-Funktion (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="d2f41-103">DatePart function (Access custom web app)</span></span>

<span data-ttu-id="d2f41-104">Gibt einen numerischen Wert, der den angegebenen Datumsteil des angegebenen Datums darstellt.</span><span class="sxs-lookup"><span data-stu-id="d2f41-104">Returns a numeric value that represents the specified date part of the specified date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="d2f41-p101">[!HINWEIS] Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="d2f41-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d2f41-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2f41-107">Syntax</span></span>

<span data-ttu-id="d2f41-108">**DatePart** (*DatePart*, *Datum*)</span><span class="sxs-lookup"><span data-stu-id="d2f41-108">**DatePart** (*DatePart*, *Date*)</span></span> 
  
<span data-ttu-id="d2f41-109">Die **DatePart** -Funktion enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="d2f41-109">The **DatePart** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="d2f41-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="d2f41-110">**Argument name**</span></span>|<span data-ttu-id="d2f41-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="d2f41-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="d2f41-112">*DatePart*</span><span class="sxs-lookup"><span data-stu-id="d2f41-112">*DatePart*</span></span>  <br/> |<span data-ttu-id="d2f41-113">Der Teil des *Datum* (einen Datums- oder Zeitwerte-Wert) für die eine ganze Zahl zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d2f41-113">The part of  *Date*  (a date or time value) for which an integer will be returned.</span></span> <span data-ttu-id="d2f41-114">Finden Sie im Abschnitt "Hinweise" für die Liste der zulässigen Werte.</span><span class="sxs-lookup"><span data-stu-id="d2f41-114">Refer to the Remarks section for the list of valid abbreviations.</span></span>  <br/> |
| <span data-ttu-id="d2f41-115">*Date*</span><span class="sxs-lookup"><span data-stu-id="d2f41-115">*Date*</span></span>  <br/> |<span data-ttu-id="d2f41-p103">Ein Ausdruck, der in einen Datums-/Uhrzeitwert aufgelöst werden kann. Der  *Date*  -Argumentausdruck, Spaltenausdruck, benutzerdefinierte Variable oder Zeichenfolgenliteral.  </span><span class="sxs-lookup"><span data-stu-id="d2f41-p103">An expression that can be resolved to a Date/Time value. The  *Date*  argument expression, column expression, user-defined variable or string literal.  </span></span><br/> |
   
## <a name="remarks"></a><span data-ttu-id="d2f41-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="d2f41-118">Remarks</span></span>

<span data-ttu-id="d2f41-119">In der folgenden Tabelle werden alle zulässigen  *DatePart*  -Argumente aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d2f41-119">The following table lists all valid  *DatePart*  arguments.</span></span> 
  
|<span data-ttu-id="d2f41-120">***DatePart***</span><span class="sxs-lookup"><span data-stu-id="d2f41-120">***DatePart***</span></span>|
|:-----|
|<span data-ttu-id="d2f41-121">**year**</span><span class="sxs-lookup"><span data-stu-id="d2f41-121">**year**</span></span> <br/> |
|<span data-ttu-id="d2f41-122">**quarter**</span><span class="sxs-lookup"><span data-stu-id="d2f41-122">**quarter**</span></span> <br/> |
|<span data-ttu-id="d2f41-123">**month**</span><span class="sxs-lookup"><span data-stu-id="d2f41-123">**month**</span></span> <br/> |
|<span data-ttu-id="d2f41-124">**dayofyear**</span><span class="sxs-lookup"><span data-stu-id="d2f41-124">**dayofyear**</span></span> <br/> |
|<span data-ttu-id="d2f41-125">**day**</span><span class="sxs-lookup"><span data-stu-id="d2f41-125">**day**</span></span> <br/> |
|<span data-ttu-id="d2f41-126">**week**</span><span class="sxs-lookup"><span data-stu-id="d2f41-126">**week**</span></span> <br/> |
|<span data-ttu-id="d2f41-127">**Weekday**</span><span class="sxs-lookup"><span data-stu-id="d2f41-127">**weekday**</span></span> <br/> |
|<span data-ttu-id="d2f41-128">**hour**</span><span class="sxs-lookup"><span data-stu-id="d2f41-128">**hour**</span></span> <br/> |
|<span data-ttu-id="d2f41-129">**minute**</span><span class="sxs-lookup"><span data-stu-id="d2f41-129">**minute**</span></span> <br/> |
|<span data-ttu-id="d2f41-130">**second**</span><span class="sxs-lookup"><span data-stu-id="d2f41-130">**second**</span></span> <br/> |
|<span data-ttu-id="d2f41-131">**millisecond**</span><span class="sxs-lookup"><span data-stu-id="d2f41-131">**millisecond**</span></span> <br/> |
   

