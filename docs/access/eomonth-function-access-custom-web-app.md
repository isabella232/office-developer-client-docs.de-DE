---
title: EOMonth-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: df98bcca-152b-49f2-b4e1-35d68008fb8f
description: Gibt den letzten Tag des Monats vor oder die angegebene Anzahl von Monaten zurück.
ms.openlocfilehash: 87a837069be223fdd2f9c809d706782e0955e2aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437455"
---
# <a name="eomonth-function-access-custom-web-app"></a><span data-ttu-id="7121e-103">EOMonth-Funktion (benutzerdefinierte Access-Web-App)</span><span class="sxs-lookup"><span data-stu-id="7121e-103">EOMonth Function (Access custom web app)</span></span>

<span data-ttu-id="7121e-104">Gibt den letzten Tag des Monats vor oder die angegebene Anzahl von Monaten zurück.</span><span class="sxs-lookup"><span data-stu-id="7121e-104">Returns the last day of the month before or specified number of months.</span></span>
  
> [!NOTE]
> <span data-ttu-id="7121e-p101">Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="7121e-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="7121e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7121e-107">Syntax</span></span>

 <span data-ttu-id="7121e-108">**EOMonth** (*Date*, *NumberOfMonth*)</span><span class="sxs-lookup"><span data-stu-id="7121e-108">**EOMonth** (*Date*, *NumberOfMonth*)</span></span> 
  
<span data-ttu-id="7121e-109">**EOMonth** enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="7121e-109">The **EOMonth** contains the following arguments.</span></span> 
  
|<span data-ttu-id="7121e-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="7121e-110">**Argument name**</span></span>|<span data-ttu-id="7121e-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7121e-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="7121e-112">*Date*</span><span class="sxs-lookup"><span data-stu-id="7121e-112">*Date*</span></span>  <br/> |<span data-ttu-id="7121e-113">Das Startdatum im Datums-/Uhrzeitformat oder in einer akzeptierten Textdarstellung eines Datums.</span><span class="sxs-lookup"><span data-stu-id="7121e-113">The start date in Date/Time format, or in an accepted text representation of a date.</span></span>  <br/> |
| <span data-ttu-id="7121e-114">*NumberOfMonth*</span><span class="sxs-lookup"><span data-stu-id="7121e-114">*NumberOfMonth*</span></span>  <br/> |<span data-ttu-id="7121e-115">Eine Zahl, die die Anzahl der Monate vor oder nach dem *Datum darstellt.*</span><span class="sxs-lookup"><span data-stu-id="7121e-115">A number representing the number of months before or after the  *Date*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7121e-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7121e-116">Remarks</span></span>

<span data-ttu-id="7121e-117">Wenn  *Date*  kein gültiges Datum ist, **gibt EOMonth** einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="7121e-117">If  *Date*  is not a valid date, **EOMonth** returns an error.</span></span> 
  
<span data-ttu-id="7121e-118">Wenn  *Date*  plus  *NumberOfMonth*  ein ungültiges Datum ergibt, gibt **EOMonth** einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="7121e-118">If  *Date*  plus  *NumberOfMonth*  yields an invalid date, **EOMonth** returns an error.</span></span> 
  

