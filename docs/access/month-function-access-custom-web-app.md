---
title: Month-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5df43594-a434-4fb7-8109-e5cf0401ae09
description: Gibt eine ganze Zahl, die den Monat des angegebenen Datums darstellt.
ms.openlocfilehash: 5e4a583a5a299456e57b90d7cef41a32b0a6ffba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790336"
---
# <a name="month-function-access-custom-web-app"></a><span data-ttu-id="8feba-103">Month-Funktion (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="8feba-103">Month Function (Access custom web app)</span></span>

<span data-ttu-id="8feba-104">Gibt eine ganze Zahl, die den Monat des angegebenen Datums darstellt.</span><span class="sxs-lookup"><span data-stu-id="8feba-104">Returns an integer that represents the month of the specified date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="8feba-p101"> Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="8feba-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8feba-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8feba-107">Syntax</span></span>

 <span data-ttu-id="8feba-108">**Monat** (*Datum*)</span><span class="sxs-lookup"><span data-stu-id="8feba-108">**Month** (*Date*)</span></span> 
  
<span data-ttu-id="8feba-109">**Month** -Funktion enthält das folgende Argument.</span><span class="sxs-lookup"><span data-stu-id="8feba-109">The **Month** function contains the following argument.</span></span> 
  
|<span data-ttu-id="8feba-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="8feba-110">**Argument name**</span></span>|<span data-ttu-id="8feba-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="8feba-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="8feba-112">*Date*</span><span class="sxs-lookup"><span data-stu-id="8feba-112">*Date*</span></span>  <br/> |<span data-ttu-id="8feba-113">Ein Ausdruck, der in einen Datums-/Uhrzeitwert aufgelöst werden kann.</span><span class="sxs-lookup"><span data-stu-id="8feba-113">An expression that can be resolved to a Date/Time value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8feba-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8feba-114">Remarks</span></span>

 <span data-ttu-id="8feba-115">**Monat** gibt den gleichen Wert wie **DatePart** (Monat, Datum) zurück.</span><span class="sxs-lookup"><span data-stu-id="8feba-115">**Month** returns the same value as **DatePart** (month, date).</span></span> 
  
<span data-ttu-id="8feba-116">Wenn *Datum* nur einen Teil einer Uhrzeit enthält, ist der Rückgabewert 1, der Basis Monat.</span><span class="sxs-lookup"><span data-stu-id="8feba-116">If  *Date*  contains only a time part, the return value is 1, the base month.</span></span> 
  

