---
title: Arbeiten mit mehrwertigen Spalten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 911a41c3-c10f-4473-8853-fafb56b721ba
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 34f19e279c86e0c0856d242cf2aa13d744d46f13
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420185"
---
# <a name="working-with-multivalued-columns"></a><span data-ttu-id="13b1a-103">Arbeiten mit mehrwertigen Spalten</span><span class="sxs-lookup"><span data-stu-id="13b1a-103">Working with Multivalued Columns</span></span>

  
  
<span data-ttu-id="13b1a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="13b1a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="13b1a-105">Eine mehrwertige Spalte enthält die Daten einer mehrwertigen Eigenschaft, bei der es sich um eine Eigenschaft mit einem Array von Werten des Basistyps anstelle eines einzelnen Werts handelt.</span><span class="sxs-lookup"><span data-stu-id="13b1a-105">A multivalued column contains the data of a multivalued property, which is a property that has an array of values of the base type instead of a single value.</span></span> <span data-ttu-id="13b1a-106">Da keine der Tabellen mehrwertige Eigenschaften in ihren Standardspaltensätzen enthält, sind mehrwertige Eigenschaften nur dann in einer Tabelle enthalten, wenn der Benutzer der Tabelle sie anfordert.</span><span class="sxs-lookup"><span data-stu-id="13b1a-106">Because none of the tables include multivalued properties in their default column sets, multivalued properties are included in a table only if the user of the table requests it.</span></span> 
  
<span data-ttu-id="13b1a-107">Mehrwertige Spalten können in Tabellen angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="13b1a-107">Multivalued columns can be displayed in tables:</span></span>
  
- <span data-ttu-id="13b1a-108">In einer einzelnen Zeile, bei der alle Eigenschaftswerte in der Instanz einer einzelnen Spalte angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="13b1a-108">In a single row, with all of the property values appearing in the single column instance.</span></span> <span data-ttu-id="13b1a-109">Dies ist die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="13b1a-109">This is the default.</span></span>
    
    - <span data-ttu-id="13b1a-110">Oder -</span><span class="sxs-lookup"><span data-stu-id="13b1a-110">Or -</span></span>
    
- <span data-ttu-id="13b1a-111">In einer Reihe von Zeilen mit einer Zeile für jeden Eigenschaftswerte.</span><span class="sxs-lookup"><span data-stu-id="13b1a-111">In a series of rows, with one row for each of the property values.</span></span> <span data-ttu-id="13b1a-112">Jeder eindeutige Wert wird in der Spalte in seiner eigenen Zeile angezeigt, und es gibt so viele Zeilen wie Werte in der mehrwertigen Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="13b1a-112">Each unique value appears in the column in its own row with there being as many rows as there are values in the multivalued property.</span></span> <span data-ttu-id="13b1a-113">Jede Zeile hat einen eindeutigen Wert für die **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) -Eigenschaft, aber die gleichen Werte für die anderen Spalten.</span><span class="sxs-lookup"><span data-stu-id="13b1a-113">Each row has a unique value for the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property, but the same values for the other columns.</span></span> <span data-ttu-id="13b1a-114">Wenn eine Zeile mehr als eine Spalte mit mehreren Werten enthält, z. B. zwei Spalten mit  _M-_ bzw.  _N-Werten,_ werden  _M \* N-Instanzen_ der Zeile in der Tabelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="13b1a-114">If a row contains more than one column with multiple values, for example, two columns with  _M_ and  _N_ values respectively, then  _M\*N_ instances of the row appear in the table.</span></span> 
    
