---
title: Dinge-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4d8d6a34-f884-40a4-b330-5c104d16cf97
description: Fügt eine Textzeichenfolge in einer anderen Zeichenfolge. Löscht eine angegebene Anzahl von Zeichen in der ersten Zeichenfolge an der Startposition und klicken Sie dann in der ersten Zeichenfolge an der Startposition die zweite Zeichenfolge eingefügt.
ms.openlocfilehash: 5540bb5936803370835a0c3d80b420edc13d0de6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790363"
---
# <a name="stuff-function-access-custom-web-app"></a><span data-ttu-id="c0c5d-104">Dinge-Funktion (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="c0c5d-104">Stuff Function (Access custom web app)</span></span>

<span data-ttu-id="c0c5d-105">Fügt eine Textzeichenfolge in einer anderen Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="c0c5d-105">Inserts a text string into another text string.</span></span> <span data-ttu-id="c0c5d-106">Löscht eine angegebene Anzahl von Zeichen in der ersten Zeichenfolge an der Startposition und klicken Sie dann in der ersten Zeichenfolge an der Startposition die zweite Zeichenfolge eingefügt.</span><span class="sxs-lookup"><span data-stu-id="c0c5d-106">It deletes a specified length of characters in the first string at the start position and then inserts the second string into the first string at the start position.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="c0c5d-p103">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/de-de/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="c0c5d-p103">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/de-de/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c0c5d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0c5d-109">Syntax</span></span>

 <span data-ttu-id="c0c5d-110">**Sammlung (engl.)** (*IntoTextExpression*, *Starten*, *Länge*, *ThisTextExpression*)</span><span class="sxs-lookup"><span data-stu-id="c0c5d-110">**Stuff** (*IntoTextExpression*, *Start*, *Length*, *ThisTextExpression*)</span></span> 
  
<span data-ttu-id="c0c5d-111">Die **Dinge** -Funktion enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="c0c5d-111">The **Stuff** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="c0c5d-112">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="c0c5d-112">**Argument name**</span></span>|<span data-ttu-id="c0c5d-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="c0c5d-113">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="c0c5d-114">*IntoTextExpression*</span><span class="sxs-lookup"><span data-stu-id="c0c5d-114">*IntoTextExpression*</span></span>  <br/> |<span data-ttu-id="c0c5d-115">Ein Ausdruck, der den Text angibt, in dem der durch die *ThisTextExpression* angegebene Text eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="c0c5d-115">A text expression that specifies the text into which the text specified by the  *ThisTextExpression*  will be inserted.</span></span>  <br/> |
| <span data-ttu-id="c0c5d-116">*Start*</span><span class="sxs-lookup"><span data-stu-id="c0c5d-116">*Start*</span></span>  <br/> |<span data-ttu-id="c0c5d-117">Ein Ganzzahlwert, der den Speicherort zum Löschen und Einfügen begonnen angibt.</span><span class="sxs-lookup"><span data-stu-id="c0c5d-117">An integer value that specifies the location to start deletion and insertion.</span></span> <span data-ttu-id="c0c5d-118">Wenn Start oder Length negativ ist, wird eine null-Zeichenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c0c5d-118">If start or length is negative, a null string is returned.</span></span> <span data-ttu-id="c0c5d-119">Wenn Start länger als die erste *IntoTextExpression* ist, wird eine null-Zeichenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c0c5d-119">If start is longer than the first  *IntoTextExpression*  , a null string is returned.</span></span>  <br/> |
| <span data-ttu-id="c0c5d-120">*Length*</span><span class="sxs-lookup"><span data-stu-id="c0c5d-120">*Length*</span></span>  <br/> |<span data-ttu-id="c0c5d-121">Eine ganze Zahl, die die Anzahl der zu löschenden Zeichen angibt.</span><span class="sxs-lookup"><span data-stu-id="c0c5d-121">An integer that specifies the number of characters to delete.</span></span> <span data-ttu-id="c0c5d-122">Wenn Length länger als die erste *IntoTextExpression* ist, erfolgt die Löschung bis zum letzten Zeichen in der letzten *IntoTextExpression* .</span><span class="sxs-lookup"><span data-stu-id="c0c5d-122">If length is longer than the first  *IntoTextExpression*  , deletion occurs up to the last character in the last  *IntoTextExpression*  .</span></span>  <br/> |
| <span data-ttu-id="c0c5d-123">*ThisTextExpression*</span><span class="sxs-lookup"><span data-stu-id="c0c5d-123">*ThisTextExpression*</span></span>  <br/> |<span data-ttu-id="c0c5d-124">Hat einen Text-Ausdruck gibt den Text in *IntoTextExpression* einfügen.</span><span class="sxs-lookup"><span data-stu-id="c0c5d-124">A text expression hat specifies the text to insert into  *IntoTextExpression*  .</span></span> <span data-ttu-id="c0c5d-125">Dieser Ausdruck ersetzt Length Zeichen des *IntoTextExpression* , beginnend am *Starten* .</span><span class="sxs-lookup"><span data-stu-id="c0c5d-125">This expression will replace length characters of  *IntoTextExpression*  beginning at  *Start*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c0c5d-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c0c5d-126">Remarks</span></span>

<span data-ttu-id="c0c5d-127">Wenn die Argumente *Start* oder *Length* negativ sind oder die Startposition größer als die Länge der ersten Zeichenfolge ist, wird eine leere Zeichenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c0c5d-127">If the  *Start*  or  *Length*  arguments are negative, or if the starting position is larger than length of the first string, a null string is returned.</span></span> <span data-ttu-id="c0c5d-128">Wenn die Startposition 0 ist, wird ein Nullwert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c0c5d-128">If the start position is 0, a null value is returned.</span></span> <span data-ttu-id="c0c5d-129">Wenn die Länge zu löschenden länger als die erste Zeichenfolge ist, wird es auf das erste Zeichen in der ersten Zeichenfolge gelöscht.</span><span class="sxs-lookup"><span data-stu-id="c0c5d-129">If the length to delete is longer than the first string, it is deleted to the first character in the first string.</span></span> 
  

