---
title: Arbeiten mit Spalten mit mehreren Werten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 911a41c3-c10f-4473-8853-fafb56b721ba
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ee3307836e8b167efbc2cdc870e698257526ef97
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795866"
---
# <a name="working-with-multivalued-columns"></a><span data-ttu-id="e153a-103">Arbeiten mit Spalten mit mehreren Werten</span><span class="sxs-lookup"><span data-stu-id="e153a-103">Working with Multivalued Columns</span></span>

  
  
<span data-ttu-id="e153a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e153a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e153a-105">Mehrwertige Spalte enthält die Daten der eine mehrwertige Eigenschaft, die eine Eigenschaft, die ein Array von Werten vom Basistyp anstatt einen single-Wert aufweist.</span><span class="sxs-lookup"><span data-stu-id="e153a-105">A multivalued column contains the data of a multivalued property, which is a property that has an array of values of the base type instead of a single value.</span></span> <span data-ttu-id="e153a-106">Weil keine der Tabellen die Spalte Standardgruppen mehrwertige Eigenschaften verwendet, sind mehrwertige Eigenschaften in einer Tabelle enthalten nur, wenn der Tabelle der Benutzer diese anfordert.</span><span class="sxs-lookup"><span data-stu-id="e153a-106">Because none of the tables include multivalued properties in their default column sets, multivalued properties are included in a table only if the user of the table requests it.</span></span> 
  
<span data-ttu-id="e153a-107">Mehrwertige Spalten können in Tabellen angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="e153a-107">Multivalued columns can be displayed in tables:</span></span>
  
- <span data-ttu-id="e153a-108">In einer einzelnen Zeile mit allen der Eigenschaftswerte in der Instanz einspaltige angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e153a-108">In a single row, with all of the property values appearing in the single column instance.</span></span> <span data-ttu-id="e153a-109">Dies ist die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="e153a-109">This is the default.</span></span>
    
    - <span data-ttu-id="e153a-110">Oder -</span><span class="sxs-lookup"><span data-stu-id="e153a-110">Or -</span></span>
    
- <span data-ttu-id="e153a-111">In einer Reihe von Zeilen, mit der eine Zeile für jeden der Eigenschaftswerte.</span><span class="sxs-lookup"><span data-stu-id="e153a-111">In a series of rows, with one row for each of the property values.</span></span> <span data-ttu-id="e153a-112">Wie viele Zeilen als dort Werte in der mehrwertigen Eigenschaft sind, wird in der Spalte in einer eigenen Zeile mit jedem eindeutiger Wert angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e153a-112">Each unique value appears in the column in its own row with there being as many rows as there are values in the multivalued property.</span></span> <span data-ttu-id="e153a-113">Jede Zeile enthält einen eindeutigen Wert für die **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))-Eigenschaft, aber die gleichen Werte für die anderen Spalten.</span><span class="sxs-lookup"><span data-stu-id="e153a-113">Each row has a unique value for the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property, but the same values for the other columns.</span></span> <span data-ttu-id="e153a-114">Wenn eine Zeile mehr als eine Spalte mit mehreren Werten enthält, beispielsweise zwei Spalten mit _M_ und _N_ Werte, die jeweils dann _M\*N_ Instanzen der Zeile in der Tabelle angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e153a-114">If a row contains more than one column with multiple values, for example, two columns with  _M_ and  _N_ values respectively, then  _M\*N_ instances of the row appear in the table.</span></span> 
    
