---
title: Jetzt Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8842a555-d4c8-4528-b5f9-0ddf5691273d
description: Gibt den aktuellen Wert für Datum und Uhrzeit in der Zeitzone, die von der Anwendung definiert.
ms.openlocfilehash: 721c0d2a872e0c4ec9ca75c963d5429a72fb2d3d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790326"
---
# <a name="now-function-access-custom-web-app"></a><span data-ttu-id="fe5de-103">Jetzt Funktion (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="fe5de-103">Now Function (Access custom web app)</span></span>

<span data-ttu-id="fe5de-104">Gibt den aktuellen Wert für Datum und Uhrzeit in der Zeitzone, die von der Anwendung definiert.</span><span class="sxs-lookup"><span data-stu-id="fe5de-104">Returns the current date and time value in the time zone defined by the application.</span></span>
  
> [!NOTE]
> <span data-ttu-id="fe5de-p101">[!HINWEIS] Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="fe5de-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="fe5de-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe5de-107">Syntax</span></span>

 <span data-ttu-id="fe5de-108">**Jetzt** ()</span><span class="sxs-lookup"><span data-stu-id="fe5de-108">**Now** ()</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fe5de-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fe5de-109">Remarks</span></span>

<span data-ttu-id="fe5de-110">Das Ergebnis des **jetzt** Funktion ändert sich nur, wenn die Spalte mit der Formel aktualisiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fe5de-110">The result of the **Now** function changes only when the column that contains the formula is refreshed.</span></span> <span data-ttu-id="fe5de-111">Es wird nicht ständig aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="fe5de-111">It is not updated continuously.</span></span> 
  
<span data-ttu-id="fe5de-112">Die **heute** -Funktion gibt zurück, die an denselben Tag jedoch ist nicht wirklich präzise in Bezug auf Zeit. Die zurückgegebene Uhrzeit handelt es sich immer 00:00:00: 00 Uhr, und nur das Datum wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="fe5de-112">The **Today** function returns the same date but is not precise with regard to time; the time returned is always 12:00:00 AM and only the date is updated.</span></span> 
  

