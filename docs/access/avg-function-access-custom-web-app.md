---
title: AVG-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d432e823-a255-4860-9c8b-201b2e0476fd
description: Berechnet das arithmetische Mittel einer Gruppe von Werten zurück, die in einem angegebenen Feld enthalten sind.
ms.openlocfilehash: afe832a51fc9cd3b224087a0b06fe539f6a7004b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790192"
---
# <a name="avg-function-access-custom-web-app"></a><span data-ttu-id="a8039-103">AVG-Funktion (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="a8039-103">Avg Function (Access custom web app)</span></span>

<span data-ttu-id="a8039-104">Berechnet das arithmetische Mittel einer Gruppe von Werten zurück, die in einem angegebenen Feld enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="a8039-104">Calculates the arithmetic mean of a set of values contained in a specified field.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="a8039-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="a8039-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a8039-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8039-107">Syntax</span></span>

 <span data-ttu-id="a8039-108">**AVG** (*NumericExpression*)</span><span class="sxs-lookup"><span data-stu-id="a8039-108">**Avg** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="a8039-109">Die **Avg** -Funktion enthält das folgende Argument.</span><span class="sxs-lookup"><span data-stu-id="a8039-109">The **Avg** function contains the following argument.</span></span> 
  
|<span data-ttu-id="a8039-110">**Argument**</span><span class="sxs-lookup"><span data-stu-id="a8039-110">**Argument**</span></span>|<span data-ttu-id="a8039-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a8039-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a8039-112">NumericExpression</span><span class="sxs-lookup"><span data-stu-id="a8039-112">NumericExpression</span></span>  <br/> |<span data-ttu-id="a8039-113">Ein Zeichenfolgenausdruck, der das Feld mit den numerischen Daten möchten Sie Mittelwert oder ein Ausdruck, der mithilfe der Daten in diesem Feld eine Berechnung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a8039-113">A string expression identifying the field that contains the numeric data you want to average or an expression that performs a calculation using the data in that field.</span></span> <span data-ttu-id="a8039-114">Zu den Operanden von *NumericExpression* zählen der Name des Tabellenfelds, eine Variable oder eine Funktion (die integrierte oder benutzerdefinierte sein kann jedoch keine der anderen SQL-Aggregatfunktionen).</span><span class="sxs-lookup"><span data-stu-id="a8039-114">Operands in  *NumericExpression*  can include the name of a table field, a variable, or a function (which can be either intrinsic or user-defined but not one of the other SQL aggregate functions).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a8039-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a8039-115">Remarks</span></span>

<span data-ttu-id="a8039-116">Durch **Avg** berechnete Mittelwert ist das arithmetische Mittel (die Summe der Werte dividiert durch die Anzahl der Werte).</span><span class="sxs-lookup"><span data-stu-id="a8039-116">The average calculated by **Avg** is the arithmetic mean (the sum of the values divided by the number of values).</span></span> <span data-ttu-id="a8039-117">**Avg**, beispielsweise können Sie die durchschnittlichen Frachtkosten berechnen.</span><span class="sxs-lookup"><span data-stu-id="a8039-117">You could use **Avg**, for example, to calculate average freight cost.</span></span> 
  
<span data-ttu-id="a8039-118">Die **Avg** -Funktion umfasst keine **Null** -Werte in der Berechnung.</span><span class="sxs-lookup"><span data-stu-id="a8039-118">The **Avg** function does not include any **Null** values in the calculation.</span></span> 
  

