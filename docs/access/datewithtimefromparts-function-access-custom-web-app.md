---
title: DateWithTimeFromParts-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: aa97cbaa-8b14-42e3-a098-938ebe0769eb
description: Gibt ein Datum und einen Zeitraum basierend auf einer angegebenen Jahr, Monat, Tag und Uhrzeit.
ms.openlocfilehash: 8cc1fbe700d18c04d944793bcea889424b0cff3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790161"
---
# <a name="datewithtimefromparts-function-access-custom-web-app"></a><span data-ttu-id="88a9b-103">DateWithTimeFromParts-Funktion (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="88a9b-103">DateWithTimeFromParts function (Access custom web app)</span></span>

<span data-ttu-id="88a9b-104">Gibt ein Datum und einen Zeitraum basierend auf einer angegebenen Jahr, Monat, Tag und Uhrzeit.</span><span class="sxs-lookup"><span data-stu-id="88a9b-104">Returns a Date and Time based on a specified year, month, day, and time.</span></span>
  
> [!NOTE]
> <span data-ttu-id="88a9b-p101">[!HINWEIS] Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="88a9b-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="88a9b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="88a9b-107">Syntax</span></span>

<span data-ttu-id="88a9b-108">**DateWithTimeFromParts** (*Jahr*, *Monat*, *Tag*, *Stunde*, *Minute*, *Sekunde*)</span><span class="sxs-lookup"><span data-stu-id="88a9b-108">**DateWithTimeFromParts** (*Year*, *Month*, *Day*, *Hour*, *Minute*, *Second*)</span></span> 
  
<span data-ttu-id="88a9b-109">Die **DateWithTimeFromParts** -Funktion enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="88a9b-109">The **DateWithTimeFromParts** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="88a9b-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="88a9b-110">**Argument name**</span></span>|<span data-ttu-id="88a9b-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="88a9b-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="88a9b-112">*Jahr*</span><span class="sxs-lookup"><span data-stu-id="88a9b-112">*Year*</span></span>  <br/> |<span data-ttu-id="88a9b-113">Ein Ausdruck, der ganze Zahl, die einem Jahr angibt.</span><span class="sxs-lookup"><span data-stu-id="88a9b-113">Integer expression specifying a year.</span></span>  <br/> |
| <span data-ttu-id="88a9b-114">*Month*</span><span class="sxs-lookup"><span data-stu-id="88a9b-114">*Month*</span></span>  <br/> |<span data-ttu-id="88a9b-115">Ein Ausdruck, der ganze Zahl, die einen Monat angibt.</span><span class="sxs-lookup"><span data-stu-id="88a9b-115">Integer expression specifying a month.</span></span>  <br/> |
| <span data-ttu-id="88a9b-116">*Tag*</span><span class="sxs-lookup"><span data-stu-id="88a9b-116">*Day*</span></span>  <br/> |<span data-ttu-id="88a9b-117">Ein Ausdruck, der ganze Zahl, die einen Tag angibt.</span><span class="sxs-lookup"><span data-stu-id="88a9b-117">Integer expression specifying a day.</span></span>  <br/> |
| <span data-ttu-id="88a9b-118">*Stunde*</span><span class="sxs-lookup"><span data-stu-id="88a9b-118">*Hour*</span></span>  <br/> |<span data-ttu-id="88a9b-119">Integer-Ausdruck Stunden angeben.</span><span class="sxs-lookup"><span data-stu-id="88a9b-119">Integer expression specifying hours.</span></span>  <br/> |
| <span data-ttu-id="88a9b-120">*Minute*</span><span class="sxs-lookup"><span data-stu-id="88a9b-120">*Minute*</span></span>  <br/> |<span data-ttu-id="88a9b-121">Integer-Ausdruck Minuten angeben.</span><span class="sxs-lookup"><span data-stu-id="88a9b-121">Integer expression specifying minutes.</span></span>  <br/> |
| <span data-ttu-id="88a9b-122">*Sekunde*</span><span class="sxs-lookup"><span data-stu-id="88a9b-122">*Second*</span></span>  <br/> |<span data-ttu-id="88a9b-123">Integer-Ausdruck Sekunden angeben.</span><span class="sxs-lookup"><span data-stu-id="88a9b-123">Integer expression specifying seconds.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="88a9b-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="88a9b-124">Remarks</span></span>

<span data-ttu-id="88a9b-125">**DateWithTimeFromParts** gibt einen vollständig initialisierten Datums-/Zeitwert zurück.</span><span class="sxs-lookup"><span data-stu-id="88a9b-125">**DateWithTimeFromParts** returns a fully initialized Date/Time value.</span></span> <span data-ttu-id="88a9b-126">Wenn die Argumente nicht gültig sind, wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="88a9b-126">If the arguments are not valid, an error is raised.</span></span> <span data-ttu-id="88a9b-127">Falls erforderlich, dass Argumente Null sind, wird Null zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="88a9b-127">If required arguments are Null, then Null is returned.</span></span> 
  

