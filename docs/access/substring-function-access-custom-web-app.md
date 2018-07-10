---
title: Teilzeichenfolgefunktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae99a0fa-76c4-4c07-9ae9-a7abce23394f
description: Teil eines Ausdrucks Text zurückgegeben.
ms.openlocfilehash: 49d9afefe4b25d91738e518e0ddb2b902067c038
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790375"
---
# <a name="substring-function-access-custom-web-app"></a><span data-ttu-id="d7ad0-103">Teilzeichenfolgefunktion (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="d7ad0-103">SubString Function (Access custom web app)</span></span>

<span data-ttu-id="d7ad0-104">Teil eines Ausdrucks Text zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d7ad0-104">Returns part of a text expression.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="d7ad0-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/de-de/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="d7ad0-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/de-de/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d7ad0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7ad0-107">Syntax</span></span>

 <span data-ttu-id="d7ad0-108">**Teilzeichenfolge** (*TextExpression*, *Starten*, *Länge*)</span><span class="sxs-lookup"><span data-stu-id="d7ad0-108">**SubString** (*TextExpression*, *Start*, *Length*)</span></span> 
  
<span data-ttu-id="d7ad0-109">Die **Teilzeichenfolge** -Funktion enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="d7ad0-109">The **SubString** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="d7ad0-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="d7ad0-110">**Argument name**</span></span>|<span data-ttu-id="d7ad0-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="d7ad0-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="d7ad0-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="d7ad0-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="d7ad0-113">Ein Textausdruck.</span><span class="sxs-lookup"><span data-stu-id="d7ad0-113">A text expression.</span></span>  <br/> |
| <span data-ttu-id="d7ad0-114">*Start*</span><span class="sxs-lookup"><span data-stu-id="d7ad0-114">*Start*</span></span>  <br/> |<span data-ttu-id="d7ad0-115">Ein Integer-Ausdruck, der angibt, an dem die zurückgegebenen Zeichen beginnen.</span><span class="sxs-lookup"><span data-stu-id="d7ad0-115">An integer expression that specifies where the returned characters start.</span></span> <span data-ttu-id="d7ad0-116">Wenn Start kleiner als 1 ist, beginnt der zurückgegebene Ausdruck mit dem ersten Zeichen, die im Ausdruck angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="d7ad0-116">If start is less than 1, the returned expression will begin at the first character that is specified in expression.</span></span> <span data-ttu-id="d7ad0-117">In diesem Fall ist die Anzahl der Zeichen, die zurückgegeben werden, den größten Wert entweder die Summe der Start + Length-1 oder 0.</span><span class="sxs-lookup"><span data-stu-id="d7ad0-117">In this case, the number of characters that are returned is the largest value of either the sum of start + length- 1 or 0.</span></span> <span data-ttu-id="d7ad0-118">Wenn Start größer als die Anzahl der Zeichen im Wertausdruck ist, wird ein leere Ausdruck zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d7ad0-118">If start is greater than the number of characters in the value expression, a zero-length expression is returned.</span></span>  <br/> |
| <span data-ttu-id="d7ad0-119">*Length*</span><span class="sxs-lookup"><span data-stu-id="d7ad0-119">*Length*</span></span>  <br/> |<span data-ttu-id="d7ad0-120">Eine positive ganze Zahl-Ausdruck, der angibt, wie viele Zeichen des Ausdrucks zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d7ad0-120">A positive integer expression that specifies how many characters of the expression will be returned.</span></span> <span data-ttu-id="d7ad0-121">Wenn Length negativ ist, wird ein Fehler generiert, und die Anweisung wird beendet.</span><span class="sxs-lookup"><span data-stu-id="d7ad0-121">If length is negative, an error is generated and the statement is terminated.</span></span> <span data-ttu-id="d7ad0-122">Ist die Summe der Start als auch Length größer als die Anzahl der Zeichen im Ausdruck ist, wird der gesamten Wert Ausdruck Anfang am Anfang zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d7ad0-122">If the sum of start and length is greater than the number of characters in expression, the whole value expression beginning at start is returned.</span></span>  <br/> |
   

