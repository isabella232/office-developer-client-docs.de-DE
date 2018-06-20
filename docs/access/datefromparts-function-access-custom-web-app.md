---
title: DateFromParts-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4fa49d5f-12ea-4d14-9a03-28418f01746c
description: Gibt einen Date-Wert für das angegebene Jahr, Monat und Tag zurück.
ms.openlocfilehash: 5a2ff76d99076cf9f53b0dce8c5019f38d910f58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790163"
---
# <a name="datefromparts-function-access-custom-web-app"></a><span data-ttu-id="e1125-103">DateFromParts-Funktion (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="e1125-103">DateFromParts function (Access custom web app)</span></span>

<span data-ttu-id="e1125-104">Gibt einen Date-Wert für das angegebene Jahr, Monat und Tag zurück.</span><span class="sxs-lookup"><span data-stu-id="e1125-104">Returns a date value for the specified year, month, and day.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e1125-p101">[!HINWEIS] Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="e1125-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e1125-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1125-107">Syntax</span></span>

<span data-ttu-id="e1125-108">**DateFromParts** (*Jahr*, *Monat*, *Tag*)</span><span class="sxs-lookup"><span data-stu-id="e1125-108">**DateFromParts** (*Year*, *Month*, *Day*)</span></span> 
  
<span data-ttu-id="e1125-109">Die **DateFromParts** -Funktion enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="e1125-109">The **DateFromParts** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="e1125-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="e1125-110">**Argument name**</span></span>|<span data-ttu-id="e1125-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="e1125-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="e1125-112">*Jahr*</span><span class="sxs-lookup"><span data-stu-id="e1125-112">*Year*</span></span>  <br/> |<span data-ttu-id="e1125-113">Ein Ausdruck, der ganze Zahl, die einem Jahr angibt.</span><span class="sxs-lookup"><span data-stu-id="e1125-113">Integer expression specifying a year.</span></span>  <br/> |
| <span data-ttu-id="e1125-114">*Month*</span><span class="sxs-lookup"><span data-stu-id="e1125-114">*Month*</span></span>  <br/> |<span data-ttu-id="e1125-115">Ein Ausdruck, der ganze Zahl, die einen Monat, von 1 bis 12 angibt.</span><span class="sxs-lookup"><span data-stu-id="e1125-115">Integer expression specifying a month, from 1 to 12.</span></span>  <br/> |
| <span data-ttu-id="e1125-116">*Tag*</span><span class="sxs-lookup"><span data-stu-id="e1125-116">*Day*</span></span>  <br/> |<span data-ttu-id="e1125-117">Ein Ausdruck, der ganze Zahl, die einen Tag angibt.</span><span class="sxs-lookup"><span data-stu-id="e1125-117">Integer expression specifying a day.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1125-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e1125-118">Remarks</span></span>

<span data-ttu-id="e1125-119">**DateFromParts** gibt einen Date-Wert zurück, mit der Datumsteil auf das angegebene Jahr, Monat und Tag und auf den Standardwert den Zeitbereich festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e1125-119">**DateFromParts** returns a date value with the date portion set to the specified year, month and day, and the time portion set to the default.</span></span> <span data-ttu-id="e1125-120">Wenn die Argumente nicht gültig sind, wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="e1125-120">If the arguments are not valid, then an error is raised.</span></span> <span data-ttu-id="e1125-121">Falls erforderlich, dass Argumente null sind, wird NULL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e1125-121">If required arguments are null, then NULL is returned.</span></span> 
  
## <a name="example"></a><span data-ttu-id="e1125-122">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e1125-122">Example</span></span>

<span data-ttu-id="e1125-123">Der folgende Ausdruck wird die **DateFromParts** -Funktion verwendet, um den ersten Tag des aktuellen Monats zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="e1125-123">The following expression uses the **DateFromParts** function to calculate the first day of the current month.</span></span> 
  
`DateFromParts(Year(Today()),Month(Today()),1)`



