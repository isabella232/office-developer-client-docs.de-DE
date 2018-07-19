---
title: Count-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d931535b-428f-4300-93bf-cfe0ebcc2ac9
description: Gibt die Anzahl von Datensätzen in einer Abfrage oder Tabelle zurück.
ms.openlocfilehash: 300fcbfd2aa927dd19516355ae28eec2adadf521
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790212"
---
# <a name="count-function-access-custom-web-app"></a><span data-ttu-id="66bb7-103">Count-Funktion (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="66bb7-103">Count function (Access custom web app)</span></span>

<span data-ttu-id="66bb7-104">Gibt die Anzahl von Datensätzen in einer Abfrage oder Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="66bb7-104">Returns the number of records in a query or table.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="66bb7-p101"> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/de-de/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="66bb7-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/de-de/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="66bb7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="66bb7-107">Syntax</span></span>

<span data-ttu-id="66bb7-108">**Count** (*Ausdruck*)</span><span class="sxs-lookup"><span data-stu-id="66bb7-108">**Count** (*Expression*)</span></span> 
  
<span data-ttu-id="66bb7-109">Die **Count** -Funktion enthält das folgende Argument.</span><span class="sxs-lookup"><span data-stu-id="66bb7-109">The **Count** function contains the following argument.</span></span> 
  
|<span data-ttu-id="66bb7-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="66bb7-110">**Argument name**</span></span>|<span data-ttu-id="66bb7-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="66bb7-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="66bb7-112">*Expression*</span><span class="sxs-lookup"><span data-stu-id="66bb7-112">*Expression*</span></span>  <br/> |<span data-ttu-id="66bb7-113">Ein Zeichenfolgenausdruck, der das Feld, das Daten enthält, die Sie Count oder ein Ausdruck, der eine Berechnung mit den Daten in das Feld durchführt möchten.</span><span class="sxs-lookup"><span data-stu-id="66bb7-113">A string expression identifying the field that contains the data you want to count or an expression that performs a calculation using the data in the field.</span></span> <span data-ttu-id="66bb7-114">Zu den Operanden von *Ausdruck* zählen der Name des Felds oder Funktion (die integrierte oder benutzerdefinierte werden können, jedoch keine anderen SQL-Aggregatfunktionen).</span><span class="sxs-lookup"><span data-stu-id="66bb7-114">Operands in  *Expression*  can include the name of a table field or function (which can be either intrinsic or user-defined but not other SQL aggregate functions).</span></span> <span data-ttu-id="66bb7-115">Sie können jede Art von Daten, einschließlich Text zählen.</span><span class="sxs-lookup"><span data-stu-id="66bb7-115">You can count any kind of data, including text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="66bb7-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="66bb7-116">Remarks</span></span>

<span data-ttu-id="66bb7-117">Count können Sie die Anzahl der Datensätze in einer zugrunde liegenden Abfrage zählen.</span><span class="sxs-lookup"><span data-stu-id="66bb7-117">You can use Count to count the number of records in an underlying query.</span></span> <span data-ttu-id="66bb7-118">Count können Sie beispielsweise die Anzahl von Bestellungen, die einem bestimmten Land oder einer Region zählen.</span><span class="sxs-lookup"><span data-stu-id="66bb7-118">For example, you could use Count to count the number of orders shipped to a particular country or region.</span></span>
  
<span data-ttu-id="66bb7-119">**Count** (\*) die Anzahl der Elemente in einer Gruppe zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="66bb7-119">**Count** (\*) returns the number of items in a group.</span></span> <span data-ttu-id="66bb7-120">Dazu gehören NULL-Werte und Duplikate.</span><span class="sxs-lookup"><span data-stu-id="66bb7-120">This includes NULL values and duplicates.</span></span> 
  

