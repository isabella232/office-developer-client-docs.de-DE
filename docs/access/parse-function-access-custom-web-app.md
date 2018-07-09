---
title: Parse-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09dee0ae-89b2-449c-a3c8-d6b270710b64
description: Analysiert einen Textwert und gibt den Wert in einem angegebenen Typ unter Verwendung der Kultur der Anwendung zurück.
ms.openlocfilehash: fa3c453f1faeadca173aaace513ee5ba9115c5fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790339"
---
# <a name="parse-function-access-custom-web-app"></a><span data-ttu-id="16bf8-103">Parse-Funktion (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="16bf8-103">Parse Function (Access custom web app)</span></span>

<span data-ttu-id="16bf8-104">Analysiert einen Textwert und gibt den Wert in einem angegebenen Typ unter Verwendung der Kultur der Anwendung zurück.</span><span class="sxs-lookup"><span data-stu-id="16bf8-104">Parses a text value and returns its value in a given type using the culture of the application.</span></span>
  
> [!NOTE]
> <span data-ttu-id="16bf8-p101">Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="16bf8-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="16bf8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="16bf8-107">Syntax</span></span>

 <span data-ttu-id="16bf8-108">**Analysieren** (*TextExpression*, *Datentyp*)</span><span class="sxs-lookup"><span data-stu-id="16bf8-108">**Parse** (*TextExpression*, *DataType*)</span></span> 
  
<span data-ttu-id="16bf8-109">Die **Parse** -Funktion enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="16bf8-109">The **Parse** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="16bf8-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="16bf8-110">**Argument name**</span></span>|<span data-ttu-id="16bf8-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="16bf8-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="16bf8-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="16bf8-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="16bf8-113">Ein Ausdruck, der den formatierten Wert in den angegebenen Datentyp zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="16bf8-113">A text expression representing the formatted value to parse into the specified data type.</span></span>  <br/> |
| <span data-ttu-id="16bf8-114">*DataType*</span><span class="sxs-lookup"><span data-stu-id="16bf8-114">*DataType*</span></span>  <br/> |<span data-ttu-id="16bf8-115">Literale Wert, der den Datentyp für das Ergebnis angefordert darstellt.</span><span class="sxs-lookup"><span data-stu-id="16bf8-115">Literal value representing the data type requested for the result.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="16bf8-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="16bf8-116">Remarks</span></span>

<span data-ttu-id="16bf8-117">Verwenden Sie nur für die Konvertierung von Zeichenfolge Datum/Uhrzeit und Typen der Nummer **zu analysieren** .</span><span class="sxs-lookup"><span data-stu-id="16bf8-117">Use **Parse** only for converting from string to date/time and number types.</span></span> <span data-ttu-id="16bf8-118">Verwenden Sie für allgemeine typkonvertierungen die **Convert** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="16bf8-118">For general type conversions, use the **Convert** function.</span></span> <span data-ttu-id="16bf8-119">Behalten Sie im Hinterkopf, dass es eine bestimmte Leistung führt zu mehr Verarbeitungsaufwand bei der Analyse des String-Werts ist.</span><span class="sxs-lookup"><span data-stu-id="16bf8-119">Keep in mind that there is a certain performance overhead in parsing the string value.</span></span> 
  

