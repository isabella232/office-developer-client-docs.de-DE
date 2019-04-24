---
title: EOMonth-Funktion (Access Custom Web App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: df98bcca-152b-49f2-b4e1-35d68008fb8f
description: Gibt den letzten Tag des Monats vor oder angegebene Anzahl von Monaten zurück.
ms.openlocfilehash: 87a837069be223fdd2f9c809d706782e0955e2aa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302560"
---
# <a name="eomonth-function-access-custom-web-app"></a><span data-ttu-id="14769-103">EOMonth-Funktion (Access Custom Web App)</span><span class="sxs-lookup"><span data-stu-id="14769-103">EOMonth Function (Access custom web app)</span></span>

<span data-ttu-id="14769-104">Gibt den letzten Tag des Monats vor oder angegebene Anzahl von Monaten zurück.</span><span class="sxs-lookup"><span data-stu-id="14769-104">Returns the last day of the month before or specified number of months.</span></span>
  
> [!NOTE]
> <span data-ttu-id="14769-p101">Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="14769-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="14769-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="14769-107">Syntax</span></span>

 <span data-ttu-id="14769-108">**EOMonth** (*Datum*, *NumberOfMonth*)</span><span class="sxs-lookup"><span data-stu-id="14769-108">**EOMonth** (*Date*, *NumberOfMonth*)</span></span> 
  
<span data-ttu-id="14769-109">Die **EOMonth** enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="14769-109">The **EOMonth** contains the following arguments.</span></span> 
  
|<span data-ttu-id="14769-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="14769-110">**Argument name**</span></span>|<span data-ttu-id="14769-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="14769-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="14769-112">*Date*</span><span class="sxs-lookup"><span data-stu-id="14769-112">*Date*</span></span>  <br/> |<span data-ttu-id="14769-113">Das Startdatum im Datum/Uhrzeit-Format oder in einer akzeptierten Textdarstellung eines Datums.</span><span class="sxs-lookup"><span data-stu-id="14769-113">The start date in Date/Time format, or in an accepted text representation of a date.</span></span>  <br/> |
| <span data-ttu-id="14769-114">*NumberOfMonth*</span><span class="sxs-lookup"><span data-stu-id="14769-114">*NumberOfMonth*</span></span>  <br/> |<span data-ttu-id="14769-115">Eine Zahl, die die Anzahl der Monate vor oder nach dem *Datum* darstellt.</span><span class="sxs-lookup"><span data-stu-id="14769-115">A number representing the number of months before or after the  *Date*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="14769-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="14769-116">Remarks</span></span>

<span data-ttu-id="14769-117">Wenn *Date* kein gültiges Datum ist, gibt **EOMonth** einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="14769-117">If  *Date*  is not a valid date, **EOMonth** returns an error.</span></span> 
  
<span data-ttu-id="14769-118">Wenn *Date* Plus *NumberOfMonth* ein ungültiges Datum ergibt, gibt **EOMonth** einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="14769-118">If  *Date*  plus  *NumberOfMonth*  yields an invalid date, **EOMonth** returns an error.</span></span> 
  

