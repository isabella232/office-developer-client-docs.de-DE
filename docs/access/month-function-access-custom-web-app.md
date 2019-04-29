---
title: Month-Funktion (Access Custom Web App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5df43594-a434-4fb7-8109-e5cf0401ae09
description: Gibt eine ganze Zahl zurück, die den Monat des angegebenen Datums darstellt.
ms.openlocfilehash: 0ca7059a2fd6dad1f9790ad6f4eafe7affa014dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411491"
---
# <a name="month-function-access-custom-web-app"></a><span data-ttu-id="bf6ab-103">Month-Funktion (Access Custom Web App)</span><span class="sxs-lookup"><span data-stu-id="bf6ab-103">Month Function (Access custom web app)</span></span>

<span data-ttu-id="bf6ab-104">Gibt eine ganze Zahl zurück, die den Monat des angegebenen Datums darstellt.</span><span class="sxs-lookup"><span data-stu-id="bf6ab-104">Returns an integer that represents the month of the specified date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="bf6ab-p101">Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="bf6ab-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="bf6ab-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf6ab-107">Syntax</span></span>

 <span data-ttu-id="bf6ab-108">**Month** (*Datum*)</span><span class="sxs-lookup"><span data-stu-id="bf6ab-108">**Month** (*Date*)</span></span> 
  
<span data-ttu-id="bf6ab-109">Die **Month** -Funktion enthält das folgende Argument.</span><span class="sxs-lookup"><span data-stu-id="bf6ab-109">The **Month** function contains the following argument.</span></span> 
  
|<span data-ttu-id="bf6ab-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="bf6ab-110">**Argument name**</span></span>|<span data-ttu-id="bf6ab-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bf6ab-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="bf6ab-112">*Date*</span><span class="sxs-lookup"><span data-stu-id="bf6ab-112">*Date*</span></span>  <br/> |<span data-ttu-id="bf6ab-113">Ein Ausdruck, der in einen Datums-/Uhrzeitwert aufgelöst werden kann.</span><span class="sxs-lookup"><span data-stu-id="bf6ab-113">An expression that can be resolved to a Date/Time value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bf6ab-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bf6ab-114">Remarks</span></span>

 <span data-ttu-id="bf6ab-115">**Month** gibt den gleichen Wert wie **datepart** (month, Date) zurück.</span><span class="sxs-lookup"><span data-stu-id="bf6ab-115">**Month** returns the same value as **DatePart** (month, date).</span></span> 
  
<span data-ttu-id="bf6ab-116">Wenn *Date* nur einen Zeit Teil enthält, ist der Rückgabewert 1, der Basis Monat.</span><span class="sxs-lookup"><span data-stu-id="bf6ab-116">If  *Date*  contains only a time part, the return value is 1, the base month.</span></span> 
  

