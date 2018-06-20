---
title: TimeFromParts-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f631b7e-6e3c-46dc-a05f-6a07f9a91268
description: Gibt einen Zeitwert basierend auf angegebenen Teile zurück.
ms.openlocfilehash: 55a4d1c31fdd2248e3e154d83e803d9f5a5ebb06
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790366"
---
# <a name="timefromparts-function-access-custom-web-app"></a><span data-ttu-id="c77bf-103">TimeFromParts-Funktion (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="c77bf-103">TimeFromParts Function (Access custom web app)</span></span>

<span data-ttu-id="c77bf-104">Gibt einen Zeitwert basierend auf angegebenen Teile zurück.</span><span class="sxs-lookup"><span data-stu-id="c77bf-104">Returns a time value based on specified parts.</span></span>
  
> [!NOTE]
> <span data-ttu-id="c77bf-p101">[!HINWEIS] Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="c77bf-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c77bf-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c77bf-107">Syntax</span></span>

 <span data-ttu-id="c77bf-108">**TimeFromParts** (*Stunde*, *Minute*, *Sekunde*)</span><span class="sxs-lookup"><span data-stu-id="c77bf-108">**TimeFromParts** (*Hour*, *Minute*, *Second*)</span></span> 
  
<span data-ttu-id="c77bf-109">Die **TimeFromParts** -Funktion enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="c77bf-109">The **TimeFromParts** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="c77bf-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="c77bf-110">**Argument name**</span></span>|<span data-ttu-id="c77bf-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="c77bf-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="c77bf-112">*Stunde*</span><span class="sxs-lookup"><span data-stu-id="c77bf-112">*Hour*</span></span>  <br/> |<span data-ttu-id="c77bf-113">Integer-Ausdruck Stunden angeben.</span><span class="sxs-lookup"><span data-stu-id="c77bf-113">Integer expression specifying hours.</span></span>  <br/> |
| <span data-ttu-id="c77bf-114">*Minute*</span><span class="sxs-lookup"><span data-stu-id="c77bf-114">*Minute*</span></span>  <br/> |<span data-ttu-id="c77bf-115">Integer-Ausdruck Minuten angeben.</span><span class="sxs-lookup"><span data-stu-id="c77bf-115">Integer expression specifying minutes.</span></span>  <br/> |
| <span data-ttu-id="c77bf-116">*Sekunde*</span><span class="sxs-lookup"><span data-stu-id="c77bf-116">*Second*</span></span>  <br/> |<span data-ttu-id="c77bf-117">Integer-Ausdruck Sekunden angeben.</span><span class="sxs-lookup"><span data-stu-id="c77bf-117">Integer expression specifying seconds.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c77bf-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c77bf-118">See also</span></span>

 <span data-ttu-id="c77bf-119">**TimeFromParts** gibt einen vollständig initialisiert Zeitwert zurück.</span><span class="sxs-lookup"><span data-stu-id="c77bf-119">**TimeFromParts** returns a fully initialized time value.</span></span> <span data-ttu-id="c77bf-120">Wenn die Argumente ungültig sind, wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="c77bf-120">If the arguments are invalid, then an error is raised.</span></span> <span data-ttu-id="c77bf-121">Wenn einer der Parameter null ist, wird Null zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c77bf-121">If any of the parameters are null, null is returned.</span></span> 
  

