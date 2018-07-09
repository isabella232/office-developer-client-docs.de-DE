---
title: Try_Parse-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed35263c-b0ad-4269-9caa-c0164015e980
description: Analysiert ein Textwerts in den angegebenen Datentyp in der Kultur der Anwendung, oder gibt Null zurück, wenn die Konvertierung nicht gültig ist.
ms.openlocfilehash: 3446e928d9772641f9aea7b956e142f995824b1e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790379"
---
# <a name="tryparse-function-access-custom-web-app"></a><span data-ttu-id="1b1d6-103">Try_Parse-Funktion (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="1b1d6-103">Try_Parse Function (Access custom web app)</span></span>

<span data-ttu-id="1b1d6-104">Analysiert ein Textwerts in den angegebenen Datentyp in der Kultur der Anwendung, oder gibt Null zurück, wenn die Konvertierung nicht gültig ist.</span><span class="sxs-lookup"><span data-stu-id="1b1d6-104">Parses a text value to the specified data type in the culture of the application or returns Null if the conversion is not valid.</span></span>
  
> [!NOTE]
> <span data-ttu-id="1b1d6-p101">Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="1b1d6-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="1b1d6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b1d6-107">Syntax</span></span>

 <span data-ttu-id="1b1d6-108">**Try_Parse** (*TextExpression*, *Datentyp*)</span><span class="sxs-lookup"><span data-stu-id="1b1d6-108">**Try_Parse** (*TextExpression*, *DataType*)</span></span> 
  
<span data-ttu-id="1b1d6-109">Die **Try_Parse** -Funktion enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="1b1d6-109">The **Try_Parse** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="1b1d6-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="1b1d6-110">**Argument name**</span></span>|<span data-ttu-id="1b1d6-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="1b1d6-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="1b1d6-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="1b1d6-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="1b1d6-113">Ein Ausdruck, der den formatierten Wert in den angegebenen Datentyp zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="1b1d6-113">A text expression representing the formatted value to parse into the specified data type.</span></span>  <br/> |
| <span data-ttu-id="1b1d6-114">*DataType*</span><span class="sxs-lookup"><span data-stu-id="1b1d6-114">*DataType*</span></span>  <br/> |<span data-ttu-id="1b1d6-115">Der Datentyp in die *TextExpression* zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="1b1d6-115">The data type into which to parse  *TextExpression*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1b1d6-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1b1d6-116">Remarks</span></span>

<span data-ttu-id="1b1d6-117">Verwenden Sie **Try_Parse** nur für die Konvertierung von Zeichenfolge Datum/Uhrzeit und Typen der Nummer.</span><span class="sxs-lookup"><span data-stu-id="1b1d6-117">Use **Try_Parse** only for converting from string to date/time and number types.</span></span> <span data-ttu-id="1b1d6-118">Allgemeine typkonvertierungen auch weiterhin **Konvertieren**verwenden.</span><span class="sxs-lookup"><span data-stu-id="1b1d6-118">For general type conversions, continue to use **Convert**.</span></span> 
  

