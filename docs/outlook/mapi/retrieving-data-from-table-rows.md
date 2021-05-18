---
title: Abrufen von Daten aus Tabellenzeilen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 19a42794-a3a2-4336-af2a-473f24431252
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2f389d26ec80b9af3ed28c5eb85b589c9cbb26c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405254"
---
# <a name="retrieving-data-from-table-rows"></a><span data-ttu-id="d7166-103">Abrufen von Daten aus Tabellenzeilen</span><span class="sxs-lookup"><span data-stu-id="d7166-103">Retrieving Data from Table Rows</span></span>

  
  
<span data-ttu-id="d7166-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7166-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7166-105">Das Abrufen von Zeilen aus einer Tabelle umfasst:</span><span class="sxs-lookup"><span data-stu-id="d7166-105">Retrieving rows from a table involves:</span></span>
  
- <span data-ttu-id="d7166-106">Abrufen der Eigenschaftswerte für alle Spalten.</span><span class="sxs-lookup"><span data-stu-id="d7166-106">Obtaining the property values for all the columns.</span></span>
    
- <span data-ttu-id="d7166-107">Ändern der aktuellen Position.</span><span class="sxs-lookup"><span data-stu-id="d7166-107">Modifying the current position.</span></span>
    
<span data-ttu-id="d7166-108">Eine der erforderlichen Spalten in den meisten Tabellen ist eine Eintrags-ID , die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) -Eigenschaft, die zum Öffnen des Objekts verwendet werden kann, das die Zeile darstellt.</span><span class="sxs-lookup"><span data-stu-id="d7166-108">One of the required columns in most tables is an entry identifier — the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property — that can be used to open the object that represents the row.</span></span> <span data-ttu-id="d7166-109">Dieser Eintragsbezeichner ist in der Regel eine kurzfristige Eintrags-ID, die nicht über die Lebensdauer der Tabelle hinaus beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="d7166-109">This entry identifier is usually a short-term entry identifier, one that does not persist past the lifetime of the table.</span></span> <span data-ttu-id="d7166-110">Es kann jedoch eine langfristige ID sein, wenn der Dienstanbieter, der die Tabelle implementieren, nur einen Typ von Eintrags-ID unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d7166-110">However, it can be a long-term identifier if the service provider implementing the table only supports one type of entry identifier.</span></span>
  
<span data-ttu-id="d7166-111">Clients und Dienstanbieter können einen der folgenden Aufrufe zum Abrufen von Zeilen erstellen:</span><span class="sxs-lookup"><span data-stu-id="d7166-111">Clients and service providers can make one of the following calls to retrieve rows:</span></span>
  
|||
|:-----|:-----|
|[<span data-ttu-id="d7166-112">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="d7166-112">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="d7166-113">Ruft eine angegebene Anzahl von Zeilen ab, die mit der aktuellen Zeile in Vorwärts- oder Rückwärtsrichtung beginnen.</span><span class="sxs-lookup"><span data-stu-id="d7166-113">Retrieves a specified number of rows starting with the current row in either a forward or backward direction.</span></span>  <br/> |
|[<span data-ttu-id="d7166-114">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="d7166-114">HrQueryAllRows</span></span>](hrqueryallrows.md) <br/> |<span data-ttu-id="d7166-115">Ruft alle Zeilen in einer Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="d7166-115">Retrieves all of the rows in a table.</span></span>  <br/> |
|[<span data-ttu-id="d7166-116">ITableData::HrQueryRow</span><span class="sxs-lookup"><span data-stu-id="d7166-116">ITableData::HrQueryRow</span></span>](itabledata-hrqueryrow.md) <br/> |<span data-ttu-id="d7166-117">Ruft eine Zeile in einer Tabelle entsprechend dem Wert der Indexspalte ab.</span><span class="sxs-lookup"><span data-stu-id="d7166-117">Retrieves a row in a table according to the value of its index column.</span></span> <span data-ttu-id="d7166-118">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) ist in der Regel die Indexspalte für eine Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d7166-118">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) is usually the index column for a table.</span></span>  <br/> |
   
<span data-ttu-id="d7166-119">Wenn eine optionale Eigenschaft als eine der Spalten in einer Tabelle enthalten ist, verfügen einige der Zeilen möglicherweise über gültige Werte für die Spalte, andere nicht.</span><span class="sxs-lookup"><span data-stu-id="d7166-119">When an optional property is included as one of the columns in a table, some of the rows might have valid values for the column while others might not.</span></span> <span data-ttu-id="d7166-120">Ob ein gültiger Wert für eine Spalte vorhanden ist, hängt davon ab, ob das Objekt, das die Informationen für die Zeile liefert, die Eigenschaft legt.</span><span class="sxs-lookup"><span data-stu-id="d7166-120">Whether a valid value exists for a column depends on whether the object providing the information for the row sets the property.</span></span> <span data-ttu-id="d7166-121">Je nach Implementierung des Objekts kann eine nicht vorhandene Eigenschaft in der Tabelle als PR_NULL **(** [PidTagNull](pidtagnull-canonical-property.md)) oder als beliebiger Wert dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d7166-121">Depending on the implementation of the object, a non-existent property can be represented in the table as **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) or an arbitrary value.</span></span> <span data-ttu-id="d7166-122">Benutzer von Tabellen müssen darauf achten, zwischen Eigenschaften zu unterscheiden, die nicht vorhanden sind und bedeutungslose Werte und Eigenschaften aufweisen, die vorhanden sind und gültige Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d7166-122">Users of tables must be careful to differentiate between properties that are nonexistent and have meaningless values and properties that do exist and have valid values.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d7166-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d7166-123">See also</span></span>



[<span data-ttu-id="d7166-124">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="d7166-124">MAPI Tables</span></span>](mapi-tables.md)

