---
title: DateFromParts-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4fa49d5f-12ea-4d14-9a03-28418f01746c
description: Gibt einen Datumswert für das angegebene Jahr, den Monat und den Tag zurück.
ms.openlocfilehash: 7d47fe93d1990365f1db5885a3ea8fc056aabb9f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423223"
---
# <a name="datefromparts-function-access-custom-web-app"></a><span data-ttu-id="47d10-103">DateFromParts-Funktion (benutzerdefinierte Access-Web-App)</span><span class="sxs-lookup"><span data-stu-id="47d10-103">DateFromParts function (Access custom web app)</span></span>

<span data-ttu-id="47d10-104">Gibt einen Datumswert für das angegebene Jahr, den Monat und den Tag zurück.</span><span class="sxs-lookup"><span data-stu-id="47d10-104">Returns a date value for the specified year, month, and day.</span></span>
  
> [!NOTE]
> <span data-ttu-id="47d10-p101">Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="47d10-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="47d10-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="47d10-107">Syntax</span></span>

<span data-ttu-id="47d10-108">**DateFromParts** (*Year*, *Month*, *Day*)</span><span class="sxs-lookup"><span data-stu-id="47d10-108">**DateFromParts** (*Year*, *Month*, *Day*)</span></span> 
  
<span data-ttu-id="47d10-109">Die **DateFromParts-Funktion** enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="47d10-109">The **DateFromParts** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="47d10-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="47d10-110">**Argument name**</span></span>|<span data-ttu-id="47d10-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="47d10-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="47d10-112">*Jahr*</span><span class="sxs-lookup"><span data-stu-id="47d10-112">*Year*</span></span>  <br/> |<span data-ttu-id="47d10-113">Ganzzahliger Ausdruck, der ein Jahr an gibt.</span><span class="sxs-lookup"><span data-stu-id="47d10-113">Integer expression specifying a year.</span></span>  <br/> |
| <span data-ttu-id="47d10-114">*Month*</span><span class="sxs-lookup"><span data-stu-id="47d10-114">*Month*</span></span>  <br/> |<span data-ttu-id="47d10-115">Ganzzahliger Ausdruck, der einen Monat von 1 bis 12 an gibt.</span><span class="sxs-lookup"><span data-stu-id="47d10-115">Integer expression specifying a month, from 1 to 12.</span></span>  <br/> |
| <span data-ttu-id="47d10-116">*Day*</span><span class="sxs-lookup"><span data-stu-id="47d10-116">*Day*</span></span>  <br/> |<span data-ttu-id="47d10-117">Ganzzahliger Ausdruck, der einen Tag an gibt.</span><span class="sxs-lookup"><span data-stu-id="47d10-117">Integer expression specifying a day.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="47d10-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="47d10-118">Remarks</span></span>

<span data-ttu-id="47d10-119">**DateFromParts** gibt einen Datumswert zurück, bei dem der Datumsteil auf das angegebene Jahr, den Monat und den Tag und den Zeitteil auf den Standardwert festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="47d10-119">**DateFromParts** returns a date value with the date portion set to the specified year, month and day, and the time portion set to the default.</span></span> <span data-ttu-id="47d10-120">Wenn die Argumente ungültig sind, wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="47d10-120">If the arguments are not valid, then an error is raised.</span></span> <span data-ttu-id="47d10-121">Wenn erforderliche Argumente null sind, wird NULL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="47d10-121">If required arguments are null, then NULL is returned.</span></span> 
  
## <a name="example"></a><span data-ttu-id="47d10-122">Beispiel</span><span class="sxs-lookup"><span data-stu-id="47d10-122">Example</span></span>

<span data-ttu-id="47d10-123">Der folgende Ausdruck verwendet die **DateFromParts-Funktion,** um den ersten Tag des aktuellen Monats zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="47d10-123">The following expression uses the **DateFromParts** function to calculate the first day of the current month.</span></span> 
  
`DateFromParts(Year(Today()),Month(Today()),1)`



