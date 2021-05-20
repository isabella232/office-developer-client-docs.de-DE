---
title: Var-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cb2aace1-fa2d-480e-bfc7-44ae399943f5
description: Gibt die statistische Varianz für eine Grundgesamtheitsstichprobe zurück, die als Wertesatz in einem angegebenen Feld in einer Abfrage dargestellt wird.
ms.openlocfilehash: 80cea512b0386d9b0461c927675ae51be3e0dcda
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437756"
---
# <a name="var-function-access-custom-web-app"></a><span data-ttu-id="19f98-103">Var-Funktion (benutzerdefinierte Access-Web-App)</span><span class="sxs-lookup"><span data-stu-id="19f98-103">Var Function (Access custom web app)</span></span>

<span data-ttu-id="19f98-104">Gibt die statistische Varianz für eine Grundgesamtheitsstichprobe zurück, die als Wertesatz in einem angegebenen Feld in einer Abfrage dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="19f98-104">Returns the statistical variance for a population sample represented as a set of values contained in a specified field in a query.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="19f98-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="19f98-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="19f98-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="19f98-107">Syntax</span></span>

 <span data-ttu-id="19f98-108">**Var** (*NumericExpression*)</span><span class="sxs-lookup"><span data-stu-id="19f98-108">**Var** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="19f98-109">Die **Var-Funktion** enthält das folgende Argument.</span><span class="sxs-lookup"><span data-stu-id="19f98-109">The **Var** function contains the following argument.</span></span> 
  
|<span data-ttu-id="19f98-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="19f98-110">**Argument name**</span></span>|<span data-ttu-id="19f98-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="19f98-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="19f98-112">*NumericExpression*</span><span class="sxs-lookup"><span data-stu-id="19f98-112">*NumericExpression*</span></span>  <br/> |<span data-ttu-id="19f98-113">Ein Textausdruck, der das Feld identifiziert, das die numerischen Daten enthält, die Ausgewertet werden sollen, oder ein Ausdruck, der eine Berechnung mit den Daten in diesem Feld ausführt.</span><span class="sxs-lookup"><span data-stu-id="19f98-113">A text expression identifying the field that contains the numeric data you want to evaluate or an expression that performs a calculation using the data in that field.</span></span> <span data-ttu-id="19f98-114">Operanden in *NumericExpression* können den Namen eines Tabellenfelds, einer Konstanten oder einer Funktion enthalten (die entweder systeminterne oder benutzerdefinierte, aber keine der anderen Aggregatfunktionen SQL sein kann).</span><span class="sxs-lookup"><span data-stu-id="19f98-114">Operands in  *NumericExpression*  can include the name of a table field, a constant, or a function (which can be either intrinsic or user-defined but not one of the other SQL aggregate functions).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="19f98-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="19f98-115">Remarks</span></span>

 <span data-ttu-id="19f98-116">**Var** kann nur mit numerischen Spalten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="19f98-116">**Var** can be used with numeric columns only.</span></span> <span data-ttu-id="19f98-117">Nullwerte werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="19f98-117">Null values are ignored.</span></span> 
  

