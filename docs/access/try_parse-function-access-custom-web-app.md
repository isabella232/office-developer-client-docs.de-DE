---
title: Try_Parse-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed35263c-b0ad-4269-9caa-c0164015e980
description: Analysiert einen Textwert für den angegebenen Datentyp in der Kultur der Anwendung oder gibt Null zurück, wenn die Konvertierung ungültig ist.
ms.openlocfilehash: 5d201557607d2d18c36238d9658b705a6a49fda8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427528"
---
# <a name="try_parse-function-access-custom-web-app"></a><span data-ttu-id="37bb3-103">Try_Parse-Funktion (benutzerdefinierte Access-Web-App)</span><span class="sxs-lookup"><span data-stu-id="37bb3-103">Try_Parse Function (Access custom web app)</span></span>

<span data-ttu-id="37bb3-104">Analysiert einen Textwert für den angegebenen Datentyp in der Kultur der Anwendung oder gibt Null zurück, wenn die Konvertierung ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="37bb3-104">Parses a text value to the specified data type in the culture of the application or returns Null if the conversion is not valid.</span></span>
  
> [!NOTE]
> <span data-ttu-id="37bb3-p101">Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="37bb3-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="37bb3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="37bb3-107">Syntax</span></span>

 <span data-ttu-id="37bb3-108">**Try_Parse** (*TextExpression*, *DataType*)</span><span class="sxs-lookup"><span data-stu-id="37bb3-108">**Try_Parse** (*TextExpression*, *DataType*)</span></span> 
  
<span data-ttu-id="37bb3-109">Die **Try_Parse** enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="37bb3-109">The **Try_Parse** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="37bb3-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="37bb3-110">**Argument name**</span></span>|<span data-ttu-id="37bb3-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="37bb3-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="37bb3-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="37bb3-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="37bb3-113">Ein Textausdruck, der den formatierten Wert darstellt, der in den angegebenen Datentyp analysiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="37bb3-113">A text expression representing the formatted value to parse into the specified data type.</span></span>  <br/> |
| <span data-ttu-id="37bb3-114">*DataType*</span><span class="sxs-lookup"><span data-stu-id="37bb3-114">*DataType*</span></span>  <br/> |<span data-ttu-id="37bb3-115">Der Datentyp, in den *TextExpression analysiert werden soll.*</span><span class="sxs-lookup"><span data-stu-id="37bb3-115">The data type into which to parse  *TextExpression*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="37bb3-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="37bb3-116">Remarks</span></span>

<span data-ttu-id="37bb3-117">Verwenden **Try_Parse** nur zum Konvertieren von Zeichenfolgen in Datums-/Uhrzeit- und Zahlentypen.</span><span class="sxs-lookup"><span data-stu-id="37bb3-117">Use **Try_Parse** only for converting from string to date/time and number types.</span></span> <span data-ttu-id="37bb3-118">Verwenden Sie für allgemeine Typkonvertierungen weiterhin **Convert**.</span><span class="sxs-lookup"><span data-stu-id="37bb3-118">For general type conversions, continue to use **Convert**.</span></span> 
  

