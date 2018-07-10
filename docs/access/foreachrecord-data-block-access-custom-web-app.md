---
title: FürJedenDatensatz-Datenblock (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8ffa0de2-5abb-4375-9fb5-042ce3c21506
description: Mit einem FürJedenDatensatz-Datenblock wird eine Reihe von Anweisungen für jeden Datensatz in einer Domäne wiederholt.
ms.openlocfilehash: 8ad14a01be05de9fb34299e49a9737f2009ef5ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790213"
---
# <a name="foreachrecord-data-block-access-custom-web-app"></a><span data-ttu-id="9648e-103">FürJedenDatensatz-Datenblock (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="9648e-103">ForEachRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="9648e-104">Mit einem **FürJedenDatensatz** -Datenblock wird eine Reihe von Anweisungen für jeden Datensatz in einer Domäne wiederholt.</span><span class="sxs-lookup"><span data-stu-id="9648e-104">A **ForEachRecord** data block repeats a set of statements for each record in a domain.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="9648e-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/de-de/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="9648e-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/de-de/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9648e-107">Der **FürJedenDatensatz** -Datenblock ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9648e-107">The **ForEachRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="9648e-108">Einstellung</span><span class="sxs-lookup"><span data-stu-id="9648e-108">Setting</span></span>

<span data-ttu-id="9648e-109">Die **FürJedenDatensatz** -Aktion kann mit den folgenden Argumenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9648e-109">The **ForEachRecord** action has the following arguments.</span></span> 
  
|<span data-ttu-id="9648e-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="9648e-110">**Argument name**</span></span>|<span data-ttu-id="9648e-111">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="9648e-111">**Required**</span></span>|<span data-ttu-id="9648e-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9648e-112">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9648e-113">**In**</span><span class="sxs-lookup"><span data-stu-id="9648e-113">**In**</span></span> <br/> |<span data-ttu-id="9648e-114">Ja</span><span class="sxs-lookup"><span data-stu-id="9648e-114">Yes</span></span>  <br/> |<span data-ttu-id="9648e-115">Eine Zeichenfolge zur Identifizierung von Datensätzen für den Betrieb die Domäne.</span><span class="sxs-lookup"><span data-stu-id="9648e-115">A string that identifies the domain of records to operate on.</span></span> <span data-ttu-id="9648e-116">Das *im* Argument kann der Name der Tabelle, einer select-Abfrage oder eine SQL-Anweisung enthalten.</span><span class="sxs-lookup"><span data-stu-id="9648e-116">The  *In*  argument can contain the name of the table, a select query, or a SQL statement.</span></span>  <br/> <span data-ttu-id="9648e-117">**Hinweis**: die angegebene Domäne darf keine enthalten Daten in einer verknüpften Tabelle oder ODBC-Datenquelle gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="9648e-117">**NOTE**: The specified domain cannot include data stored in a linked table or ODBC data source.</span></span>           |
|<span data-ttu-id="9648e-118">**Where Condition**</span><span class="sxs-lookup"><span data-stu-id="9648e-118">**Where Condition**</span></span> <br/> |<span data-ttu-id="9648e-119">Nein</span><span class="sxs-lookup"><span data-stu-id="9648e-119">No</span></span>  <br/> |<span data-ttu-id="9648e-120">Ein Zeichenfolgenausdruck, der zum Einschränken des Bereichs der Daten auf dem des **FürJedenDatensatz** -Datenblocks wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9648e-120">A string expression used to restrict the range of data on which the **ForEachRecord** data block is performed.</span></span> <span data-ttu-id="9648e-121">Häufig wird beispielsweise Kriterien entspricht der WHERE-Klausel in einem SQL-Ausdruck ohne das Wort, in dem.</span><span class="sxs-lookup"><span data-stu-id="9648e-121">For example, criteria is often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="9648e-122">Wenn Kriterien Length angegeben werden, wirkt sich auf die gesamte Domäne, die durch das Argument *im* angegebenen **FürJedenDatensatz** -Datenblock.</span><span class="sxs-lookup"><span data-stu-id="9648e-122">If criteria are omitted, the **ForEachRecord** data block operates on the entire domain specified by the  *In*  argument.</span></span> <span data-ttu-id="9648e-123">Jedes Feld, das im Argument Kriterien enthalten ist, muss auch ein Feld in *In* sein.</span><span class="sxs-lookup"><span data-stu-id="9648e-123">Any field that is included in criteria must also be a field in  *In*  .</span></span>  <br/> |
|<span data-ttu-id="9648e-124">**Alias**</span><span class="sxs-lookup"><span data-stu-id="9648e-124">**Alias**</span></span> <br/> |<span data-ttu-id="9648e-125">Nein</span><span class="sxs-lookup"><span data-stu-id="9648e-125">No</span></span>  <br/> |<span data-ttu-id="9648e-126">Eine Zeichenfolge, die einen alternativen Namen für die Domäne, die durch das Argument *im* angegebenen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="9648e-126">A string that provides an alternative name for the domain specified by the  *In*  argument.</span></span> <span data-ttu-id="9648e-127">Häufig verwendet, um den Tabellennamen für nachfolgende Verweise zu verhindern, dass mögliche mehrdeutige Verweise zu verkürzen.</span><span class="sxs-lookup"><span data-stu-id="9648e-127">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.</span></span> <span data-ttu-id="9648e-128">Wenn *Alias* nicht angegeben ist, wird den Namen der Tabelle oder Abfrage als Alias verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9648e-128">If  *Alias*  is not specified, the table or query name will be used as the alias.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9648e-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9648e-129">Remarks</span></span>

<span data-ttu-id="9648e-130">Mit der **[BeendenFürJedenDatensatz](exitforeachrecord-macro-action-access-custom-web-app.md)** -Aktion beenden Sie einen **FürJedenDatensatz** -Datenblock sofort.</span><span class="sxs-lookup"><span data-stu-id="9648e-130">Use the **[ExitForEachRecord](exitforeachrecord-macro-action-access-custom-web-app.md)** action to exit a **ForEachRecord** data block immediately.</span></span> 
  

