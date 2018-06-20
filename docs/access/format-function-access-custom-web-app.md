---
title: Format-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 550fc235-f0b9-4d8e-805b-ce467821a8c9
description: Gibt einen Wert nach einem bestimmten Muster formatiert.
ms.openlocfilehash: 974b56ab8e6bc3f97c1931ba67ca9cd08c3511c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790222"
---
# <a name="format-function-access-custom-web-app"></a><span data-ttu-id="9a749-103">Format-Funktion (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="9a749-103">Format Function (Access custom web app)</span></span>

<span data-ttu-id="9a749-104">Gibt einen Wert nach einem bestimmten Muster formatiert.</span><span class="sxs-lookup"><span data-stu-id="9a749-104">Returns a value formatted according to a specified pattern.</span></span>
  
> [!NOTE]
> <span data-ttu-id="9a749-p101">[!HINWEIS] Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="9a749-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9a749-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a749-107">Syntax</span></span>

 <span data-ttu-id="9a749-108">**Format** (*Ausdruck*, *Format*)</span><span class="sxs-lookup"><span data-stu-id="9a749-108">**Format** (*Expression*, *Format*)</span></span> 
  
<span data-ttu-id="9a749-109">Die **Format** -Funktion enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="9a749-109">The **Format** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="9a749-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="9a749-110">**Argument name**</span></span>|<span data-ttu-id="9a749-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="9a749-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="9a749-112">*Expression*</span><span class="sxs-lookup"><span data-stu-id="9a749-112">*Expression*</span></span>  <br/> |<span data-ttu-id="9a749-113">Ausdruck, der einen unterstützten Datentyp formatieren.</span><span class="sxs-lookup"><span data-stu-id="9a749-113">Expression of a supported data type to format.</span></span>  <br/> |
| <span data-ttu-id="9a749-114">*Format*</span><span class="sxs-lookup"><span data-stu-id="9a749-114">*Format*</span></span>  <br/> | <span data-ttu-id="9a749-115">Ein Formatmuster.</span><span class="sxs-lookup"><span data-stu-id="9a749-115">A format pattern.</span></span> <span data-ttu-id="9a749-116">Das Formatargument muss eine gültige Formatzeichenfolge, entweder als String-Standardformat (z. B. "C" oder "D") oder als ein Muster der benutzerdefinierten Zeichen für Datumsangaben und numerische Werte (beispielsweise "MMMM Dd, Yyyy (Dddd)") enthalten.</span><span class="sxs-lookup"><span data-stu-id="9a749-116">The format argument must contain a valid format string, either as a standard format string (for example, "C" or "D"), or as a pattern of custom characters for dates and numeric values (for example, "MMMM dd, yyyy (dddd)").</span></span> <span data-ttu-id="9a749-117">Weitere Informationen finden Sie unter "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="9a749-117">For more information, see Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9a749-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9a749-118">Remarks</span></span>

<span data-ttu-id="9a749-119">Für den *Format* -Parameter können Sie Zeichenfolgen übergeben, die mit einem der folgenden Muster übereinstimmen:</span><span class="sxs-lookup"><span data-stu-id="9a749-119">For the  *Format*  parameter, you can pass strings that match any of the following patterns:</span></span> 
  
- [<span data-ttu-id="9a749-120">Standardmäßige numerische Formatzeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="9a749-120">Standard Numeric Format Strings</span></span>](http://msdn.microsoft.com/en-us/library/dwhawy9k%28v=vs.110%29.aspx)
    
- [<span data-ttu-id="9a749-121">Benutzerdefinierte numerische Formatzeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="9a749-121">Custom Numeric Format Strings</span></span>](http://msdn.microsoft.com/en-us/library/0c899ak8%28v=vs.110%29.aspx)
    
- [<span data-ttu-id="9a749-122">Formatzeichenfolgen für Datum und Uhrzeit</span><span class="sxs-lookup"><span data-stu-id="9a749-122">Standard Date and Time Format Strings</span></span>](http://msdn.microsoft.com/en-us/library/az4se3k1%28v=vs.110%29.aspx)
    
- [<span data-ttu-id="9a749-123">Benutzerdefinierte Datums- / Formatieren von Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="9a749-123">Custom Date and Time Format Strings</span></span>](http://msdn.microsoft.com/en-us/library/8kb3ddd4%28v=vs.110%29.aspx)
    
<span data-ttu-id="9a749-124">Sie können nicht in den folgenden Bereichen von Access 2013 Web apps die **Format** -Funktion verwenden:</span><span class="sxs-lookup"><span data-stu-id="9a749-124">You cannot use the **Format** function in the following areas of Access 2013 web apps:</span></span> 
  
- <span data-ttu-id="9a749-125">Berechnete Spalten auf Tabellenebene</span><span class="sxs-lookup"><span data-stu-id="9a749-125">Calculated columns at the table level</span></span>
    
- <span data-ttu-id="9a749-126">UI-Makros</span><span class="sxs-lookup"><span data-stu-id="9a749-126">UI macros</span></span>
    
- <span data-ttu-id="9a749-127">Ausdrücke in Ansichten (beispielsweise in Forms)</span><span class="sxs-lookup"><span data-stu-id="9a749-127">Expressions in views (for example, in forms)</span></span>
    