<span data-ttu-id="13b1a-115">Ein Tabellenbenutzer fordert den nicht standardmäßigen Anzeigetyp an, indem er die [IMAPITable::SetColumns-Methode](imapitable-setcolumns.md) aufruft, deren MVI_FLAG-Flag im Eigenschaftstyp der mehrwertigen Spalte festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="13b1a-115">A table user requests the nondefault type of display by calling the [IMAPITable::SetColumns](imapitable-setcolumns.md) method with the MVI_FLAG flag set in the property type of the multivalued column.</span></span> <span data-ttu-id="13b1a-116">Das MVI_FLAG ist eine Konstante, die als Ergebnis der Kombination der MV_FLAG- und MV_INSTANCE-Flags mit einem logischen **OR-Vorgang definiert** ist.</span><span class="sxs-lookup"><span data-stu-id="13b1a-116">The MVI_FLAG flag is a constant defined as the result of combining the MV_FLAG and MV_INSTANCE flags with a logical **OR** operation.</span></span> <span data-ttu-id="13b1a-117">Neben der Verwendung in **SetColumns** kann MVI_FLAG auch an [IMAPITable::SortTable](imapitable-sorttable.md) im  _parameter lpSortCriteria_ und [IMAPITable::Restrict](imapitable-restrict.md) im **ulPropTag-Element** des  _lpRestriction-Parameters_ übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="13b1a-117">In addition to being used in **SetColumns**, MVI_FLAG can also be passed to [IMAPITable::SortTable](imapitable-sorttable.md) in the  _lpSortCriteria_ parameter and [IMAPITable::Restrict](imapitable-restrict.md) in the **ulPropTag** member of the  _lpRestriction_ parameter.</span></span> <span data-ttu-id="13b1a-118">Wenn die MVI_FLAG übergeben wird, führt **SortTable** eine ähnliche Leistung wie **SetColumns** aus, fügt für jeden Wert in der mehrwertigen Spalte eine Zeile hinzu und sortiert die einzelnen Werte in den Instanzen.</span><span class="sxs-lookup"><span data-stu-id="13b1a-118">When passed the MVI_FLAG, **SortTable** performs similarly to **SetColumns**, adding one row for each value in the multivalued column and sorting on the single values in the instances.</span></span> <span data-ttu-id="13b1a-119">Für jeden Wert wird eine Zeile hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="13b1a-119">One row is added for each value.</span></span> 
  
 <span data-ttu-id="13b1a-120">**Restrict** erweitert die mehrwertige Spalte jedoch nicht in zusätzliche berechnete Zeilen.</span><span class="sxs-lookup"><span data-stu-id="13b1a-120">**Restrict**, however, does not expand the multivalued column into additional computed rows.</span></span> <span data-ttu-id="13b1a-121">Eine mehrwertige Spalte mit MVI_FLAG Dienstanbieter angewiesen, diese Spalte beim Einschränken der Tabelle zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="13b1a-121">A multivalued column with the MVI_FLAG set instructs the service provider to use that column in restricting the table.</span></span> <span data-ttu-id="13b1a-122">Wenn in der Einschränkung ein Eigenschaftswert enthalten ist, muss es sich um ein einzelnes Werteigenschaftstag handelt, das mit dem Tag identisch ist, das von [IMAPITable::QueryRows](imapitable-queryrows.md) für die Spalte zurückgegeben würde.</span><span class="sxs-lookup"><span data-stu-id="13b1a-122">If there is a property value in the restriction, it must be a single value property tag identical to the one that would be returned by [IMAPITable::QueryRows](imapitable-queryrows.md) for the column.</span></span> 
  
<span data-ttu-id="13b1a-123">Tabellen implementierer sind nur erforderlich, um den Standardanzeigetyp zu unterstützen und können den MAPI_E_TOO_COMPLEX zurückgeben, wenn ein Aufrufer die andere Alternative anfordert.</span><span class="sxs-lookup"><span data-stu-id="13b1a-123">Table implementers are only required to support the default type of display and can return the MAPI_E_TOO_COMPLEX value when a caller requests the other alternative.</span></span> <span data-ttu-id="13b1a-124">Die Möglichkeit, beide Anzeigetypen zu unterstützen, ist für Nachrichtenspeicheranbieter, die Ordnerinhaltstabellen implementieren, am wichtigsten.</span><span class="sxs-lookup"><span data-stu-id="13b1a-124">The ability to support both types of display is most important for message store providers implementing folder contents tables.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="13b1a-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13b1a-125">See also</span></span>



[<span data-ttu-id="13b1a-126">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="13b1a-126">MAPI Tables</span></span>](mapi-tables.md)

