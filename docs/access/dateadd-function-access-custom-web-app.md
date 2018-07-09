---
title: DateAdd-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7174c585-86e1-42a3-bb7f-d6641001b0f2
description: Addiert zu dem angegebenen Datum die angegebene Anzahl von Intervallen (positive oder negative ganze Zahl) der angegebenen Datumskomponente und gibt das zugehörige Ergebnis zurück.
ms.openlocfilehash: a2baa58a2ccab7d030750d03d4fddb84e8eb8ff7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790217"
---
# <a name="dateadd-function-access-custom-web-app"></a><span data-ttu-id="433d2-103">DateAdd-Funktion (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="433d2-103">DateAdd function (Access custom web app)</span></span>

<span data-ttu-id="433d2-104">Addiert zu dem angegebenen Datum die angegebene Anzahl von Intervallen (positive oder negative ganze Zahl) der angegebenen Datumskomponente und gibt das zugehörige Ergebnis zurück.</span><span class="sxs-lookup"><span data-stu-id="433d2-104">Returns a specified date with the specified number interval (positive or negative integer) added to a specified date part of that date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="433d2-p101">Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="433d2-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="433d2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="433d2-107">Syntax</span></span>

<span data-ttu-id="433d2-108">**DateAdd** (*DatePart*, *Zahl*, *Datum*)</span><span class="sxs-lookup"><span data-stu-id="433d2-108">**DateAdd** (*DatePart*, *Number*, *Date*)</span></span> 
  
<span data-ttu-id="433d2-109">Die **DateAdd** -Funktion enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="433d2-109">The **DateAdd** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="433d2-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="433d2-110">**Argument name**</span></span>|<span data-ttu-id="433d2-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="433d2-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="433d2-112">*DatePart*</span><span class="sxs-lookup"><span data-stu-id="433d2-112">*DatePart*</span></span>  <br/> |<span data-ttu-id="433d2-p102">Die  *Date*  -Komponente, zu der eine ganze Zahl addiert wird. Eine Liste der zulässigen Einstellungen finden Sie im Abschnitt „Hinweise".  </span><span class="sxs-lookup"><span data-stu-id="433d2-p102">The part of  *Date*  to which an integer number is added. Refer to the Remarks section for the list of valid settings.  </span></span><br/> |
| <span data-ttu-id="433d2-115">*Number*</span><span class="sxs-lookup"><span data-stu-id="433d2-115">*Number*</span></span>  <br/> |<span data-ttu-id="433d2-p103">Ist ein Ausdruck, der in eine ganze Zahl aufgelöst werden kann, die zu der  *DatePart*  -Komponente von  *Date*  addiert wird. Wenn Sie einen Wert mit einem Dezimalbruch angeben, wird der Bruch gekürzt.  </span><span class="sxs-lookup"><span data-stu-id="433d2-p103">Is an expression that can be resolved to an integer that is added to a  *DatePart*  of  *Date*  . If you specify a value with a decimal fraction, the fraction is truncated.  </span></span><br/> |
| <span data-ttu-id="433d2-118">*Date*</span><span class="sxs-lookup"><span data-stu-id="433d2-118">*Date*</span></span>  <br/> |<span data-ttu-id="433d2-p104">Ein Ausdruck, der in einen Datums-/Uhrzeitwert aufgelöst werden kann. Der  *Date*  -Argumentausdruck, Spaltenausdruck, benutzerdefinierte Variable oder Zeichenfolgenliteral.  </span><span class="sxs-lookup"><span data-stu-id="433d2-p104">An expression that can be resolved to a Date/Time value. The  *Date*  argument expression, column expression, user-defined variable or string literal.  </span></span><br/> |
   
## <a name="remarks"></a><span data-ttu-id="433d2-121">Remarks</span><span class="sxs-lookup"><span data-stu-id="433d2-121">Remarks</span></span>

<span data-ttu-id="433d2-122">In der folgenden Tabelle werden alle zulässigen  *DatePart*  -Argumente aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="433d2-122">The following table lists all valid  *DatePart*  arguments.</span></span> 
  
|<span data-ttu-id="433d2-123">***DatePart***</span><span class="sxs-lookup"><span data-stu-id="433d2-123">***DatePart***</span></span>|
|:-----|
|<span data-ttu-id="433d2-124">**year**</span><span class="sxs-lookup"><span data-stu-id="433d2-124">**year**</span></span> <br/> |
|<span data-ttu-id="433d2-125">**quarter**</span><span class="sxs-lookup"><span data-stu-id="433d2-125">**quarter**</span></span> <br/> |
|<span data-ttu-id="433d2-126">**month**</span><span class="sxs-lookup"><span data-stu-id="433d2-126">**month**</span></span> <br/> |
|<span data-ttu-id="433d2-127">**dayofyear**</span><span class="sxs-lookup"><span data-stu-id="433d2-127">**dayofyear**</span></span> <br/> |
|<span data-ttu-id="433d2-128">**day**</span><span class="sxs-lookup"><span data-stu-id="433d2-128">**day**</span></span> <br/> |
|<span data-ttu-id="433d2-129">**week**</span><span class="sxs-lookup"><span data-stu-id="433d2-129">**week**</span></span> <br/> |
|<span data-ttu-id="433d2-130">**hour**</span><span class="sxs-lookup"><span data-stu-id="433d2-130">**hour**</span></span> <br/> |
|<span data-ttu-id="433d2-131">**minute**</span><span class="sxs-lookup"><span data-stu-id="433d2-131">**minute**</span></span> <br/> |
|<span data-ttu-id="433d2-132">**second**</span><span class="sxs-lookup"><span data-stu-id="433d2-132">**second**</span></span> <br/> |
|<span data-ttu-id="433d2-133">**millisecond**</span><span class="sxs-lookup"><span data-stu-id="433d2-133">**millisecond**</span></span> <br/> |
   
## <a name="example"></a><span data-ttu-id="433d2-134">Example</span><span class="sxs-lookup"><span data-stu-id="433d2-134">Example</span></span>

<span data-ttu-id="433d2-135">Mit dem folgenden Ausdruck wird der letzte Tag des Monats berechnet.</span><span class="sxs-lookup"><span data-stu-id="433d2-135">The following expression calculates the last day of the current month.</span></span>
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today())+1,0))`

<span data-ttu-id="433d2-136">Mit dem folgenden Ausdruck wird der letzte Tag des vorherigen Monats berechnet.</span><span class="sxs-lookup"><span data-stu-id="433d2-136">The following expression calculates the last day of the previous month.</span></span>
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today()),0))`


