---
title: Sum-Funktion (Access Custom Web App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2345092-ba5f-4030-9070-391233e70f92
description: Gibt die Summe aller Werte im Ausdruck zurück.
ms.openlocfilehash: b0fed86469b32ddcc7f60a388f5d42c7bbd48b6c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304235"
---
# <a name="sum-function-access-custom-web-app"></a><span data-ttu-id="fe10e-103">Sum-Funktion (Access Custom Web App)</span><span class="sxs-lookup"><span data-stu-id="fe10e-103">Sum Function (Access custom web app)</span></span>

<span data-ttu-id="fe10e-104">Gibt die Summe aller Werte im Ausdruck zurück.</span><span class="sxs-lookup"><span data-stu-id="fe10e-104">Returns the sum of all the values in the expression.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="fe10e-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="fe10e-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="fe10e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe10e-107">Syntax</span></span>

 <span data-ttu-id="fe10e-108">**Summe** (*Numerischer Ausdruck*)</span><span class="sxs-lookup"><span data-stu-id="fe10e-108">**Sum** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="fe10e-109">Die **Sum** -Funktion enthält das folgende Argument.</span><span class="sxs-lookup"><span data-stu-id="fe10e-109">The **Sum** function contains the following argument.</span></span> 
  
|<span data-ttu-id="fe10e-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="fe10e-110">**Argument name**</span></span>|<span data-ttu-id="fe10e-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fe10e-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="fe10e-112">*Numerischer Ausdruck*</span><span class="sxs-lookup"><span data-stu-id="fe10e-112">*NumericExpression*</span></span>  <br/> |<span data-ttu-id="fe10e-113">Ein Ausdruck, der das Feld mit den numerischen Daten enthält, die Sie hinzufügen möchten, oder ein Ausdruck, der eine Berechnung mithilfe der Daten in diesem Feld ausführt.</span><span class="sxs-lookup"><span data-stu-id="fe10e-113">An expression identifying the field that contains the numeric data you want to add or an expression that performs a calculation using the data in that field.</span></span> <span data-ttu-id="fe10e-114">Operanden in *numericive* können den Namen eines Tabellenfelds, eine Konstante oder eine Funktion enthalten (Dies kann entweder systeminterne oder benutzerdefinierte, aber nicht eine der anderen SQL-Aggregatfunktionen sein).</span><span class="sxs-lookup"><span data-stu-id="fe10e-114">Operands in  *NumericExpression*  can include the name of a table field, a constant, or a function (which can be either intrinsic or user-defined but not one of the other SQL aggregate functions).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fe10e-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fe10e-115">Remarks</span></span>

<span data-ttu-id="fe10e-116">Die **Sum** -Funktion ignoriert Datensätze, die Nullwerte enthalten.</span><span class="sxs-lookup"><span data-stu-id="fe10e-116">The **Sum** function ignores records that contain Null values.</span></span> 
  
<span data-ttu-id="fe10e-117">Die **Sum** -Funktion kann nur mit numerischen Spalten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fe10e-117">The **Sum** function can only be used with numeric columns.</span></span> 
  

