---
title: SUBSTRING-Funktion (Access Custom Web App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae99a0fa-76c4-4c07-9ae9-a7abce23394f
description: Gibt einen Teil eines Text Ausdrucks zurück.
ms.openlocfilehash: af93620905af366f41bcc50ab6102114acd3db9f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433472"
---
# <a name="substring-function-access-custom-web-app"></a><span data-ttu-id="d4106-103">SUBSTRING-Funktion (Access Custom Web App)</span><span class="sxs-lookup"><span data-stu-id="d4106-103">SubString Function (Access custom web app)</span></span>

<span data-ttu-id="d4106-104">Gibt einen Teil eines Text Ausdrucks zurück.</span><span class="sxs-lookup"><span data-stu-id="d4106-104">Returns part of a text expression.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="d4106-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="d4106-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d4106-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4106-107">Syntax</span></span>

 <span data-ttu-id="d4106-108">Teil **Zeichenfolge** (*Text*-, *Start*-, *Länge*)</span><span class="sxs-lookup"><span data-stu-id="d4106-108">**SubString** (*TextExpression*, *Start*, *Length*)</span></span> 
  
<span data-ttu-id="d4106-109">Die **SUBSTRING** -Funktion enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="d4106-109">The **SubString** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="d4106-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="d4106-110">**Argument name**</span></span>|<span data-ttu-id="d4106-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d4106-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="d4106-112">*Text*</span><span class="sxs-lookup"><span data-stu-id="d4106-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="d4106-113">Ein Textausdruck.</span><span class="sxs-lookup"><span data-stu-id="d4106-113">A text expression.</span></span>  <br/> |
| <span data-ttu-id="d4106-114">*Start*</span><span class="sxs-lookup"><span data-stu-id="d4106-114">*Start*</span></span>  <br/> |<span data-ttu-id="d4106-115">Ein ganzzahliger Ausdruck, der angibt, wo die zurückgegebenen Zeichen beginnen.</span><span class="sxs-lookup"><span data-stu-id="d4106-115">An integer expression that specifies where the returned characters start.</span></span> <span data-ttu-id="d4106-116">Wenn Start kleiner als 1 ist, beginnt der zurückgegebene Ausdruck mit dem ersten Zeichen, das in Expression angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="d4106-116">If start is less than 1, the returned expression will begin at the first character that is specified in expression.</span></span> <span data-ttu-id="d4106-117">In diesem Fall ist die Anzahl der zurückgegebenen Zeichen der größte Wert der Summe von Start + Länge-1 oder 0.</span><span class="sxs-lookup"><span data-stu-id="d4106-117">In this case, the number of characters that are returned is the largest value of either the sum of start + length- 1 or 0.</span></span> <span data-ttu-id="d4106-118">Wenn Start größer ist als die Anzahl der Zeichen im Wertausdruck, wird ein Ausdruck mit der Länge Null zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d4106-118">If start is greater than the number of characters in the value expression, a zero-length expression is returned.</span></span>  <br/> |
| <span data-ttu-id="d4106-119">*Length*</span><span class="sxs-lookup"><span data-stu-id="d4106-119">*Length*</span></span>  <br/> |<span data-ttu-id="d4106-120">Ein positiver ganzzahliger Ausdruck, der angibt, wie viele Zeichen des Ausdrucks zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d4106-120">A positive integer expression that specifies how many characters of the expression will be returned.</span></span> <span data-ttu-id="d4106-121">Wenn length negativ ist, wird ein Fehler generiert, und die Anweisung wird beendet.</span><span class="sxs-lookup"><span data-stu-id="d4106-121">If length is negative, an error is generated and the statement is terminated.</span></span> <span data-ttu-id="d4106-122">Wenn die Summe von Start und length größer als die Anzahl der Zeichen in Expression ist, wird der gesamte Wertausdruck, der bei Start beginnt, zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d4106-122">If the sum of start and length is greater than the number of characters in expression, the whole value expression beginning at start is returned.</span></span>  <br/> |
   

