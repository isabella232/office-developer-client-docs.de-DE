---
title: ForEachRecord Data Block (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8ffa0de2-5abb-4375-9fb5-042ce3c21506
description: Ein ForEachRecord-Datenblock wiederholt einen Satz von Anweisungen für jeden Datensatz in einer Domäne.
ms.openlocfilehash: 9715824bff7d478fa2880ada5e8770f7a0c88883
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428235"
---
# <a name="foreachrecord-data-block-access-custom-web-app"></a><span data-ttu-id="7f393-103">ForEachRecord Data Block (benutzerdefinierte Access-Web-App)</span><span class="sxs-lookup"><span data-stu-id="7f393-103">ForEachRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="7f393-104">Ein **ForEachRecord-Datenblock** wiederholt einen Satz von Anweisungen für jeden Datensatz in einer Domäne.</span><span class="sxs-lookup"><span data-stu-id="7f393-104">A **ForEachRecord** data block repeats a set of statements for each record in a domain.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="7f393-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="7f393-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7f393-107">Der **FürJedenDatensatz**-Datenblock ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7f393-107">The **ForEachRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="7f393-108">Setting</span><span class="sxs-lookup"><span data-stu-id="7f393-108">Setting</span></span>

<span data-ttu-id="7f393-109">Die **FürJedenDatensatz**-Aktion kann mit den folgenden Argumenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7f393-109">The **ForEachRecord** action has the following arguments.</span></span> 
  
|<span data-ttu-id="7f393-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="7f393-110">**Argument name**</span></span>|<span data-ttu-id="7f393-111">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="7f393-111">**Required**</span></span>|<span data-ttu-id="7f393-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7f393-112">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7f393-113">**In**</span><span class="sxs-lookup"><span data-stu-id="7f393-113">**In**</span></span> <br/> |<span data-ttu-id="7f393-114">Ja</span><span class="sxs-lookup"><span data-stu-id="7f393-114">Yes</span></span>  <br/> |<span data-ttu-id="7f393-115">Eine Zeichenfolge, die die Domäne von Datensätzen bezeichnet, für die eine Aktion ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7f393-115">A string that identifies the domain of records to operate on.</span></span> <span data-ttu-id="7f393-116">Das *Argument In* kann den Namen der Tabelle, eine Auswahlabfrage oder eine SQL enthalten.</span><span class="sxs-lookup"><span data-stu-id="7f393-116">The  *In*  argument can contain the name of the table, a select query, or a SQL statement.</span></span>  <br/> <span data-ttu-id="7f393-117">**HINWEIS**: Die angegebene Domäne darf keine Daten enthalten, die in einer verknüpften Tabelle oder ODBC-Datenquelle gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="7f393-117">**NOTE**: The specified domain cannot include data stored in a linked table or ODBC data source.</span></span>           |
|<span data-ttu-id="7f393-118">**Bedingung**</span><span class="sxs-lookup"><span data-stu-id="7f393-118">**Where Condition**</span></span> <br/> |<span data-ttu-id="7f393-119">Nein</span><span class="sxs-lookup"><span data-stu-id="7f393-119">No</span></span>  <br/> |<span data-ttu-id="7f393-120">Ein Zeichenfolgenausdruck, der verwendet wird, um den Datenbereich einzuschränken, für den der **ForEachRecord-Datenblock** ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7f393-120">A string expression used to restrict the range of data on which the **ForEachRecord** data block is performed.</span></span> <span data-ttu-id="7f393-121">Beispielsweise ist criteria oft äquivalent mit der WHERE-Klausel in einem SQL-Ausdruck, ohne das Wort WHERE.</span><span class="sxs-lookup"><span data-stu-id="7f393-121">For example, criteria is often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="7f393-122">Wenn Kriterien nicht angegeben werden, wird der **ForEachRecord-Datenblock** für die gesamte Domäne ausgeführt, die durch das  *Argument In angegeben*  wird.</span><span class="sxs-lookup"><span data-stu-id="7f393-122">If criteria are omitted, the **ForEachRecord** data block operates on the entire domain specified by the  *In*  argument.</span></span> <span data-ttu-id="7f393-123">Jedes Feld, das in Kriterien enthalten ist, muss auch ein Feld in *sein.*</span><span class="sxs-lookup"><span data-stu-id="7f393-123">Any field that is included in criteria must also be a field in  *In*  .</span></span>  <br/> |
|<span data-ttu-id="7f393-124">**Alias**</span><span class="sxs-lookup"><span data-stu-id="7f393-124">**Alias**</span></span> <br/> |<span data-ttu-id="7f393-125">Nein</span><span class="sxs-lookup"><span data-stu-id="7f393-125">No</span></span>  <br/> |<span data-ttu-id="7f393-126">Eine Zeichenfolge, die einen alternativen Namen für die durch das  *Argument In*  angegebene Domäne enthält.</span><span class="sxs-lookup"><span data-stu-id="7f393-126">A string that provides an alternative name for the domain specified by the  *In*  argument.</span></span> <span data-ttu-id="7f393-127">Wird häufig als Abkürzung des Tabellennamens in späteren Verweisen verwendet, um mögliche Mehrdeutigkeiten zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="7f393-127">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.</span></span> <span data-ttu-id="7f393-128">Wenn  *Alias*  nicht angegeben ist, wird der Tabellen- oder Abfragename als Alias verwendet.</span><span class="sxs-lookup"><span data-stu-id="7f393-128">If  *Alias*  is not specified, the table or query name will be used as the alias.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7f393-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7f393-129">Remarks</span></span>

<span data-ttu-id="7f393-130">Mit der **[BeendenFürJedenDatensatz](exitforeachrecord-macro-action-access-custom-web-app.md)** -Aktion beenden Sie einen **FürJedenDatensatz** -Datenblock sofort.</span><span class="sxs-lookup"><span data-stu-id="7f393-130">Use the **[ExitForEachRecord](exitforeachrecord-macro-action-access-custom-web-app.md)** action to exit a **ForEachRecord** data block immediately.</span></span> 
  

