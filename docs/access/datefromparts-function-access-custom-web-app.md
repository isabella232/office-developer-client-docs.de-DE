---
title: DateFromParts-Funktion (Access Custom Web App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4fa49d5f-12ea-4d14-9a03-28418f01746c
description: Gibt einen Datumswert für das angegebene Jahr, den Monat und den Tag zurück.
ms.openlocfilehash: 7d47fe93d1990365f1db5885a3ea8fc056aabb9f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282122"
---
# <a name="datefromparts-function-access-custom-web-app"></a><span data-ttu-id="23af3-103">DateFromParts-Funktion (Access Custom Web App)</span><span class="sxs-lookup"><span data-stu-id="23af3-103">DateFromParts function (Access custom web app)</span></span>

<span data-ttu-id="23af3-104">Gibt einen Datumswert für das angegebene Jahr, den Monat und den Tag zurück.</span><span class="sxs-lookup"><span data-stu-id="23af3-104">Returns a date value for the specified year, month, and day.</span></span>
  
> [!NOTE]
> <span data-ttu-id="23af3-p101">Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="23af3-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="23af3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="23af3-107">Syntax</span></span>

<span data-ttu-id="23af3-108">**DateFromParts** (*Jahr*, *Monat*, *Tag*)</span><span class="sxs-lookup"><span data-stu-id="23af3-108">**DateFromParts** (*Year*, *Month*, *Day*)</span></span> 
  
<span data-ttu-id="23af3-109">Die **DateFromParts** -Funktion enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="23af3-109">The **DateFromParts** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="23af3-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="23af3-110">**Argument name**</span></span>|<span data-ttu-id="23af3-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="23af3-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="23af3-112">*Jahr*</span><span class="sxs-lookup"><span data-stu-id="23af3-112">*Year*</span></span>  <br/> |<span data-ttu-id="23af3-113">Integer-Ausdruck, der ein Jahr angibt.</span><span class="sxs-lookup"><span data-stu-id="23af3-113">Integer expression specifying a year.</span></span>  <br/> |
| <span data-ttu-id="23af3-114">*Month*</span><span class="sxs-lookup"><span data-stu-id="23af3-114">*Month*</span></span>  <br/> |<span data-ttu-id="23af3-115">Integer-Ausdruck, der einen Monat zwischen 1 und 12 angibt.</span><span class="sxs-lookup"><span data-stu-id="23af3-115">Integer expression specifying a month, from 1 to 12.</span></span>  <br/> |
| <span data-ttu-id="23af3-116">*Day*</span><span class="sxs-lookup"><span data-stu-id="23af3-116">*Day*</span></span>  <br/> |<span data-ttu-id="23af3-117">Integer-Ausdruck, der einen Tag angibt.</span><span class="sxs-lookup"><span data-stu-id="23af3-117">Integer expression specifying a day.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="23af3-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="23af3-118">Remarks</span></span>

<span data-ttu-id="23af3-119">**DateFromParts** gibt einen Date-Wert zurück, wobei der Datumsteil auf das angegebene Jahr, den Monat und den angegebenen Tag sowie auf den standardmäßigen Zeitabschnitt festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="23af3-119">**DateFromParts** returns a date value with the date portion set to the specified year, month and day, and the time portion set to the default.</span></span> <span data-ttu-id="23af3-120">Wenn die Argumente ungültig sind, wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="23af3-120">If the arguments are not valid, then an error is raised.</span></span> <span data-ttu-id="23af3-121">Wenn die erforderlichen Argumente NULL sind, wird NULL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="23af3-121">If required arguments are null, then NULL is returned.</span></span> 
  
## <a name="example"></a><span data-ttu-id="23af3-122">Beispiel</span><span class="sxs-lookup"><span data-stu-id="23af3-122">Example</span></span>

<span data-ttu-id="23af3-123">Der folgende Ausdruck verwendet die **DateFromParts** -Funktion, um den ersten Tag des aktuellen Monats zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="23af3-123">The following expression uses the **DateFromParts** function to calculate the first day of the current month.</span></span> 
  
`DateFromParts(Year(Today()),Month(Today()),1)`



