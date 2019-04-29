---
title: Tipps für das Arbeiten mit Tabellen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: adb4d589-7e03-4222-8717-898ef397c6b6
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8f310c6331df941d3093b276b6dec47f740412e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439737"
---
# <a name="tips-for-working-with-tables"></a><span data-ttu-id="e19ee-103">Tipps für das Arbeiten mit Tabellen</span><span class="sxs-lookup"><span data-stu-id="e19ee-103">Tips for Working with Tables</span></span>

  
  
<span data-ttu-id="e19ee-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e19ee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e19ee-105">Das Arbeiten mit einer MAPI-Tabelle ähnelt dem Arbeiten mit einer relationalen Datenbanktabelle.</span><span class="sxs-lookup"><span data-stu-id="e19ee-105">Working with a MAPI table is a little like working with a relational database table.</span></span> <span data-ttu-id="e19ee-106">Ein Benutzer kann die Anzahl der Zeilen und Spalten in der Ansicht begrenzen und deren Reihenfolge angeben.</span><span class="sxs-lookup"><span data-stu-id="e19ee-106">A user can limit the number of rows and columns in the view and specify their order.</span></span> <span data-ttu-id="e19ee-107">Zeilen können einzeln oder in Gruppen abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e19ee-107">Rows can be retrieved one at a time or in groups.</span></span> <span data-ttu-id="e19ee-108">Ein Cursor, der die aktuelle Position verfolgt, kann an eine bestimmte Stelle in der Tabelle verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="e19ee-108">A cursor that keeps track of the current position can be moved to a specific place in the table.</span></span> 
  
<span data-ttu-id="e19ee-109">Zum Arbeiten mit Tabellen verwenden Clients die schreibgeschützte Schnittstelle [IMAPITable: IUnknown](imapitableiunknown.md), wohingegen Dienstanbieter, je nachdem, ob Sie die Daten besitzen, auf denen die Tabelle basiert, entweder **IMAPITable** oder [ITableData: IUnknown](itabledataiunknown.md)verwenden können.</span><span class="sxs-lookup"><span data-stu-id="e19ee-109">To work with tables, clients use the read-only interface, [IMAPITable : IUnknown](imapitableiunknown.md), whereas service providers, depending on whether they own the data that the table is based on, can use either **IMAPITable** or [ITableData : IUnknown](itabledataiunknown.md).</span></span> <span data-ttu-id="e19ee-110">Die in diesen Schnittstellen definierten Vorgänge können als Vorgänge kategorisiert werden, die von allen Benutzern von Tabellen ausgeführt oder aufgerufen werden können, und Vorgänge, die nicht so häufig verwendet werden, da Sie weiter fortgeschritten sind.</span><span class="sxs-lookup"><span data-stu-id="e19ee-110">The operations defined in these interfaces can be categorized as operations that all users of tables either do or can invoke and operations that are not as widely used because they are more advanced.</span></span> <span data-ttu-id="e19ee-111">Einige der erweiterten Vorgänge sind komplexer zu implementieren; andere sind nicht komplexer, sondern interessieren sich für eine kleine Gruppe von MAPI-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="e19ee-111">Some of the advanced operations are more complex to implement; others are no more complex, but are of interest to a small minority of MAPI components.</span></span> 
  
<span data-ttu-id="e19ee-112">Die gängigeren Vorgänge sind:</span><span class="sxs-lookup"><span data-stu-id="e19ee-112">The more common operations are:</span></span>
  
- <span data-ttu-id="e19ee-113">Spalten Vorgänge, die sich auf einzelne Spalten auswirken.</span><span class="sxs-lookup"><span data-stu-id="e19ee-113">Column operations, which affect single columns.</span></span> <span data-ttu-id="e19ee-114">Dazu gehören das Angeben der Eigenschaften, die in den Spaltensatz eingeschlossen werden sollen, und die Reihenfolge, in der Sie eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e19ee-114">These include specifying the properties to be included in the column set and the order in which they should be included.</span></span>
    
- <span data-ttu-id="e19ee-115">Zeilenvorgänge, die sich auf einzelne Zeilen auswirken.</span><span class="sxs-lookup"><span data-stu-id="e19ee-115">Row operations, which affect single rows.</span></span> <span data-ttu-id="e19ee-116">Hierzu gehört der Datenabruf und die Wartungsvorgänge: Hinzufügen, löschen und Ändern einer einzelnen Zeile oder Zeilen.</span><span class="sxs-lookup"><span data-stu-id="e19ee-116">These include data retrieval and the maintenance operations: adding, deleting, and modifying a single row or rows.</span></span>
    
- <span data-ttu-id="e19ee-117">Globale Vorgänge, die sich auf die gesamte Tabelle auswirken.</span><span class="sxs-lookup"><span data-stu-id="e19ee-117">Global operations, which affect the entire table.</span></span> <span data-ttu-id="e19ee-118">Dazu gehört die Ereignisbenachrichtigung, das Suchen und sortieren.</span><span class="sxs-lookup"><span data-stu-id="e19ee-118">These include event notification, searching and sorting.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e19ee-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e19ee-119">See also</span></span>



[<span data-ttu-id="e19ee-120">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="e19ee-120">MAPI Tables</span></span>](mapi-tables.md)

