---
title: LookupRecord-Daten Block (Access Custom Web App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 001899f7-5b1a-4c0b-a0e4-e01985eea818
description: Mit einem NachschlagenDatensatz -Datenblock wird eine Reihe von Aktionen für einen bestimmten Datensatz ausgeführt.
ms.openlocfilehash: a6d89b1700a47f88086fd8c4e7b594b90425912c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304270"
---
# <a name="lookuprecord-data-block-access-custom-web-app"></a><span data-ttu-id="3a4a9-103">LookupRecord-Daten Block (Access Custom Web App)</span><span class="sxs-lookup"><span data-stu-id="3a4a9-103">LookupRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="3a4a9-104">Mit einem **NachschlagenDatensatz** -Datenblock wird eine Reihe von Aktionen für einen bestimmten Datensatz ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3a4a9-104">A **LookupRecord** data block performs a set of actions on a specific record.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="3a4a9-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="3a4a9-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3a4a9-107">Der **NachschlagenDatensatz**-Datenblock ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3a4a9-107">The **LookupRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="3a4a9-108">Einstellung</span><span class="sxs-lookup"><span data-stu-id="3a4a9-108">Setting</span></span>

<span data-ttu-id="3a4a9-109">Die **NachschlagenDatensatz**-Aktion kann mit den folgenden Argumenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3a4a9-109">The **SetField** action has the following arguments.</span></span> 
  
|<span data-ttu-id="3a4a9-110">**Argument**</span><span class="sxs-lookup"><span data-stu-id="3a4a9-110">**Argument**</span></span>|<span data-ttu-id="3a4a9-111">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="3a4a9-111">**Required**</span></span>|<span data-ttu-id="3a4a9-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3a4a9-112">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="3a4a9-113">_In_</span><span class="sxs-lookup"><span data-stu-id="3a4a9-113">_In_</span></span> <br/> |<span data-ttu-id="3a4a9-114">Ja</span><span class="sxs-lookup"><span data-stu-id="3a4a9-114">Yes</span></span>  <br/> |<span data-ttu-id="3a4a9-115">Eine Zeichenfolge, die den Datensatz bezeichnet, für den eine Aktion ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3a4a9-115">A string that identifies the record to operate on.</span></span> <span data-ttu-id="3a4a9-116">Das Argument *in* kann den Namen der Tabelle, eine Auswahlabfrage oder eine SQL-Anweisung enthalten.</span><span class="sxs-lookup"><span data-stu-id="3a4a9-116">The  *In*  argument can contain the name of the table, a select query, or a SQL statement.</span></span>  <br/> |
| <span data-ttu-id="3a4a9-117">_Bedingung_</span><span class="sxs-lookup"><span data-stu-id="3a4a9-117">_Where Condition_</span></span> <br/> |<span data-ttu-id="3a4a9-118">Nein</span><span class="sxs-lookup"><span data-stu-id="3a4a9-118">No</span></span>  <br/> |<span data-ttu-id="3a4a9-119">Ein Zeichenfolgenausdruck, mit dem der Datenumfang eingeschränkt wird, auf dem der **LookupRecord** -Datenblock ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3a4a9-119">A string expression used to restrict the range of data on which the **LookupRecord** data block is performed.</span></span> <span data-ttu-id="3a4a9-120">Beispielsweise ist criteria oft äquivalent mit der WHERE-Klausel in einem SQL-Ausdruck, ohne das Wort WHERE.</span><span class="sxs-lookup"><span data-stu-id="3a4a9-120">For example, criteria is often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="3a4a9-121">Wenn criteria nicht angegeben wird, wird der **LookupRecord** -Datenblock auf die gesamte Domäne angewendet, die durch das *in* -Argument angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3a4a9-121">If criteria is omitted, the **LookupRecord** data block operates on the entire domain specified by the  *In*  argument.</span></span> <span data-ttu-id="3a4a9-122">Jedes Feld, das in Criteria enthalten ist, muss auch ein Feld in *in* sein.</span><span class="sxs-lookup"><span data-stu-id="3a4a9-122">Any field that is included in criteria must also be a field in  *In*  .</span></span>  <br/> |
| <span data-ttu-id="3a4a9-123">_Alias_</span><span class="sxs-lookup"><span data-stu-id="3a4a9-123">_Alias_</span></span> <br/> |<span data-ttu-id="3a4a9-124">Nein</span><span class="sxs-lookup"><span data-stu-id="3a4a9-124">No</span></span>  <br/> |<span data-ttu-id="3a4a9-125">Eine Zeichenfolge, die einen alternativen Namen für den *im* Argument angegebenen Datensatz bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="3a4a9-125">A string that provides an alternative name for the record specified by the  *In*  argument.</span></span> <span data-ttu-id="3a4a9-126">Wird häufig als Abkürzung des Tabellennamens in späteren Verweisen verwendet, um mögliche Mehrdeutigkeiten zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="3a4a9-126">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.</span></span> <span data-ttu-id="3a4a9-127">Wenn *Alias* nicht angegeben wird, wird der Tabellen-oder Abfragename als Alias verwendet.</span><span class="sxs-lookup"><span data-stu-id="3a4a9-127">If  *Alias*  is not specified, the table or query name will be used as the alias.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3a4a9-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3a4a9-128">Remarks</span></span>

<span data-ttu-id="3a4a9-129">Wenn von den im  *In*  -Argument und im  *Bedingung*  -Argument angegebenen Kriterien mehrere Datensätze angegeben werden, wird der **NachschlagenDatensatz** -Datenblock nur für den ersten Datensatz ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3a4a9-129">If the criteria specified by the  *In*  and  *Where Condition*  arguments specifies more than one record, then the **LookupRecord** data block will only operate on the first record.</span></span> 
  
<span data-ttu-id="3a4a9-130">Wenn kein Datensatz erfüllt ist, wenn *Condition* oder If *in* keine Datensätze enthält, erstellt **LookupRecord** einen leeren Datensatz, in dem alle Felder einen **null** -Wert enthalten.</span><span class="sxs-lookup"><span data-stu-id="3a4a9-130">If no record satisfies  *Where Condition*  or if  *In*  contains no records, then **LookupRecord** creates a blank record in which all of the fields contain a **Null** value.</span></span> 
  

