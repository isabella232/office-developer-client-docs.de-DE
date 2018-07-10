---
title: '[NOT] ist NULL (Access benutzerdefinierte Web app)'
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b941a0c7-9753-4920-bb6d-cbba94ba9422
description: Bestimmt, ob ein bestimmter Ausdruck gleich NULL ist.
ms.openlocfilehash: fcbceb1e8edac65fe232ba9c2b12195b99db9545
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790206"
---
# <a name="is-not-null-access-custom-web-app"></a><span data-ttu-id="f06b0-103">[NOT] ist NULL (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="f06b0-103">IS [NOT] NULL (Access custom web app)</span></span>

<span data-ttu-id="f06b0-104">Bestimmt, ob ein bestimmter Ausdruck gleich NULL ist.</span><span class="sxs-lookup"><span data-stu-id="f06b0-104">Determines whether a specified expression is NULL.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="f06b0-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/de-de/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="f06b0-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/de-de/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f06b0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f06b0-107">Syntax</span></span>

 <span data-ttu-id="f06b0-108">*Ausdruck* **IS** [ *Nicht* ] **NULL**</span><span class="sxs-lookup"><span data-stu-id="f06b0-108">*expression* **IS** [  *NOT*  ] **NULL**</span></span>
  
<span data-ttu-id="f06b0-109">Die **IS [NOT] NULL** Prädikat enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="f06b0-109">The **IS [NOT] NULL** predicate contains the following arguments.</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f06b0-110">*expression*</span><span class="sxs-lookup"><span data-stu-id="f06b0-110">*expression*</span></span>  <br/> |<span data-ttu-id="f06b0-111">Ein beliebiger gültiger Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="f06b0-111">Any valid expression.</span></span>  <br/> |
| <span data-ttu-id="f06b0-112">*NOT*</span><span class="sxs-lookup"><span data-stu-id="f06b0-112">*NOT*</span></span>  <br/> |<span data-ttu-id="f06b0-113">Gibt an, dass das boolesche Ergebnis negiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f06b0-113">Specifies that the Boolean result be negated.</span></span> <span data-ttu-id="f06b0-114">Das Prädikat kehrt die Rückgabewerte, gibt TRUE zurück, wenn der Wert nicht NULL ist, und FALSE, wenn der Wert NULL ist.</span><span class="sxs-lookup"><span data-stu-id="f06b0-114">The predicate reverses its return values, returning TRUE if the value is not NULL, and FALSE if the value is NULL.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f06b0-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f06b0-115">Remarks</span></span>

<span data-ttu-id="f06b0-116">Wenn der Wert des *Ausdrucks* NULL ist, ISTNULL wird TRUE zurückgegeben. Andernfalls wird FALSE zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f06b0-116">If the value of  *expression*  is NULL, IS NULL returns TRUE; otherwise, it returns FALSE.</span></span> 
  
<span data-ttu-id="f06b0-117">Wenn der Wert des Ausdrucks NULL ist, gibt IS NOT NULL FALSE zurück. Andernfalls wird TRUE zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f06b0-117">If the value of expression is NULL, IS NOT NULL returns FALSE; otherwise, it returns TRUE.</span></span>
  

