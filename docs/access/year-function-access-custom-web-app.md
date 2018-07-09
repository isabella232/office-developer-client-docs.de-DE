---
title: Year-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a70751eb-bfde-4f7d-ad90-a1e4cca25dbc
description: Gibt einen numerischen Wert, der das Jahr des angegebenen Datums im gregorianischen Kalender darstellt.
ms.openlocfilehash: f9d72343637734257a2ed9589e5539b845933826
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790387"
---
# <a name="year-function-access-custom-web-app"></a><span data-ttu-id="478be-103">Year-Funktion (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="478be-103">Year Function (Access custom web app)</span></span>

<span data-ttu-id="478be-104">Gibt einen numerischen Wert, der das Jahr des angegebenen Datums im gregorianischen Kalender darstellt.</span><span class="sxs-lookup"><span data-stu-id="478be-104">Returns a numeric value that represents the year of the specified date in the Gregorian calendar.</span></span>
  
> [!NOTE]
> <span data-ttu-id="478be-p101">Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="478be-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="478be-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="478be-107">Syntax</span></span>

 <span data-ttu-id="478be-108">**Jahr** (*Datum*)</span><span class="sxs-lookup"><span data-stu-id="478be-108">**Year** (*Date*)</span></span> 
  
<span data-ttu-id="478be-109">Die **Year** -Funktion enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="478be-109">The **Year** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="478be-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="478be-110">**Argument name**</span></span>|<span data-ttu-id="478be-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="478be-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="478be-112">*Date*</span><span class="sxs-lookup"><span data-stu-id="478be-112">*Date*</span></span>  <br/> |<span data-ttu-id="478be-p102">Ein Ausdruck, der in einen Datums-/Uhrzeitwert aufgelöst werden kann. Der  *Date*  -Argumentausdruck, Spaltenausdruck, benutzerdefinierte Variable oder Zeichenfolgenliteral.  </span><span class="sxs-lookup"><span data-stu-id="478be-p102">An expression that can be resolved to a Date/Time value. The  *Date*  argument expression, column expression, user-defined variable or string literal.  </span></span><br/> |
   
## <a name="remarks"></a><span data-ttu-id="478be-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="478be-115">Remarks</span></span>

<span data-ttu-id="478be-116">Von den Funktionen **Jahr**, **Monat**und **Tag** zurückgegebenen Werte werden Gregorianische Werte das Anzeigeformat für den angegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="478be-116">Values returned by the **Year**, **Month**, and **Day** functions will be Gregorian values regardless of the display format for the supplied date value.</span></span> <span data-ttu-id="478be-117">Wenn das Anzeigeformat für das angegebene Datum verwendet, der Hijri-Kalender, die zurückgegebenen Werte für das **Jahr**, **Monat**und **Tag** -Funktionen wird werden beispielsweise Werte zugeordnet, mit dem entsprechenden gregorianischen Datum.</span><span class="sxs-lookup"><span data-stu-id="478be-117">For example, if the display format of the supplied date uses the Hijri calendar, the returned values for the **Year**, **Month**, and **Day** functions will be values associated with the equivalent Gregorian date.</span></span> 
  

