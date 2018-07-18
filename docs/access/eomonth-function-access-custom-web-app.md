---
title: EOMonth-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: df98bcca-152b-49f2-b4e1-35d68008fb8f
description: Gibt den letzten Tag im Monat vor oder eine bestimmte Anzahl von Monaten zurück.
ms.openlocfilehash: cee42c4e5cb3a24b2e702673238ac9ee09bc7372
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790182"
---
# <a name="eomonth-function-access-custom-web-app"></a><span data-ttu-id="7d825-103">EOMonth-Funktion (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="7d825-103">EOMonth Function (Access custom web app)</span></span>

<span data-ttu-id="7d825-104">Gibt den letzten Tag im Monat vor oder eine bestimmte Anzahl von Monaten zurück.</span><span class="sxs-lookup"><span data-stu-id="7d825-104">Returns the last day of the month before or specified number of months.</span></span>
  
> [!NOTE]
> <span data-ttu-id="7d825-p101">[!HINWEIS] Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="7d825-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="7d825-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d825-107">Syntax</span></span>

 <span data-ttu-id="7d825-108">**EOMonth** (*Datum*, *NumberOfMonth*)</span><span class="sxs-lookup"><span data-stu-id="7d825-108">**EOMonth** (*Date*, *NumberOfMonth*)</span></span> 
  
<span data-ttu-id="7d825-109">Die **EOMonth** enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="7d825-109">The **EOMonth** contains the following arguments.</span></span> 
  
|<span data-ttu-id="7d825-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="7d825-110">**Argument name**</span></span>|<span data-ttu-id="7d825-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="7d825-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="7d825-112">*Date*</span><span class="sxs-lookup"><span data-stu-id="7d825-112">*Date*</span></span>  <br/> |<span data-ttu-id="7d825-113">Das Startdatum in Datums-/Uhrzeitformat oder in einer akzeptierten Textdarstellung eines Datums.</span><span class="sxs-lookup"><span data-stu-id="7d825-113">The start date in Date/Time format, or in an accepted text representation of a date.</span></span>  <br/> |
| <span data-ttu-id="7d825-114">*NumberOfMonth*</span><span class="sxs-lookup"><span data-stu-id="7d825-114">*NumberOfMonth*</span></span>  <br/> |<span data-ttu-id="7d825-115">Eine Zahl, die die Anzahl der Monate vor oder nach dem *Datum* darstellt.</span><span class="sxs-lookup"><span data-stu-id="7d825-115">A number representing the number of months before or after the  *Date*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7d825-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7d825-116">Remarks</span></span>

<span data-ttu-id="7d825-117">Wenn *Datum* kein gültiges Datum vorliegt, gibt **EOMonth** einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="7d825-117">If  *Date*  is not a valid date, **EOMonth** returns an error.</span></span> 
  
<span data-ttu-id="7d825-118">Wenn *Datum* plus *NumberOfMonth* versatztage ein ungültiges Datum, gibt **EOMonth** einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="7d825-118">If  *Date*  plus  *NumberOfMonth*  yields an invalid date, **EOMonth** returns an error.</span></span> 
  

