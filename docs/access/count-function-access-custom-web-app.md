---
title: Count-Funktion (Access Custom Web App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d931535b-428f-4300-93bf-cfe0ebcc2ac9
description: Gibt die Anzahl von Datensätzen in einer Abfrage oder Tabelle zurück.
ms.openlocfilehash: 98dbed393bf2f6dc401119f6c5dc7ab6b5ff7864
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282236"
---
# <a name="count-function-access-custom-web-app"></a><span data-ttu-id="f127c-103">Count-Funktion (Access Custom Web App)</span><span class="sxs-lookup"><span data-stu-id="f127c-103">Count function (Access custom web app)</span></span>

<span data-ttu-id="f127c-104">Gibt die Anzahl von Datensätzen in einer Abfrage oder Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="f127c-104">Returns the number of records in a query or table.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="f127c-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="f127c-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f127c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f127c-107">Syntax</span></span>

<span data-ttu-id="f127c-108">**Anzahl** (*Ausdruck*)</span><span class="sxs-lookup"><span data-stu-id="f127c-108">**Count** (*Expression*)</span></span> 
  
<span data-ttu-id="f127c-109">Die **count** -Funktion enthält das folgende Argument.</span><span class="sxs-lookup"><span data-stu-id="f127c-109">The **Count** function contains the following argument.</span></span> 
  
|<span data-ttu-id="f127c-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="f127c-110">**Argument name**</span></span>|<span data-ttu-id="f127c-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f127c-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="f127c-112">*Ausdruck*</span><span class="sxs-lookup"><span data-stu-id="f127c-112">*Expression*</span></span>  <br/> |<span data-ttu-id="f127c-113">Ein Zeichenfolgenausdruck, der das Feld identifiziert, das die zu zählenden Daten enthält, oder ein Ausdruck, der eine Berechnung mithilfe der Daten im Feld ausführt.</span><span class="sxs-lookup"><span data-stu-id="f127c-113">A string expression identifying the field that contains the data you want to count or an expression that performs a calculation using the data in the field.</span></span> <span data-ttu-id="f127c-114">Operanden in *Expression* können den Namen eines Tabellenfelds oder einer Funktion enthalten (Dies kann sowohl systeminterne als auch benutzerdefinierte, aber nicht andere SQL-Aggregatfunktionen sein).</span><span class="sxs-lookup"><span data-stu-id="f127c-114">Operands in  *Expression*  can include the name of a table field or function (which can be either intrinsic or user-defined but not other SQL aggregate functions).</span></span> <span data-ttu-id="f127c-115">Sie können beliebige Daten, einschließlich Text, zählen.</span><span class="sxs-lookup"><span data-stu-id="f127c-115">You can count any kind of data, including text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f127c-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f127c-116">Remarks</span></span>

<span data-ttu-id="f127c-117">Mithilfe der Count-Funktion kann die Anzahl von Datensätzen in einer zugrunde liegenden Abfrage gezählt werden.</span><span class="sxs-lookup"><span data-stu-id="f127c-117">You can use Count to count the number of records in an underlying query.</span></span> <span data-ttu-id="f127c-118">Sie können beispielsweise count verwenden, um die Anzahl der Bestellungen zu ermitteln, die an ein bestimmtes Land oder eine bestimmte Region geliefert wurden.</span><span class="sxs-lookup"><span data-stu-id="f127c-118">For example, you could use Count to count the number of orders shipped to a particular country or region.</span></span>
  
<span data-ttu-id="f127c-119">**Anzahl** (\*) gibt die Anzahl der Elemente in einer Gruppe zurück.</span><span class="sxs-lookup"><span data-stu-id="f127c-119">**Count** (\*) returns the number of items in a group.</span></span> <span data-ttu-id="f127c-120">Dazu gehören NULL-Werte und Duplikate.</span><span class="sxs-lookup"><span data-stu-id="f127c-120">This includes NULL values and duplicates.</span></span> 
  

