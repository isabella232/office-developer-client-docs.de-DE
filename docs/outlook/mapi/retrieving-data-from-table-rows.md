---
title: Abrufen von Daten aus einer Tabellenzeilen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 19a42794-a3a2-4336-af2a-473f24431252
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 91b1fa06fd47321e9c19d9751caac793e27e8f16
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795394"
---
# <a name="retrieving-data-from-table-rows"></a><span data-ttu-id="e0f3d-103">Abrufen von Daten aus einer Tabellenzeilen</span><span class="sxs-lookup"><span data-stu-id="e0f3d-103">Retrieving Data from Table Rows</span></span>

  
  
<span data-ttu-id="e0f3d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e0f3d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e0f3d-105">Abrufen von Zeilen aus einer Tabelle umfasst:</span><span class="sxs-lookup"><span data-stu-id="e0f3d-105">Retrieving rows from a table involves:</span></span>
  
- <span data-ttu-id="e0f3d-106">Abrufen der Eigenschaftswerte für alle Spalten.</span><span class="sxs-lookup"><span data-stu-id="e0f3d-106">Obtaining the property values for all the columns.</span></span>
    
- <span data-ttu-id="e0f3d-107">Ändern der aktuellen Position.</span><span class="sxs-lookup"><span data-stu-id="e0f3d-107">Modifying the current position.</span></span>
    
<span data-ttu-id="e0f3d-108">Einer der erforderlichen Spalten in den meisten Tabellen ist eine Eintrags-ID – die Eigenschaft **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) –, die verwendet werden kann, um das Objekt zu öffnen, das die Zeile darstellt.</span><span class="sxs-lookup"><span data-stu-id="e0f3d-108">One of the required columns in most tables is an entry identifier — the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property — that can be used to open the object that represents the row.</span></span> <span data-ttu-id="e0f3d-109">Dieses Eintrags-ID ist in der Regel eine kurzfristige Eintrags-ID, eine, die nicht über die Lebensdauer der Tabelle beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="e0f3d-109">This entry identifier is usually a short-term entry identifier, one that does not persist past the lifetime of the table.</span></span> <span data-ttu-id="e0f3d-110">Es kann jedoch ein langfristige Bezeichner sein, wenn der Dienstanbieter Implementieren der Tabelle nur ein Typ von Eintrags-ID unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e0f3d-110">However, it can be a long-term identifier if the service provider implementing the table only supports one type of entry identifier.</span></span>
  
<span data-ttu-id="e0f3d-111">Clients und Dienstanbieter können einen der folgenden Aufrufe abzurufenden Zeilen vornehmen:</span><span class="sxs-lookup"><span data-stu-id="e0f3d-111">Clients and service providers can make one of the following calls to retrieve rows:</span></span>
  
|||
|:-----|:-----|
|[<span data-ttu-id="e0f3d-112">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="e0f3d-112">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="e0f3d-113">Ruft eine angegebene Anzahl von Zeilen beginnend mit der aktuellen Zeile in vorwärts oder rückwärts ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e0f3d-113">Retrieves a specified number of rows starting with the current row in either a forward or backward direction.</span></span>  <br/> |
|[<span data-ttu-id="e0f3d-114">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="e0f3d-114">HrQueryAllRows</span></span>](hrqueryallrows.md) <br/> |<span data-ttu-id="e0f3d-115">Ruft alle Zeilen in einer Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="e0f3d-115">Retrieves all of the rows in a table.</span></span>  <br/> |
|[<span data-ttu-id="e0f3d-116">ITableData::HrQueryRow</span><span class="sxs-lookup"><span data-stu-id="e0f3d-116">ITableData::HrQueryRow</span></span>](itabledata-hrqueryrow.md) <br/> |<span data-ttu-id="e0f3d-117">Ruft eine Zeile in einer Tabelle entsprechend dem Wert der Index-Spalte.</span><span class="sxs-lookup"><span data-stu-id="e0f3d-117">Retrieves a row in a table according to the value of its index column.</span></span> <span data-ttu-id="e0f3d-118">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) ist in der Regel die Indexspalte für eine Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e0f3d-118">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) is usually the index column for a table.</span></span>  <br/> |
   
<span data-ttu-id="e0f3d-119">Wenn eine optionale Eigenschaft als eine der Spalten in einer Tabelle enthalten ist, möglicherweise einige der Zeilen gültige Werte für die Spalte haben, während andere Benutzer nicht möglicherweise.</span><span class="sxs-lookup"><span data-stu-id="e0f3d-119">When an optional property is included as one of the columns in a table, some of the rows might have valid values for the column while others might not.</span></span> <span data-ttu-id="e0f3d-120">Gibt an, ob ein gültiger Wert für eine Spalte vorhanden ist, hängt davon ab, ob das Objekt, und geben Sie Informationen für die Zeile die-Eigenschaft festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="e0f3d-120">Whether a valid value exists for a column depends on whether the object providing the information for the row sets the property.</span></span> <span data-ttu-id="e0f3d-121">Je nach der Implementierung des Objekts kann eine nicht vorhandene Eigenschaft in der Tabelle als **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) oder ein beliebiger Wert dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="e0f3d-121">Depending on the implementation of the object, a non-existent property can be represented in the table as **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) or an arbitrary value.</span></span> <span data-ttu-id="e0f3d-122">Benutzer von Tabellen müssen achten unterscheiden zwischen Eigenschaften, die nicht vorhanden sind und keine Bedeutung Werte und Eigenschaften, die vorhanden und sind gültige Werte.</span><span class="sxs-lookup"><span data-stu-id="e0f3d-122">Users of tables must be careful to differentiate between properties that are nonexistent and have meaningless values and properties that do exist and have valid values.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e0f3d-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0f3d-123">See also</span></span>



[<span data-ttu-id="e0f3d-124">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="e0f3d-124">MAPI Tables</span></span>](mapi-tables.md)

