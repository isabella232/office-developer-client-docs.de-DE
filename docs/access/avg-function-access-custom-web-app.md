---
title: Avg-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d432e823-a255-4860-9c8b-201b2e0476fd
description: Berechnet das arithmetische Mittel eines Wertesatzs, der in einem angegebenen Feld enthalten ist.
ms.openlocfilehash: e67cde12e66f943d3b25fe9cb2fee4fe4aea760f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426723"
---
# <a name="avg-function-access-custom-web-app"></a><span data-ttu-id="65f80-103">Avg-Funktion (benutzerdefinierte Access-Web-App)</span><span class="sxs-lookup"><span data-stu-id="65f80-103">Avg Function (Access custom web app)</span></span>

<span data-ttu-id="65f80-104">Berechnet das arithmetische Mittel eines Wertesatzs, der in einem angegebenen Feld enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="65f80-104">Calculates the arithmetic mean of a set of values contained in a specified field.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="65f80-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="65f80-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="65f80-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="65f80-107">Syntax</span></span>

 <span data-ttu-id="65f80-108">**Avg** (*NumericExpression*)</span><span class="sxs-lookup"><span data-stu-id="65f80-108">**Avg** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="65f80-109">Die **Avg-Funktion** enthält das folgende Argument.</span><span class="sxs-lookup"><span data-stu-id="65f80-109">The **Avg** function contains the following argument.</span></span> 
  
|<span data-ttu-id="65f80-110">**Argument**</span><span class="sxs-lookup"><span data-stu-id="65f80-110">**Argument**</span></span>|<span data-ttu-id="65f80-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="65f80-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="65f80-112">NumericExpression</span><span class="sxs-lookup"><span data-stu-id="65f80-112">NumericExpression</span></span>  <br/> |<span data-ttu-id="65f80-113">Ein Zeichenfolgenausdruck, der das Feld identifiziert, das die numerischen Daten enthält, die Sie durchschnittlich verwenden möchten, oder ein Ausdruck, der eine Berechnung mit den Daten in diesem Feld durchführt.</span><span class="sxs-lookup"><span data-stu-id="65f80-113">A string expression identifying the field that contains the numeric data you want to average or an expression that performs a calculation using the data in that field.</span></span> <span data-ttu-id="65f80-114">Operanden in *NumericExpression* können den Namen eines Tabellenfelds, einer Variablen oder einer Funktion enthalten (die entweder systeminterne oder benutzerdefinierte, aber keine der anderen Aggregatfunktionen SQL kann).</span><span class="sxs-lookup"><span data-stu-id="65f80-114">Operands in  *NumericExpression*  can include the name of a table field, a variable, or a function (which can be either intrinsic or user-defined but not one of the other SQL aggregate functions).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="65f80-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="65f80-115">Remarks</span></span>

<span data-ttu-id="65f80-p103">Bei dem von der **Avg**-Funktion berechneten Durchschnittswert handelt es sich um das arithmetische Mittel (die Summe der Werte dividiert durch die Anzahl von Werten). Mithilfe der **Avg**-Funktion können Sie beispielsweise die durchschnittlichen Frachtkosten berechnen.</span><span class="sxs-lookup"><span data-stu-id="65f80-p103">The average calculated by **Avg** is the arithmetic mean (the sum of the values divided by the number of values). You could use **Avg**, for example, to calculate average freight cost.</span></span> 
  
<span data-ttu-id="65f80-118">Die **Avg-Funktion** enthält keine **Null-Werte** in der Berechnung.</span><span class="sxs-lookup"><span data-stu-id="65f80-118">The **Avg** function does not include any **Null** values in the calculation.</span></span> 
  

