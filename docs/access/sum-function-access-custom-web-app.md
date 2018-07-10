---
title: SUM-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2345092-ba5f-4030-9070-391233e70f92
description: Gibt die Summe aller Werte im Ausdruck zurück.
ms.openlocfilehash: 98531a0487505c24ed62034b7c283b9765a3e7a7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790373"
---
# <a name="sum-function-access-custom-web-app"></a><span data-ttu-id="307d7-103">SUM-Funktion (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="307d7-103">Sum Function (Access custom web app)</span></span>

<span data-ttu-id="307d7-104">Gibt die Summe aller Werte im Ausdruck zurück.</span><span class="sxs-lookup"><span data-stu-id="307d7-104">Returns the sum of all the values in the expression.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="307d7-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/de-de/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="307d7-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/de-de/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="307d7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="307d7-107">Syntax</span></span>

 <span data-ttu-id="307d7-108">**Summe** (*NumericExpression*)</span><span class="sxs-lookup"><span data-stu-id="307d7-108">**Sum** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="307d7-109">Die **Sum** -Funktion enthält das folgende Argument.</span><span class="sxs-lookup"><span data-stu-id="307d7-109">The **Sum** function contains the following argument.</span></span> 
  
|<span data-ttu-id="307d7-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="307d7-110">**Argument name**</span></span>|<span data-ttu-id="307d7-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="307d7-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="307d7-112">*NumericExpression*</span><span class="sxs-lookup"><span data-stu-id="307d7-112">*NumericExpression*</span></span>  <br/> |<span data-ttu-id="307d7-113">Ein Ausdruck, identifiziert das Feld mit den numerischen Daten, den, die Sie hinzufügen möchten, oder ein Ausdruck, der mithilfe der Daten in diesem Feld eine Berechnung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="307d7-113">An expression identifying the field that contains the numeric data you want to add or an expression that performs a calculation using the data in that field.</span></span> <span data-ttu-id="307d7-114">Zu den Operanden von *NumericExpression* zählen der Name des Tabellenfelds, eine Konstante oder eine Funktion (die integrierte oder benutzerdefinierte sein kann jedoch keine der anderen SQL-Aggregatfunktionen).</span><span class="sxs-lookup"><span data-stu-id="307d7-114">Operands in  *NumericExpression*  can include the name of a table field, a constant, or a function (which can be either intrinsic or user-defined but not one of the other SQL aggregate functions).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="307d7-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="307d7-115">Remarks</span></span>

<span data-ttu-id="307d7-116">Die **Sum** -Funktion ignoriert Datensätze, die Null-Werte enthalten.</span><span class="sxs-lookup"><span data-stu-id="307d7-116">The **Sum** function ignores records that contain Null values.</span></span> 
  
<span data-ttu-id="307d7-117">Die **Sum** -Funktion kann nur bei numerischen Spalten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="307d7-117">The **Sum** function can only be used with numeric columns.</span></span> 
  

