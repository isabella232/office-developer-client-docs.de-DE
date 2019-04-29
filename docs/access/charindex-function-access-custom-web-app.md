---
title: CharIndex-Funktion (Access Custom Web App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 340ed9a8-6f82-4aa8-a951-2c453b3d1ac4
description: Durchsucht einen Textausdruck nach einem anderen Textausdruck und gibt seine Ausgangsposition zurück, falls gefunden.
ms.openlocfilehash: dc6906f70bc5bb17e12855d69946281909962988
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423132"
---
# <a name="charindex-function-access-custom-web-app"></a><span data-ttu-id="9b724-103">CharIndex-Funktion (Access Custom Web App)</span><span class="sxs-lookup"><span data-stu-id="9b724-103">CharIndex function (Access custom web app)</span></span>

<span data-ttu-id="9b724-104">Durchsucht einen Textausdruck nach einem anderen Textausdruck und gibt seine Ausgangsposition zurück, falls gefunden.</span><span class="sxs-lookup"><span data-stu-id="9b724-104">Searches a text expression for another text expression and returns its starting position if found.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="9b724-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="9b724-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9b724-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b724-107">Syntax</span></span>

<span data-ttu-id="9b724-108">**CHARINDEX** (*Text*-, *WithinText*-, [*Start*])</span><span class="sxs-lookup"><span data-stu-id="9b724-108">**CharIndex** (*TextExpression*, *WithinText*, [*Start*])</span></span> 
  
|<span data-ttu-id="9b724-109">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="9b724-109">**Argument Name**</span></span>|<span data-ttu-id="9b724-110">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="9b724-110">**Required**</span></span>|<span data-ttu-id="9b724-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9b724-111">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="9b724-112">*Text*</span><span class="sxs-lookup"><span data-stu-id="9b724-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="9b724-113">Ja</span><span class="sxs-lookup"><span data-stu-id="9b724-113">Yes</span></span>  <br/> |<span data-ttu-id="9b724-114">Ein Textausdruck, der den gefundenen Text enthält.</span><span class="sxs-lookup"><span data-stu-id="9b724-114">A text expression that contains the text to be found.</span></span>  <br/> |
| <span data-ttu-id="9b724-115">*WithinText*</span><span class="sxs-lookup"><span data-stu-id="9b724-115">*WithinText*</span></span>  <br/> |<span data-ttu-id="9b724-116">Ja</span><span class="sxs-lookup"><span data-stu-id="9b724-116">Yes</span></span>  <br/> |<span data-ttu-id="9b724-117">Der Textausdruck, der durchsucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="9b724-117">The text expression to be searched.</span></span>  <br/> |
| <span data-ttu-id="9b724-118">*Start*</span><span class="sxs-lookup"><span data-stu-id="9b724-118">*Start*</span></span>  <br/> |<span data-ttu-id="9b724-119">Nein</span><span class="sxs-lookup"><span data-stu-id="9b724-119">No</span></span>  <br/> |<span data-ttu-id="9b724-120">Eine ganze Zahl, die den Speicherort in *WithinText* angibt, an dem die Suche beginnen soll.</span><span class="sxs-lookup"><span data-stu-id="9b724-120">An integer that specifies the location in  *WithinText*  to begin the search.</span></span> <span data-ttu-id="9b724-121">Wenn *Start* nicht angegeben ist, eine negative Zahl ist oder 0 ist, beginnt die Suche am Anfang von *WithinText* .</span><span class="sxs-lookup"><span data-stu-id="9b724-121">If  *Start*  is not specified, is a negative number, or is 0, the search starts at the beginning of  *WithinText*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9b724-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b724-122">Remarks</span></span>

<span data-ttu-id="9b724-123">Wenn *Text* -oder *WithinText* ist, gibt *CHARINDEX* NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="9b724-123">If either  *TextExpression*  or  *WithinText*  is NULL,  *CharIndex*  returns NULL.</span></span> 
  
<span data-ttu-id="9b724-124">Wenn *Textform* in *WithinText*nicht gefunden wird, gibt *CHARINDEX* 0 zurück.</span><span class="sxs-lookup"><span data-stu-id="9b724-124">If  *TextExpression*  is not found within  *WithinText*,  *CharIndex*  returns 0.</span></span> 
  
<span data-ttu-id="9b724-125">Die zurückgegebene Startposition ist 1-basiert, nicht 0-basiert.</span><span class="sxs-lookup"><span data-stu-id="9b724-125">The starting position returned is 1-based, not 0-based.</span></span>
  

