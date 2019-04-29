---
title: Stuff-Funktion (Access Custom Web App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4d8d6a34-f884-40a4-b330-5c104d16cf97
description: Fügt eine Textzeichenfolge in eine andere Textzeichenfolge ein. Sie löscht eine angegebene Zeichen Länge in der ersten Zeichenfolge an der Startposition und fügt dann die zweite Zeichenfolge in die erste Zeichenfolge an der Startposition ein.
ms.openlocfilehash: 591823952faa0d593b6db1f5bfb00cc68a894a8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427675"
---
# <a name="stuff-function-access-custom-web-app"></a><span data-ttu-id="6fb5c-104">Stuff-Funktion (Access Custom Web App)</span><span class="sxs-lookup"><span data-stu-id="6fb5c-104">Stuff Function (Access custom web app)</span></span>

<span data-ttu-id="6fb5c-105">Fügt eine Textzeichenfolge in eine andere Textzeichenfolge ein.</span><span class="sxs-lookup"><span data-stu-id="6fb5c-105">Inserts a text string into another text string.</span></span> <span data-ttu-id="6fb5c-106">Sie löscht eine angegebene Zeichen Länge in der ersten Zeichenfolge an der Startposition und fügt dann die zweite Zeichenfolge in die erste Zeichenfolge an der Startposition ein.</span><span class="sxs-lookup"><span data-stu-id="6fb5c-106">It deletes a specified length of characters in the first string at the start position and then inserts the second string into the first string at the start position.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="6fb5c-p103">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="6fb5c-p103">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6fb5c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6fb5c-109">Syntax</span></span>

 <span data-ttu-id="6fb5c-110">**Stuff** (*IntoTextExpression*, *Start*, *length*, *ThisTextExpression*)</span><span class="sxs-lookup"><span data-stu-id="6fb5c-110">**Stuff** (*IntoTextExpression*, *Start*, *Length*, *ThisTextExpression*)</span></span> 
  
<span data-ttu-id="6fb5c-111">Die **stuff** -Funktion enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="6fb5c-111">The **Stuff** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="6fb5c-112">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="6fb5c-112">**Argument name**</span></span>|<span data-ttu-id="6fb5c-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6fb5c-113">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="6fb5c-114">*IntoTextExpression*</span><span class="sxs-lookup"><span data-stu-id="6fb5c-114">*IntoTextExpression*</span></span>  <br/> |<span data-ttu-id="6fb5c-115">Ein Textausdruck, der den Text angibt, in den der durch das *ThisTextExpression* angegebene Text eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="6fb5c-115">A text expression that specifies the text into which the text specified by the  *ThisTextExpression*  will be inserted.</span></span>  <br/> |
| <span data-ttu-id="6fb5c-116">*Start*</span><span class="sxs-lookup"><span data-stu-id="6fb5c-116">*Start*</span></span>  <br/> |<span data-ttu-id="6fb5c-117">Ein ganzzahliger Wert, der die Position angibt, zu der gelöscht und eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6fb5c-117">An integer value that specifies the location to start deletion and insertion.</span></span> <span data-ttu-id="6fb5c-118">Wenn Start oder length negativ ist, wird eine NULL-Zeichenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6fb5c-118">If start or length is negative, a null string is returned.</span></span> <span data-ttu-id="6fb5c-119">Wenn Start länger als der erste *IntoTextExpression* ist, wird eine NULL-Zeichenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6fb5c-119">If start is longer than the first  *IntoTextExpression*  , a null string is returned.</span></span>  <br/> |
| <span data-ttu-id="6fb5c-120">*Length*</span><span class="sxs-lookup"><span data-stu-id="6fb5c-120">*Length*</span></span>  <br/> |<span data-ttu-id="6fb5c-121">Eine ganze Zahl, die die Anzahl der zu löschenden Zeichen angibt.</span><span class="sxs-lookup"><span data-stu-id="6fb5c-121">An integer that specifies the number of characters to delete.</span></span> <span data-ttu-id="6fb5c-122">Wenn length länger als der erste *IntoTextExpression* ist, wird der Löschvorgang bis zum letzten Zeichen im letzten *IntoTextExpression* ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6fb5c-122">If length is longer than the first  *IntoTextExpression*  , deletion occurs up to the last character in the last  *IntoTextExpression*  .</span></span>  <br/> |
| <span data-ttu-id="6fb5c-123">*ThisTextExpression*</span><span class="sxs-lookup"><span data-stu-id="6fb5c-123">*ThisTextExpression*</span></span>  <br/> |<span data-ttu-id="6fb5c-124">Ein Text Ausdrucks-Hut gibt den Text an, der in *IntoTextExpression* eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6fb5c-124">A text expression hat specifies the text to insert into  *IntoTextExpression*  .</span></span> <span data-ttu-id="6fb5c-125">Dieser Ausdruck ersetzt die Länge der Zeichen von *IntoTextExpression* , die am Anfang *beginnen* .</span><span class="sxs-lookup"><span data-stu-id="6fb5c-125">This expression will replace length characters of  *IntoTextExpression*  beginning at  *Start*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6fb5c-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6fb5c-126">Remarks</span></span>

<span data-ttu-id="6fb5c-127">Wenn die Argumente *Start* oder *length* negativ sind oder wenn die Anfangsposition größer als die Länge der ersten Zeichenfolge ist, wird eine NULL-Zeichenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6fb5c-127">If the  *Start*  or  *Length*  arguments are negative, or if the starting position is larger than length of the first string, a null string is returned.</span></span> <span data-ttu-id="6fb5c-128">Wenn die Startposition 0 ist, wird ein NULL-Wert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6fb5c-128">If the start position is 0, a null value is returned.</span></span> <span data-ttu-id="6fb5c-129">Wenn die zu löschende Länge länger als die erste Zeichenfolge ist, wird Sie in das erste Zeichen in der ersten Zeichenfolge gelöscht.</span><span class="sxs-lookup"><span data-stu-id="6fb5c-129">If the length to delete is longer than the first string, it is deleted to the first character in the first string.</span></span> 
  

