---
title: Stuff-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4d8d6a34-f884-40a4-b330-5c104d16cf97
description: Fügt eine Textzeichenfolge in eine andere Textzeichenfolge ein. Es löscht eine angegebene Länge von Zeichen in der ersten Zeichenfolge an der Startposition und fügt dann die zweite Zeichenfolge in die erste Zeichenfolge an der Startposition ein.
ms.openlocfilehash: 591823952faa0d593b6db1f5bfb00cc68a894a8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427675"
---
# <a name="stuff-function-access-custom-web-app"></a><span data-ttu-id="a1852-104">Stuff-Funktion (benutzerdefinierte Access-Web-App)</span><span class="sxs-lookup"><span data-stu-id="a1852-104">Stuff Function (Access custom web app)</span></span>

<span data-ttu-id="a1852-105">Fügt eine Textzeichenfolge in eine andere Textzeichenfolge ein.</span><span class="sxs-lookup"><span data-stu-id="a1852-105">Inserts a text string into another text string.</span></span> <span data-ttu-id="a1852-106">Es löscht eine angegebene Länge von Zeichen in der ersten Zeichenfolge an der Startposition und fügt dann die zweite Zeichenfolge in die erste Zeichenfolge an der Startposition ein.</span><span class="sxs-lookup"><span data-stu-id="a1852-106">It deletes a specified length of characters in the first string at the start position and then inserts the second string into the first string at the start position.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="a1852-p103">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="a1852-p103">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a1852-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1852-109">Syntax</span></span>

 <span data-ttu-id="a1852-110">**Stuff** (*IntoTextExpression*, *Start*, *Length*, *ThisTextExpression*)</span><span class="sxs-lookup"><span data-stu-id="a1852-110">**Stuff** (*IntoTextExpression*, *Start*, *Length*, *ThisTextExpression*)</span></span> 
  
<span data-ttu-id="a1852-111">Die **Stuff-Funktion** enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="a1852-111">The **Stuff** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="a1852-112">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="a1852-112">**Argument name**</span></span>|<span data-ttu-id="a1852-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a1852-113">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="a1852-114">*IntoTextExpression*</span><span class="sxs-lookup"><span data-stu-id="a1852-114">*IntoTextExpression*</span></span>  <br/> |<span data-ttu-id="a1852-115">Ein Textausdruck, der den Text angibt, in den der durch  *thisTextExpression*  angegebene Text eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="a1852-115">A text expression that specifies the text into which the text specified by the  *ThisTextExpression*  will be inserted.</span></span>  <br/> |
| <span data-ttu-id="a1852-116">*Start*</span><span class="sxs-lookup"><span data-stu-id="a1852-116">*Start*</span></span>  <br/> |<span data-ttu-id="a1852-117">Ein ganzzahliger Wert, der die Position angibt, an der das Löschen und Einfügen gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a1852-117">An integer value that specifies the location to start deletion and insertion.</span></span> <span data-ttu-id="a1852-118">Wenn Start oder Länge negativ ist, wird eine Nullzeichenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a1852-118">If start or length is negative, a null string is returned.</span></span> <span data-ttu-id="a1852-119">Wenn start länger als der erste  *IntoTextExpression*  ist, wird eine Nullzeichenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a1852-119">If start is longer than the first  *IntoTextExpression*  , a null string is returned.</span></span>  <br/> |
| <span data-ttu-id="a1852-120">*Length*</span><span class="sxs-lookup"><span data-stu-id="a1852-120">*Length*</span></span>  <br/> |<span data-ttu-id="a1852-121">Eine ganze Zahl, die die Anzahl der zu löschenden Zeichen angibt.</span><span class="sxs-lookup"><span data-stu-id="a1852-121">An integer that specifies the number of characters to delete.</span></span> <span data-ttu-id="a1852-122">Wenn die Länge länger als das erste *IntoTextExpression-Objekt ist,* erfolgt das Löschen bis zum letzten Zeichen im letzten *IntoTextExpression -Objekt.*</span><span class="sxs-lookup"><span data-stu-id="a1852-122">If length is longer than the first  *IntoTextExpression*  , deletion occurs up to the last character in the last  *IntoTextExpression*  .</span></span>  <br/> |
| <span data-ttu-id="a1852-123">*ThisTextExpression*</span><span class="sxs-lookup"><span data-stu-id="a1852-123">*ThisTextExpression*</span></span>  <br/> |<span data-ttu-id="a1852-124">Ein Textausdruckshut gibt den Text an, der in *IntoTextExpression eingefügt werden soll.*</span><span class="sxs-lookup"><span data-stu-id="a1852-124">A text expression hat specifies the text to insert into  *IntoTextExpression*  .</span></span> <span data-ttu-id="a1852-125">Dieser Ausdruck ersetzt Längenzeichen von *IntoTextExpression, die* bei *Start beginnen.*</span><span class="sxs-lookup"><span data-stu-id="a1852-125">This expression will replace length characters of  *IntoTextExpression*  beginning at  *Start*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a1852-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a1852-126">Remarks</span></span>

<span data-ttu-id="a1852-127">Wenn die  *Argumente Start*  oder  *Length*  negativ sind oder die Anfangsposition größer als die Länge der ersten Zeichenfolge ist, wird eine Nullzeichenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a1852-127">If the  *Start*  or  *Length*  arguments are negative, or if the starting position is larger than length of the first string, a null string is returned.</span></span> <span data-ttu-id="a1852-128">Wenn die Startposition 0 ist, wird ein Nullwert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a1852-128">If the start position is 0, a null value is returned.</span></span> <span data-ttu-id="a1852-129">Wenn die zu löschende Länge länger als die erste Zeichenfolge ist, wird sie in das erste Zeichen in der ersten Zeichenfolge gelöscht.</span><span class="sxs-lookup"><span data-stu-id="a1852-129">If the length to delete is longer than the first string, it is deleted to the first character in the first string.</span></span> 
  

