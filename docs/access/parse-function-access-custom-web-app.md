---
title: Parse-Funktion (Access Custom Web App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09dee0ae-89b2-449c-a3c8-d6b270710b64
description: Analysiert einen Textwert und gibt seinen Wert in einem bestimmten Typ mithilfe der Culture der Anwendung zurück.
ms.openlocfilehash: d664985ab1d7a7d33b99c52d5bab4aa714767e40
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411134"
---
# <a name="parse-function-access-custom-web-app"></a><span data-ttu-id="3fdc1-103">Parse-Funktion (Access Custom Web App)</span><span class="sxs-lookup"><span data-stu-id="3fdc1-103">Parse Function (Access custom web app)</span></span>

<span data-ttu-id="3fdc1-104">Analysiert einen Textwert und gibt seinen Wert in einem bestimmten Typ mithilfe der Culture der Anwendung zurück.</span><span class="sxs-lookup"><span data-stu-id="3fdc1-104">Parses a text value and returns its value in a given type using the culture of the application.</span></span>
  
> [!NOTE]
> <span data-ttu-id="3fdc1-p101">Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="3fdc1-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3fdc1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3fdc1-107">Syntax</span></span>

 <span data-ttu-id="3fdc1-108">**Analysieren** (*Text*- *Datentyp, DataType*)</span><span class="sxs-lookup"><span data-stu-id="3fdc1-108">**Parse** (*TextExpression*, *DataType*)</span></span> 
  
<span data-ttu-id="3fdc1-109">Die **Parse** -Funktion enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="3fdc1-109">The **Parse** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="3fdc1-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="3fdc1-110">**Argument name**</span></span>|<span data-ttu-id="3fdc1-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3fdc1-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="3fdc1-112">*Text*</span><span class="sxs-lookup"><span data-stu-id="3fdc1-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="3fdc1-113">Ein Textausdruck, der den formatierten Wert darstellt, der in den angegebenen Datentyp analysiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3fdc1-113">A text expression representing the formatted value to parse into the specified data type.</span></span>  <br/> |
| <span data-ttu-id="3fdc1-114">*DataType*</span><span class="sxs-lookup"><span data-stu-id="3fdc1-114">*DataType*</span></span>  <br/> |<span data-ttu-id="3fdc1-115">Literalwert, der den für das Ergebnis erforderlichen Datentyp darstellt.</span><span class="sxs-lookup"><span data-stu-id="3fdc1-115">Literal value representing the data type requested for the result.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3fdc1-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3fdc1-116">Remarks</span></span>

<span data-ttu-id="3fdc1-117">Verwenden Sie **Parse** nur für die Konvertierung von Zeichenfolge zu Datum/Uhrzeit und Zahlentypen.</span><span class="sxs-lookup"><span data-stu-id="3fdc1-117">Use **Parse** only for converting from string to date/time and number types.</span></span> <span data-ttu-id="3fdc1-118">Verwenden Sie für allgemeine Typkonvertierungen die **Convert** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="3fdc1-118">For general type conversions, use the **Convert** function.</span></span> <span data-ttu-id="3fdc1-119">Beachten Sie, dass bei der Analyse des Zeichenfolgenwerts ein bestimmter Leistungsaufwand auftritt.</span><span class="sxs-lookup"><span data-stu-id="3fdc1-119">Keep in mind that there is a certain performance overhead in parsing the string value.</span></span> 
  