<span data-ttu-id="e153a-115">Ein Tabelle Benutzer fordert die nicht standardmäßigen Art der Anzeige durch Aufrufen der [IMAPITable::SetColumns](imapitable-setcolumns.md) -Methode mit dem MVI_FLAG-Flag in den Eigenschaftstyp der mehrwertige Spalte festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e153a-115">A table user requests the nondefault type of display by calling the [IMAPITable::SetColumns](imapitable-setcolumns.md) method with the MVI_FLAG flag set in the property type of the multivalued column.</span></span> <span data-ttu-id="e153a-116">Das Flag MVI_FLAG ist eine Konstante, die als Ergebnis der Kombination von die Flags MV_FLAG und MV_INSTANCE vorhanden und eine logische **OR** -Operation definiert.</span><span class="sxs-lookup"><span data-stu-id="e153a-116">The MVI_FLAG flag is a constant defined as the result of combining the MV_FLAG and MV_INSTANCE flags with a logical **OR** operation.</span></span> <span data-ttu-id="e153a-117">Neben den in **SetColumns**verwendet wird, kann MVI_FLAG auch an [SortTable](imapitable-sorttable.md) in den _LpSortCriteria_ -Parameter und die [Methode IMAPITable:: Restrict](imapitable-restrict.md) im **UlPropTag** -Member der _LpRestriction_ übergeben werden der Parameter.</span><span class="sxs-lookup"><span data-stu-id="e153a-117">In addition to being used in **SetColumns**, MVI_FLAG can also be passed to [IMAPITable::SortTable](imapitable-sorttable.md) in the  _lpSortCriteria_ parameter and [IMAPITable::Restrict](imapitable-restrict.md) in the **ulPropTag** member of the  _lpRestriction_ parameter.</span></span> <span data-ttu-id="e153a-118">Wenn die MVI_FLAG übergeben, verhält **SortTable** wie **SetColumns**, eine Zeile für jeden Wert in der mehrwertigen Spalte hinzufügen und auf die einzelnen Werte in die Instanzen sortieren.</span><span class="sxs-lookup"><span data-stu-id="e153a-118">When passed the MVI_FLAG, **SortTable** performs similarly to **SetColumns**, adding one row for each value in the multivalued column and sorting on the single values in the instances.</span></span> <span data-ttu-id="e153a-119">Eine Zeile wird für jeden Wert hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e153a-119">One row is added for each value.</span></span> 
  
 <span data-ttu-id="e153a-120">**Restrict**, wird jedoch nicht mehrwertige Spalte in zusätzliche berechnete Zeilen erweitert.</span><span class="sxs-lookup"><span data-stu-id="e153a-120">**Restrict**, however, does not expand the multivalued column into additional computed rows.</span></span> <span data-ttu-id="e153a-121">Mehrwertige Spalte mit dem MVI_FLAG weist den Dienstanbieter, verwenden Sie diese Spalte in der Tabelle einschränken.</span><span class="sxs-lookup"><span data-stu-id="e153a-121">A multivalued column with the MVI_FLAG set instructs the service provider to use that column in restricting the table.</span></span> <span data-ttu-id="e153a-122">Wenn der Wert einer Eigenschaft in der Einschränkung vorhanden ist, muss es sich ein einzelner Wert-Eigenschaftentag identisch mit demjenigen handeln, die für die Spalte von [IMAPITable::QueryRows](imapitable-queryrows.md) zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e153a-122">If there is a property value in the restriction, it must be a single value property tag identical to the one that would be returned by [IMAPITable::QueryRows](imapitable-queryrows.md) for the column.</span></span> 
  
<span data-ttu-id="e153a-123">Tabelle Implementierer sind nur erforderlich, um die standardmäßige Art der Anzeige unterstützen und können den MAPI_E_TOO_COMPLEX-Wert zurück, wenn ein Anrufer die anderen Alternative anfordert.</span><span class="sxs-lookup"><span data-stu-id="e153a-123">Table implementers are only required to support the default type of display and can return the MAPI_E_TOO_COMPLEX value when a caller requests the other alternative.</span></span> <span data-ttu-id="e153a-124">Die Möglichkeit zur Unterstützung von beide Arten von Anzeige ist wichtigste für Nachricht Anbieter Ordner Inhalt Tabellen implementieren.</span><span class="sxs-lookup"><span data-stu-id="e153a-124">The ability to support both types of display is most important for message store providers implementing folder contents tables.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e153a-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e153a-125">See also</span></span>



[<span data-ttu-id="e153a-126">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="e153a-126">MAPI Tables</span></span>](mapi-tables.md)

