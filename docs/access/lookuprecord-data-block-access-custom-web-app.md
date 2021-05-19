---
title: LookupRecord Data Block (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 001899f7-5b1a-4c0b-a0e4-e01985eea818
description: Mit einem NachschlagenDatensatz -Datenblock wird eine Reihe von Aktionen für einen bestimmten Datensatz ausgeführt.
ms.openlocfilehash: a6d89b1700a47f88086fd8c4e7b594b90425912c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434361"
---
# <a name="lookuprecord-data-block-access-custom-web-app"></a><span data-ttu-id="499de-103">LookupRecord Data Block (benutzerdefinierte Access-Web-App)</span><span class="sxs-lookup"><span data-stu-id="499de-103">LookupRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="499de-104">Mit einem **NachschlagenDatensatz** -Datenblock wird eine Reihe von Aktionen für einen bestimmten Datensatz ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="499de-104">A **LookupRecord** data block performs a set of actions on a specific record.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="499de-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="499de-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="499de-107">Der **NachschlagenDatensatz**-Datenblock ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="499de-107">The **LookupRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="499de-108">Setting</span><span class="sxs-lookup"><span data-stu-id="499de-108">Setting</span></span>

<span data-ttu-id="499de-109">Die **NachschlagenDatensatz**-Aktion kann mit den folgenden Argumenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="499de-109">The **SetField** action has the following arguments.</span></span> 
  
|<span data-ttu-id="499de-110">**Argument**</span><span class="sxs-lookup"><span data-stu-id="499de-110">**Argument**</span></span>|<span data-ttu-id="499de-111">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="499de-111">**Required**</span></span>|<span data-ttu-id="499de-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="499de-112">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="499de-113">_In_</span><span class="sxs-lookup"><span data-stu-id="499de-113">_In_</span></span> <br/> |<span data-ttu-id="499de-114">Ja</span><span class="sxs-lookup"><span data-stu-id="499de-114">Yes</span></span>  <br/> |<span data-ttu-id="499de-115">Eine Zeichenfolge, die den Datensatz bezeichnet, für den eine Aktion ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="499de-115">A string that identifies the record to operate on.</span></span> <span data-ttu-id="499de-116">Das *Argument In* kann den Namen der Tabelle, eine Auswahlabfrage oder eine SQL enthalten.</span><span class="sxs-lookup"><span data-stu-id="499de-116">The  *In*  argument can contain the name of the table, a select query, or a SQL statement.</span></span>  <br/> |
| <span data-ttu-id="499de-117">_Bedingung_</span><span class="sxs-lookup"><span data-stu-id="499de-117">_Where Condition_</span></span> <br/> |<span data-ttu-id="499de-118">Nein</span><span class="sxs-lookup"><span data-stu-id="499de-118">No</span></span>  <br/> |<span data-ttu-id="499de-119">Ein Zeichenfolgenausdruck, der verwendet wird, um den Datenbereich einzuschränken, für den der **Datenblock LookupRecord** ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="499de-119">A string expression used to restrict the range of data on which the **LookupRecord** data block is performed.</span></span> <span data-ttu-id="499de-120">Beispielsweise ist criteria oft äquivalent mit der WHERE-Klausel in einem SQL-Ausdruck, ohne das Wort WHERE.</span><span class="sxs-lookup"><span data-stu-id="499de-120">For example, criteria is often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="499de-121">Wenn Kriterien nicht angegeben werden, wird der **Datenblock LookupRecord** für die gesamte Domäne ausgeführt, die durch das  *Argument In angegeben*  wird.</span><span class="sxs-lookup"><span data-stu-id="499de-121">If criteria is omitted, the **LookupRecord** data block operates on the entire domain specified by the  *In*  argument.</span></span> <span data-ttu-id="499de-122">Jedes Feld, das in Kriterien enthalten ist, muss auch ein Feld in *sein.*</span><span class="sxs-lookup"><span data-stu-id="499de-122">Any field that is included in criteria must also be a field in  *In*  .</span></span>  <br/> |
| <span data-ttu-id="499de-123">_Alias_</span><span class="sxs-lookup"><span data-stu-id="499de-123">_Alias_</span></span> <br/> |<span data-ttu-id="499de-124">Nein</span><span class="sxs-lookup"><span data-stu-id="499de-124">No</span></span>  <br/> |<span data-ttu-id="499de-125">Eine Zeichenfolge, die einen alternativen Namen für den durch das Argument In angegebenen  *Datensatz*  enthält.</span><span class="sxs-lookup"><span data-stu-id="499de-125">A string that provides an alternative name for the record specified by the  *In*  argument.</span></span> <span data-ttu-id="499de-126">Wird häufig als Abkürzung des Tabellennamens in späteren Verweisen verwendet, um mögliche Mehrdeutigkeiten zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="499de-126">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.</span></span> <span data-ttu-id="499de-127">Wenn  *Alias*  nicht angegeben ist, wird der Tabellen- oder Abfragename als Alias verwendet.</span><span class="sxs-lookup"><span data-stu-id="499de-127">If  *Alias*  is not specified, the table or query name will be used as the alias.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="499de-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="499de-128">Remarks</span></span>

<span data-ttu-id="499de-129">Wenn von den im  *In*  -Argument und im  *Bedingung*  -Argument angegebenen Kriterien mehrere Datensätze angegeben werden, wird der **NachschlagenDatensatz** -Datenblock nur für den ersten Datensatz ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="499de-129">If the criteria specified by the  *In*  and  *Where Condition*  arguments specifies more than one record, then the **LookupRecord** data block will only operate on the first record.</span></span> 
  
<span data-ttu-id="499de-130">Wenn kein Datensatz  *Where Condition*  erfüllt oder  *Wenn In*  keine Datensätze enthält, erstellt **LookupRecord** einen leeren Datensatz, in dem alle Felder einen **Null-Wert** enthalten.</span><span class="sxs-lookup"><span data-stu-id="499de-130">If no record satisfies  *Where Condition*  or if  *In*  contains no records, then **LookupRecord** creates a blank record in which all of the fields contain a **Null** value.</span></span> 
  

