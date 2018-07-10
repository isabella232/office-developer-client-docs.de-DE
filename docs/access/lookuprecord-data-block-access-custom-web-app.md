---
title: NachschlagenDatensatz-Datenblock (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 001899f7-5b1a-4c0b-a0e4-e01985eea818
description: Mit einem NachschlagenDatensatz-Datenblock führt eine Reihe von Aktionen für einen bestimmten Datensatz.
ms.openlocfilehash: 7012fecdf0e73647b2b8177473dd8b5540b5fcca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790237"
---
# <a name="lookuprecord-data-block-access-custom-web-app"></a><span data-ttu-id="d6db4-103">NachschlagenDatensatz-Datenblock (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="d6db4-103">LookupRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="d6db4-104">Mit einem **NachschlagenDatensatz** -Datenblock wird eine Reihe von Aktionen für einen bestimmten Datensatz ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d6db4-104">A **LookupRecord** data block performs a set of actions on a specific record.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="d6db4-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/de-de/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="d6db4-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/de-de/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d6db4-107">Der **NachschlagenDatensatz** -Datenblock ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d6db4-107">The **LookupRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="d6db4-108">Einstellung</span><span class="sxs-lookup"><span data-stu-id="d6db4-108">Setting</span></span>

<span data-ttu-id="d6db4-109">Die **NachschlagenDatensatz** -Aktion kann mit den folgenden Argumenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d6db4-109">The **SetField** action has the following arguments.</span></span> 
  
|<span data-ttu-id="d6db4-110">**Argument**</span><span class="sxs-lookup"><span data-stu-id="d6db4-110">**Argument**</span></span>|<span data-ttu-id="d6db4-111">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="d6db4-111">**Required**</span></span>|<span data-ttu-id="d6db4-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d6db4-112">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="d6db4-113">_In_</span><span class="sxs-lookup"><span data-stu-id="d6db4-113">_In_</span></span> <br/> |<span data-ttu-id="d6db4-114">Ja</span><span class="sxs-lookup"><span data-stu-id="d6db4-114">Yes</span></span>  <br/> |<span data-ttu-id="d6db4-115">Eine Zeichenfolge, die den Datensatz für den Betrieb identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d6db4-115">A string that identifies the record to operate on.</span></span> <span data-ttu-id="d6db4-116">Das *im* Argument kann der Name der Tabelle, einer select-Abfrage oder eine SQL-Anweisung enthalten.</span><span class="sxs-lookup"><span data-stu-id="d6db4-116">The  *In*  argument can contain the name of the table, a select query, or a SQL statement.</span></span>  <br/> |
| <span data-ttu-id="d6db4-117">_Where Condition_</span><span class="sxs-lookup"><span data-stu-id="d6db4-117">_Where Condition_</span></span> <br/> |<span data-ttu-id="d6db4-118">Nein</span><span class="sxs-lookup"><span data-stu-id="d6db4-118">No</span></span>  <br/> |<span data-ttu-id="d6db4-119">Ein Zeichenfolgenausdruck, der zum Einschränken des Bereichs der Daten auf dem des **NachschlagenDatensatz** -Datenblocks wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d6db4-119">A string expression used to restrict the range of data on which the **LookupRecord** data block is performed.</span></span> <span data-ttu-id="d6db4-120">Häufig wird beispielsweise Kriterien entspricht der WHERE-Klausel in einem SQL-Ausdruck ohne das Wort, in dem.</span><span class="sxs-lookup"><span data-stu-id="d6db4-120">For example, criteria is often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="d6db4-121">Kriterien nicht angegeben, wirkt sich auf die gesamte Domäne angegeben, die durch das Argument *In* das **NachschlagenDatensatz** -Datenblock.</span><span class="sxs-lookup"><span data-stu-id="d6db4-121">If criteria is omitted, the **LookupRecord** data block operates on the entire domain specified by the  *In*  argument.</span></span> <span data-ttu-id="d6db4-122">Jedes Feld, das im Argument Kriterien enthalten ist, muss auch ein Feld in *In* sein.</span><span class="sxs-lookup"><span data-stu-id="d6db4-122">Any field that is included in criteria must also be a field in  *In*  .</span></span>  <br/> |
| <span data-ttu-id="d6db4-123">_Alias_</span><span class="sxs-lookup"><span data-stu-id="d6db4-123">_Alias_</span></span> <br/> |<span data-ttu-id="d6db4-124">Nein</span><span class="sxs-lookup"><span data-stu-id="d6db4-124">No</span></span>  <br/> |<span data-ttu-id="d6db4-125">Eine Zeichenfolge, die einen alternativen Namen für den durch das Argument *im* angegebenen Datensatz enthält.</span><span class="sxs-lookup"><span data-stu-id="d6db4-125">A string that provides an alternative name for the record specified by the  *In*  argument.</span></span> <span data-ttu-id="d6db4-126">Häufig verwendet, um den Tabellennamen für nachfolgende Verweise zu verhindern, dass mögliche mehrdeutige Verweise zu verkürzen.</span><span class="sxs-lookup"><span data-stu-id="d6db4-126">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.</span></span> <span data-ttu-id="d6db4-127">Wenn *Alias* nicht angegeben ist, wird den Namen der Tabelle oder Abfrage als Alias verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d6db4-127">If  *Alias*  is not specified, the table or query name will be used as the alias.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d6db4-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d6db4-128">Remarks</span></span>

<span data-ttu-id="d6db4-129">Wenn von den im  *In*  -Argument und im  *Bedingung*  -Argument angegebenen Kriterien mehrere Datensätze angegeben werden, wird der **NachschlagenDatensatz** -Datenblock nur für den ersten Datensatz ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d6db4-129">If the criteria specified by the  *In*  and  *Where Condition*  arguments specifies more than one record, then the **LookupRecord** data block will only operate on the first record.</span></span> 
  
<span data-ttu-id="d6db4-130">Wenn kein Datensatz erfüllt die *Bedingung* oder *In* keine Datensätze enthält, erstellt **NachschlagenDatensatz** einen leeren Datensatz in dem alle Felder einen **Null** -Wert enthalten.</span><span class="sxs-lookup"><span data-stu-id="d6db4-130">If no record satisfies  *Where Condition*  or if  *In*  contains no records, then **LookupRecord** creates a blank record in which all of the fields contain a **Null** value.</span></span> 
  

