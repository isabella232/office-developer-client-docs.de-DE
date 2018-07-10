---
title: Var-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cb2aace1-fa2d-480e-bfc7-44ae399943f5
description: Gibt die statistische Varianz für eine Populationsstichprobe als Menge von Werten zurück, die in einem angegebenen Feld einer Abfrage enthalten sind.
ms.openlocfilehash: 9937f1985c0a7df5eb06977333ab889947891380
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790385"
---
# <a name="var-function-access-custom-web-app"></a><span data-ttu-id="c8fe2-103">Var-Funktion (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="c8fe2-103">Var Function (Access custom web app)</span></span>

<span data-ttu-id="c8fe2-104">Gibt die statistische Varianz für eine Populationsstichprobe als Menge von Werten zurück, die in einem angegebenen Feld einer Abfrage enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c8fe2-104">Returns the statistical variance for a population sample represented as a set of values contained in a specified field in a query.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="c8fe2-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/de-de/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="c8fe2-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/de-de/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c8fe2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8fe2-107">Syntax</span></span>

 <span data-ttu-id="c8fe2-108">**Var** (*NumericExpression*)</span><span class="sxs-lookup"><span data-stu-id="c8fe2-108">**Var** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="c8fe2-109">Die **Var** -Funktion enthält das folgende Argument.</span><span class="sxs-lookup"><span data-stu-id="c8fe2-109">The **Var** function contains the following argument.</span></span> 
  
|<span data-ttu-id="c8fe2-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="c8fe2-110">**Argument name**</span></span>|<span data-ttu-id="c8fe2-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="c8fe2-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="c8fe2-112">*NumericExpression*</span><span class="sxs-lookup"><span data-stu-id="c8fe2-112">*NumericExpression*</span></span>  <br/> |<span data-ttu-id="c8fe2-113">Ein Ausdruck, identifiziert das Feld mit den numerischen Daten, die ausgewertet werden soll, oder ein Ausdruck, der mithilfe der Daten in diesem Feld eine Berechnung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c8fe2-113">A text expression identifying the field that contains the numeric data you want to evaluate or an expression that performs a calculation using the data in that field.</span></span> <span data-ttu-id="c8fe2-114">Zu den Operanden von *NumericExpression* zählen der Name des Tabellenfelds, eine Konstante oder eine Funktion (die integrierte oder benutzerdefinierte sein kann jedoch keine der anderen SQL-Aggregatfunktionen).</span><span class="sxs-lookup"><span data-stu-id="c8fe2-114">Operands in  *NumericExpression*  can include the name of a table field, a constant, or a function (which can be either intrinsic or user-defined but not one of the other SQL aggregate functions).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c8fe2-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c8fe2-115">Remarks</span></span>

 <span data-ttu-id="c8fe2-116">**Var** kann nur bei numerischen Spalten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c8fe2-116">**Var** can be used with numeric columns only.</span></span> <span data-ttu-id="c8fe2-117">NULL-Werte werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="c8fe2-117">Null values are ignored.</span></span> 
  

