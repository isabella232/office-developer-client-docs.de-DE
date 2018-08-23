---
title: Tipps zum Arbeiten mit Tabellen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: adb4d589-7e03-4222-8717-898ef397c6b6
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d9b4d6a469904058b0484428dbf20a90119e96bc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586137"
---
# <a name="tips-for-working-with-tables"></a><span data-ttu-id="9f178-103">Tipps zum Arbeiten mit Tabellen</span><span class="sxs-lookup"><span data-stu-id="9f178-103">Tips for Working with Tables</span></span>

  
  
<span data-ttu-id="9f178-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f178-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f178-105">Arbeiten mit einem MAPI ist Tabelle etwas like arbeiten mit einer relationalen Datenbank-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="9f178-105">Working with a MAPI table is a little like working with a relational database table.</span></span> <span data-ttu-id="9f178-106">Ein Benutzer kann die Anzahl der Zeilen und Spalten in der Ansicht und ihre Reihenfolge angeben.</span><span class="sxs-lookup"><span data-stu-id="9f178-106">A user can limit the number of rows and columns in the view and specify their order.</span></span> <span data-ttu-id="9f178-107">Zeilen können abgerufenen jeweils einzeln oder in Gruppen werden.</span><span class="sxs-lookup"><span data-stu-id="9f178-107">Rows can be retrieved one at a time or in groups.</span></span> <span data-ttu-id="9f178-108">Ein Cursor, das verfolgt die aktuelle Position kann zu einer bestimmten Stelle in der Tabelle verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="9f178-108">A cursor that keeps track of the current position can be moved to a specific place in the table.</span></span> 
  
<span data-ttu-id="9f178-109">Zum Arbeiten mit Tabellen Clients verwenden die Schnittstelle schreibgeschützt [IMAPITable: IUnknown](imapitableiunknown.md), während der Dienstanbieter, je nachdem, ob sie die Daten besitzen, die die Tabelle basiert entweder **IMAPITable** verwenden können oder [ITableData: IUnknown](itabledataiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="9f178-109">To work with tables, clients use the read-only interface, [IMAPITable : IUnknown](imapitableiunknown.md), whereas service providers, depending on whether they own the data that the table is based on, can use either **IMAPITable** or [ITableData : IUnknown](itabledataiunknown.md).</span></span> <span data-ttu-id="9f178-110">Die in diese Schnittstellen definierten Vorgänge können als Vorgänge, die alle Benutzer der Tabellen oder aufgerufen werden können und Vorgänge, die nicht so weit verbreitet verwendet werden, da sie weitergehender kategorisiert werden.</span><span class="sxs-lookup"><span data-stu-id="9f178-110">The operations defined in these interfaces can be categorized as operations that all users of tables either do or can invoke and operations that are not as widely used because they are more advanced.</span></span> <span data-ttu-id="9f178-111">Einige der erweiterten Vorgänge sind schwieriger zu implementieren. andere Benutzer sind nicht komplexer, aber für eine kleine kleiner Teil der MAPI-Komponenten von Interesse sind.</span><span class="sxs-lookup"><span data-stu-id="9f178-111">Some of the advanced operations are more complex to implement; others are no more complex, but are of interest to a small minority of MAPI components.</span></span> 
  
<span data-ttu-id="9f178-112">Die häufiger Vorgänge sind:</span><span class="sxs-lookup"><span data-stu-id="9f178-112">The more common operations are:</span></span>
  
- <span data-ttu-id="9f178-113">Spalte Vorgänge, die einzelne Spalten beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="9f178-113">Column operations, which affect single columns.</span></span> <span data-ttu-id="9f178-114">Dazu gehören das Angeben der Eigenschaften enthalten sein, in der Spalte und der Reihenfolge, in der sie eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9f178-114">These include specifying the properties to be included in the column set and the order in which they should be included.</span></span>
    
- <span data-ttu-id="9f178-115">Zeile Vorgänge, die einzelne Zeilen zu beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="9f178-115">Row operations, which affect single rows.</span></span> <span data-ttu-id="9f178-116">Abrufen von Daten und die Wartungsvorgänge beinhalten: hinzufügen, löschen und ändern eine einzelne Zeile oder Zeilen.</span><span class="sxs-lookup"><span data-stu-id="9f178-116">These include data retrieval and the maintenance operations: adding, deleting, and modifying a single row or rows.</span></span>
    
- <span data-ttu-id="9f178-117">Globale Vorgänge, die sich auf die gesamte Tabelle auswirken.</span><span class="sxs-lookup"><span data-stu-id="9f178-117">Global operations, which affect the entire table.</span></span> <span data-ttu-id="9f178-118">Dazu gehören ereignisbenachrichtigung, suchen und sortieren.</span><span class="sxs-lookup"><span data-stu-id="9f178-118">These include event notification, searching and sorting.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9f178-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f178-119">See also</span></span>



[<span data-ttu-id="9f178-120">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="9f178-120">MAPI Tables</span></span>](mapi-tables.md)

