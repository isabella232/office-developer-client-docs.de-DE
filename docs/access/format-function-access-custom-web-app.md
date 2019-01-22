---
title: Format-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.assetid: 550fc235-f0b9-4d8e-805b-ce467821a8c9
description: Gibt einen Wert zurück, der entsprechend einem bestimmten Muster formatiert ist.
localization_priority: Priority
ms.openlocfilehash: 5331df30f276a7edd0571e9bf24c759d57ec6a54
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710391"
---
# <a name="format-function-access-custom-web-app"></a><span data-ttu-id="559c1-103">Format-Funktion (benutzerdefinierte Access-Web-App)</span><span class="sxs-lookup"><span data-stu-id="559c1-103">Format function (Access custom web app)</span></span>

<span data-ttu-id="559c1-104">Gibt einen Wert zurück, der entsprechend einem bestimmten Muster formatiert ist.</span><span class="sxs-lookup"><span data-stu-id="559c1-104">Returns a value formatted according to a specified pattern.</span></span>
  
> [!NOTE]
> <span data-ttu-id="559c1-p101">Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="559c1-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="559c1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="559c1-107">Syntax</span></span>

 <span data-ttu-id="559c1-108">**Format** (*Expression*, *Format*)</span><span class="sxs-lookup"><span data-stu-id="559c1-108">**Format** (*Expression*, *Format*)</span></span> 
  
<span data-ttu-id="559c1-109">Die \*\*Format \*\*-Funktion enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="559c1-109">The **DateAdd** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="559c1-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="559c1-110">**Argument name**</span></span>|<span data-ttu-id="559c1-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="559c1-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="559c1-112">*Ausdruck*</span><span class="sxs-lookup"><span data-stu-id="559c1-112">*Expression*</span></span>  <br/> |<span data-ttu-id="559c1-113">Ausdruck eines unterstützten Datentyps, der formatiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="559c1-113">Expression of a supported data type to format.</span></span>  <br/> |
| <span data-ttu-id="559c1-114">*Format*</span><span class="sxs-lookup"><span data-stu-id="559c1-114">*Format*</span></span>  <br/> | <span data-ttu-id="559c1-115">Ein Formatmuster.</span><span class="sxs-lookup"><span data-stu-id="559c1-115">A format pattern.</span></span> <span data-ttu-id="559c1-116">Das Formatargument muss eine gültige Formatzeichenfolge enthalten, entweder als Standardformatzeichenfolge (z. B. „C“ oder „D“), oder als Muster von benutzerdefinierten Zeichen für Datumsangaben und numerische Werte (z. B. „MMM dd, yyyy (dddd)“).</span><span class="sxs-lookup"><span data-stu-id="559c1-116">The format argument must contain a valid format string, either as a standard format string (for example, "C" or "D"), or as a pattern of custom characters for dates and numeric values (for example, "MMMM dd, yyyy (dddd)").</span></span> <span data-ttu-id="559c1-117">Weitere Informationen hierzu finden Sie unter „Hinweise“.</span><span class="sxs-lookup"><span data-stu-id="559c1-117">For more information, see the Remarks section.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="559c1-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="559c1-118">Remarks</span></span>

<span data-ttu-id="559c1-119">Für den *Format*-Parameter können Sie Zeichenfolgen übergeben, die einem der folgenden Muster entsprechen:</span><span class="sxs-lookup"><span data-stu-id="559c1-119">For the  *Format*  parameter, you can pass strings that match any of the following patterns:</span></span> 
  
- [<span data-ttu-id="559c1-120">Standardmäßige Formatzeichenfolgen für numerische Werte</span><span class="sxs-lookup"><span data-stu-id="559c1-120">Standard Numeric Format Strings</span></span>](https://msdn.microsoft.com/library/dwhawy9k%28v=vs.110%29.aspx)
    
- [<span data-ttu-id="559c1-121">Benutzerdefinierte Formatzeichenfolgen für numerische Werte</span><span class="sxs-lookup"><span data-stu-id="559c1-121">Custom Numeric Format Strings</span></span>](https://msdn.microsoft.com/library/0c899ak8%28v=vs.110%29.aspx)
    
- [<span data-ttu-id="559c1-122">Standardmäßige Formatzeichenfolgen für Datums- und Uhrzeitangaben</span><span class="sxs-lookup"><span data-stu-id="559c1-122">Standard Date and Time Format Strings</span></span>](https://msdn.microsoft.com/library/az4se3k1%28v=vs.110%29.aspx)
    
- [<span data-ttu-id="559c1-123">Benutzerdefinierte Formatzeichenfolgen für Datums- und Uhrzeitangaben</span><span class="sxs-lookup"><span data-stu-id="559c1-123">Custom Date and Time Format Strings</span></span>](https://msdn.microsoft.com/library/8kb3ddd4%28v=vs.110%29.aspx)
    
<span data-ttu-id="559c1-124">In den folgenden Bereichen der Access 2013-Web-Apps können Sie die **Format**-Funktion nicht verwenden:</span><span class="sxs-lookup"><span data-stu-id="559c1-124">You cannot use the **Format** function in the following areas of Access 2013 web apps:</span></span> 
  
- <span data-ttu-id="559c1-125">Berechnete Spalten auf Tabellenebene</span><span class="sxs-lookup"><span data-stu-id="559c1-125">Calculated columns at the table level</span></span>
    
- <span data-ttu-id="559c1-126">Benutzeroberflächenmakros</span><span class="sxs-lookup"><span data-stu-id="559c1-126">UI macros</span></span>
    
- <span data-ttu-id="559c1-127">Ausdrücke in Ansichten (z. B. in Formularen)</span><span class="sxs-lookup"><span data-stu-id="559c1-127">Expressions in views (for example, in forms)</span></span>
    

