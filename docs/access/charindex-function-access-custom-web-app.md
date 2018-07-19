---
title: CharIndex-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 340ed9a8-6f82-4aa8-a951-2c453b3d1ac4
description: Suchvorgänge gefunden ein Textausdruck für einen anderen Ausdruck und gibt dessen Start-positionieren, wenn.
ms.openlocfilehash: 86a46f57c64028530217326127eece887127c4c3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790214"
---
# <a name="charindex-function-access-custom-web-app"></a><span data-ttu-id="56d5c-103">CharIndex-Funktion (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="56d5c-103">CharIndex function (Access custom web app)</span></span>

<span data-ttu-id="56d5c-104">Suchvorgänge gefunden ein Textausdruck für einen anderen Ausdruck und gibt dessen Start-positionieren, wenn.</span><span class="sxs-lookup"><span data-stu-id="56d5c-104">Searches a text expression for another text expression and returns its starting position if found.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="56d5c-p101"> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/de-de/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="56d5c-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/de-de/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="56d5c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="56d5c-107">Syntax</span></span>

<span data-ttu-id="56d5c-108">**CharIndex** (*TextExpression*, *WithinText*, [*Start*])</span><span class="sxs-lookup"><span data-stu-id="56d5c-108">**CharIndex** (*TextExpression*, *WithinText*, [*Start*])</span></span> 
  
|<span data-ttu-id="56d5c-109">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="56d5c-109">**Argument Name**</span></span>|<span data-ttu-id="56d5c-110">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="56d5c-110">**Required**</span></span>|<span data-ttu-id="56d5c-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="56d5c-111">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="56d5c-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="56d5c-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="56d5c-113">Ja</span><span class="sxs-lookup"><span data-stu-id="56d5c-113">Yes</span></span>  <br/> |<span data-ttu-id="56d5c-114">Ein Ausdruck, der den gesuchten Text enthält.</span><span class="sxs-lookup"><span data-stu-id="56d5c-114">A text expression that contains the text to be found.</span></span>  <br/> |
| <span data-ttu-id="56d5c-115">*WithinText*</span><span class="sxs-lookup"><span data-stu-id="56d5c-115">*WithinText*</span></span>  <br/> |<span data-ttu-id="56d5c-116">Ja</span><span class="sxs-lookup"><span data-stu-id="56d5c-116">Yes</span></span>  <br/> |<span data-ttu-id="56d5c-117">Der Textausdruck, der durchsucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="56d5c-117">The text expression to be searched.</span></span>  <br/> |
| <span data-ttu-id="56d5c-118">*Start*</span><span class="sxs-lookup"><span data-stu-id="56d5c-118">*Start*</span></span>  <br/> |<span data-ttu-id="56d5c-119">Nein</span><span class="sxs-lookup"><span data-stu-id="56d5c-119">No</span></span>  <br/> |<span data-ttu-id="56d5c-120">Eine ganze Zahl, die den Speicherort in *WithinText* zum Starten der Suche angibt.</span><span class="sxs-lookup"><span data-stu-id="56d5c-120">An integer that specifies the location in  *WithinText*  to begin the search.</span></span> <span data-ttu-id="56d5c-121">Wenn *Starten* nicht angegeben ist, eine negative Zahl ist oder 0 ist, beginnt die Suche am Anfang des *WithinText* .</span><span class="sxs-lookup"><span data-stu-id="56d5c-121">If  *Start*  is not specified, is a negative number, or is 0, the search starts at the beginning of  *WithinText*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="56d5c-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56d5c-122">Remarks</span></span>

<span data-ttu-id="56d5c-123">Wenn *TextExpression* oder *WithinText* NULL ist, gibt *CharIndex* NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="56d5c-123">If either  *TextExpression*  or  *WithinText*  is NULL,  *CharIndex*  returns NULL.</span></span> 
  
<span data-ttu-id="56d5c-124">*TextExpression* in *WithinText*nicht gefunden wird, gibt *CharIndex* 0 zurück.</span><span class="sxs-lookup"><span data-stu-id="56d5c-124">If  *TextExpression*  is not found within  *WithinText*,  *CharIndex*  returns 0.</span></span> 
  
<span data-ttu-id="56d5c-125">Die Anfangsposition zurückgegeben ist 1-basierter, nicht 0-basiert.</span><span class="sxs-lookup"><span data-stu-id="56d5c-125">The starting position returned is 1-based, not 0-based.</span></span>
  

