---
title: TimeFromParts-Funktion (Access Custom Web App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f631b7e-6e3c-46dc-a05f-6a07f9a91268
description: Gibt einen Zeitwert basierend auf bestimmten Teilen zurück.
ms.openlocfilehash: 8e2105140056bc65e9af0a6eda6e40fc44caed1a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417994"
---
# <a name="timefromparts-function-access-custom-web-app"></a><span data-ttu-id="03f4b-103">TimeFromParts-Funktion (Access Custom Web App)</span><span class="sxs-lookup"><span data-stu-id="03f4b-103">TimeFromParts Function (Access custom web app)</span></span>

<span data-ttu-id="03f4b-104">Gibt einen Zeitwert basierend auf bestimmten Teilen zurück.</span><span class="sxs-lookup"><span data-stu-id="03f4b-104">Returns a time value based on specified parts.</span></span>
  
> [!NOTE]
> <span data-ttu-id="03f4b-p101">Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="03f4b-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="03f4b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="03f4b-107">Syntax</span></span>

 <span data-ttu-id="03f4b-108">**TimeFromParts** (*Stunde*, *Minute*, *Sekunde*)</span><span class="sxs-lookup"><span data-stu-id="03f4b-108">**TimeFromParts** (*Hour*, *Minute*, *Second*)</span></span> 
  
<span data-ttu-id="03f4b-109">Die **TimeFromParts** -Funktion enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="03f4b-109">The **TimeFromParts** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="03f4b-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="03f4b-110">**Argument name**</span></span>|<span data-ttu-id="03f4b-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="03f4b-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="03f4b-112">*Hour*</span><span class="sxs-lookup"><span data-stu-id="03f4b-112">*Hour*</span></span>  <br/> |<span data-ttu-id="03f4b-113">Integer-Ausdruck, der Stunden angibt.</span><span class="sxs-lookup"><span data-stu-id="03f4b-113">Integer expression specifying hours.</span></span>  <br/> |
| <span data-ttu-id="03f4b-114">*Minute*</span><span class="sxs-lookup"><span data-stu-id="03f4b-114">*Minute*</span></span>  <br/> |<span data-ttu-id="03f4b-115">Ganzzahliger Ausdruck, der Minuten angibt.</span><span class="sxs-lookup"><span data-stu-id="03f4b-115">Integer expression specifying minutes.</span></span>  <br/> |
| <span data-ttu-id="03f4b-116">*Zweiter*</span><span class="sxs-lookup"><span data-stu-id="03f4b-116">*Second*</span></span>  <br/> |<span data-ttu-id="03f4b-117">Integer-Ausdruck, der Sekunden angibt.</span><span class="sxs-lookup"><span data-stu-id="03f4b-117">Integer expression specifying seconds.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="03f4b-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03f4b-118">See also</span></span>

 <span data-ttu-id="03f4b-119">**TimeFromParts** gibt einen vollständig initialisierten Zeitwert zurück.</span><span class="sxs-lookup"><span data-stu-id="03f4b-119">**TimeFromParts** returns a fully initialized time value.</span></span> <span data-ttu-id="03f4b-120">Wenn die Argumente ungültig sind, wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="03f4b-120">If the arguments are invalid, then an error is raised.</span></span> <span data-ttu-id="03f4b-121">Wenn einer der Parameter NULL ist, wird NULL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="03f4b-121">If any of the parameters are null, null is returned.</span></span> 
  

