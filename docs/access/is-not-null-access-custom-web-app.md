---
title: IS [NOT] NULL (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.assetid: b941a0c7-9753-4920-bb6d-cbba94ba9422
description: Bestimmt, ob ein angegebener Ausdruck NULL ist.
localization_priority: Priority
ms.openlocfilehash: fe6a0fe4f182a1385304b783e7cfaaf515f732d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311137"
---
# <a name="is-not-null-access-custom-web-app"></a><span data-ttu-id="63f24-103">IS [NOT] NULL (benutzerdefinierte Access-Web-App)</span><span class="sxs-lookup"><span data-stu-id="63f24-103">IS [NOT] NULL (Access custom web app)</span></span>

<span data-ttu-id="63f24-104">Bestimmt, ob ein angegebener Ausdruck NULL ist.</span><span class="sxs-lookup"><span data-stu-id="63f24-104">Determines whether a specified expression is NULL.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="63f24-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="63f24-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="63f24-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="63f24-107">Syntax</span></span>

 <span data-ttu-id="63f24-108">*expression* **IS** [  *NOT*  ] **NULL**</span><span class="sxs-lookup"><span data-stu-id="63f24-108">*expression* **IS** [  *NOT*  ] **NULL**</span></span>
  
<span data-ttu-id="63f24-109">Das Prädikat **IS [NOT] NULL** enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="63f24-109">The **IS [NOT] NULL** predicate contains the following arguments.</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="63f24-110">*expression*</span><span class="sxs-lookup"><span data-stu-id="63f24-110">*expression*</span></span>  <br/> |<span data-ttu-id="63f24-111">Jeder gültige Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="63f24-111">Any valid expression.</span></span>  <br/> |
| <span data-ttu-id="63f24-112">*NOT*</span><span class="sxs-lookup"><span data-stu-id="63f24-112">*NOT*</span></span>  <br/> |<span data-ttu-id="63f24-113">Gibt an, dass das boolesche Ergebnis negiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="63f24-113">Specifies that the Boolean result be negated.</span></span> <span data-ttu-id="63f24-114">Das Prädikat kehrt die Rückgabewerte um, sodass TRUE zurückgegeben wird, wenn der Wert nicht NULL ist, und FALSE, wenn der Wert NULL ist.</span><span class="sxs-lookup"><span data-stu-id="63f24-114">The predicate reverses its return values, returning TRUE if the value is not NULL, and FALSE if the value is NULL.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="63f24-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="63f24-115">Remarks</span></span>

<span data-ttu-id="63f24-116">Wenn der Wert von *expression* NULL ist, gibt IS NULL „TRUE“ zurück; andernfalls wird „FALSE“ zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="63f24-116">If the value of  *expression*  is NULL, IS NULL returns TRUE; otherwise, it returns FALSE.</span></span> 
  
<span data-ttu-id="63f24-117">Wenn der Wert von expression NULL ist, gibt IS NULL „FALSE“ zurück; andernfalls wird „TRUE“ zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="63f24-117">If the value of expression is NULL, IS NOT NULL returns FALSE; otherwise, it returns TRUE.</span></span>
  

