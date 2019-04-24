---
title: HrQueryAllRows
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrQueryAllRows
api_type:
- HeaderDef
ms.assetid: b08fadcf-cdf3-48b7-9489-d7f745266482
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0f09304f21180d9ebc2a1e1dcc54ebadd3622804
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348244"
---
# <a name="hrqueryallrows"></a><span data-ttu-id="f9193-103">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="f9193-103">HrQueryAllRows</span></span>

  
  
<span data-ttu-id="f9193-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f9193-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f9193-105">Ruft alle Zeilen einer Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="f9193-105">Retrieves all rows of a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f9193-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="f9193-106">Header file:</span></span>  <br/> |<span data-ttu-id="f9193-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="f9193-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f9193-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="f9193-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f9193-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f9193-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f9193-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="f9193-110">Called by:</span></span>  <br/> |<span data-ttu-id="f9193-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="f9193-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrQueryAllRows(
  LPMAPITABLE ptable,
  LPSPropTagArray ptaga,
  LPSRestriction pres,
  LPSSortOrderSet psos,
  LONG crowsMax,
  LPSRowSet FAR * pprows
);
```

## <a name="parameters"></a><span data-ttu-id="f9193-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9193-112">Parameters</span></span>

 <span data-ttu-id="f9193-113">_ptable_</span><span class="sxs-lookup"><span data-stu-id="f9193-113">_ptable_</span></span>
  
> <span data-ttu-id="f9193-114">in Zeiger auf die MAPI-Tabelle, aus der die Zeilen abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f9193-114">[in] Pointer to the MAPI table from which rows are retrieved.</span></span> 
    
 <span data-ttu-id="f9193-115">_ptaga_</span><span class="sxs-lookup"><span data-stu-id="f9193-115">_ptaga_</span></span>
  
> <span data-ttu-id="f9193-116">in Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die ein Array von Property-Tags enthält, die Tabellenspalten anzeigen.</span><span class="sxs-lookup"><span data-stu-id="f9193-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags indicating table columns.</span></span> <span data-ttu-id="f9193-117">Diese Tags werden verwendet, um die einzelnen Spalten auszuwählen, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f9193-117">These tags are used to select the specific columns to be retrieved.</span></span> <span data-ttu-id="f9193-118">Wenn der _ptaga_ -Parameter NULL ist, ruft **HrQueryAllRows** den gesamten Spaltensatz der aktuellen Tabellenansicht ab, die im _ptable_ -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="f9193-118">If the  _ptaga_ parameter is NULL, **HrQueryAllRows** retrieves the entire column set of the current table view passed in the  _ptable_ parameter.</span></span> 
    
 <span data-ttu-id="f9193-119">_Pres_</span><span class="sxs-lookup"><span data-stu-id="f9193-119">_pres_</span></span>
  
> <span data-ttu-id="f9193-120">in Zeiger auf eine [SRestriction](srestriction.md) -Struktur, die Abruf Einschränkungen enthält.</span><span class="sxs-lookup"><span data-stu-id="f9193-120">[in] Pointer to an [SRestriction](srestriction.md) structure that contains retrieval restrictions.</span></span> <span data-ttu-id="f9193-121">Wenn der _Pres_ -Parameter NULL ist, macht **HrQueryAllRows** keine Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="f9193-121">If the  _pres_ parameter is NULL, **HrQueryAllRows** makes no restrictions.</span></span> 
    
 <span data-ttu-id="f9193-122">_PSOs_</span><span class="sxs-lookup"><span data-stu-id="f9193-122">_psos_</span></span>
  
> <span data-ttu-id="f9193-123">in Zeiger auf eine [SSortOrderSet](ssortorderset.md) -Struktur, die die Sortierreihenfolge der Spalten angibt, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f9193-123">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure identifying the sort order of the columns to be retrieved.</span></span> <span data-ttu-id="f9193-124">Wenn der __ Parameter "Parameters" den Wert NULL hat, wird die Standardsortierreihenfolge für die Tabelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="f9193-124">If the  _psos_ parameter is NULL, the default sort order for the table is used.</span></span> 
    
 <span data-ttu-id="f9193-125">_crowsMax_</span><span class="sxs-lookup"><span data-stu-id="f9193-125">_crowsMax_</span></span>
  
> <span data-ttu-id="f9193-126">in Maximale Anzahl von Zeilen, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f9193-126">[in] Maximum number of rows to be retrieved.</span></span> <span data-ttu-id="f9193-127">Wenn der Wert des _crowsMax_ -Parameters 0 (null) ist, wird kein Grenzwert für die Anzahl der abgerufenen Zeilen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f9193-127">If the value of the  _crowsMax_ parameter is zero, no limit on the number of rows retrieved is set.</span></span> 
    
 <span data-ttu-id="f9193-128">_pprows_</span><span class="sxs-lookup"><span data-stu-id="f9193-128">_pprows_</span></span>
  
> <span data-ttu-id="f9193-129">Out Zeiger auf einen Zeiger auf die zurückgegebene [SRowSet](srowset.md) -Struktur, die ein Array von Zeigern auf die abgerufenen Tabellenzeilen enthält.</span><span class="sxs-lookup"><span data-stu-id="f9193-129">[out] Pointer to a pointer to the returned [SRowSet](srowset.md) structure that contains an array of pointers to the retrieved table rows.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f9193-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f9193-130">Return value</span></span>

<span data-ttu-id="f9193-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="f9193-131">S_OK</span></span> 
  
> <span data-ttu-id="f9193-132">Der Aufruf hat die erwarteten Zeilen einer Tabelle abgerufen.</span><span class="sxs-lookup"><span data-stu-id="f9193-132">The call retrieved the expected rows of a table.</span></span> 
    
<span data-ttu-id="f9193-133">MAPI_E_TABLE_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="f9193-133">MAPI_E_TABLE_TOO_BIG</span></span> 
  
> <span data-ttu-id="f9193-134">Die Anzahl der Zeilen in der Tabelle ist größer als die Anzahl, die für den _crowsMax_ -Parameter übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="f9193-134">The number of rows in the table is larger than the number passed for the  _crowsMax_ parameter.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f9193-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9193-135">Remarks</span></span>

<span data-ttu-id="f9193-136">Eine Clientanwendung oder ein Dienstanbieter hat keine Kontrolle über die Anzahl der Zeilen, die **HrQueryAllRows** abruft, außer durch eine Einschränkung, auf die durch den _Pres_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="f9193-136">A client application or service provider has no control over the number of rows **HrQueryAllRows** attempts to retrieve, other than by imposing a restriction pointed to by the  _pres_ parameter.</span></span> <span data-ttu-id="f9193-137">Der Parameter _crowsMax_ schränkt den Abruf nicht auf eine bestimmte Anzahl von Tabellenzeilen ein, sondern definiert eine maximale Menge an Arbeitsspeicher, die für alle abgerufenen Zeilen verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f9193-137">The  _crowsMax_ parameter does not limit the retrieval to a certain number of table rows, but rather defines a maximum amount of memory available to hold all retrieved rows.</span></span> <span data-ttu-id="f9193-138">Der einzige Schutz vor massivem Speicherüberlauf ist das durch Festlegen von _crowsMax_bereitgestellte Notlösung-Feature.</span><span class="sxs-lookup"><span data-stu-id="f9193-138">The only protection against massive memory overflow is the stopgap feature provided by setting  _crowsMax_.</span></span> <span data-ttu-id="f9193-139">Der Fehler Return MAPI_E_TABLE_TOO_BIG gibt an, dass die Tabelle zu viele Zeilen enthält, die alle gleichzeitig im Arbeitsspeicher aufbewahrt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f9193-139">The error return MAPI_E_TABLE_TOO_BIG means the table contains too many rows to be held all at once in memory.</span></span> 
  
<span data-ttu-id="f9193-140">Tabellen, die normalerweise klein sind, wie beispielsweise eine Nachrichtenspeichertabelle oder eine Anbieter Tabelle, können mit **HrQueryAllRows**in der Regel sicher abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f9193-140">Tables that are typically small, such as a message store table or a provider table, usually can be safely retrieved with **HrQueryAllRows**.</span></span> <span data-ttu-id="f9193-141">Tabellen, die sehr umfangreich sind, wie beispielsweise eine Inhaltstabelle oder sogar eine Empfängertabelle, sollten mithilfe der [IMAPITable:: QueryRows](imapitable-queryrows.md) -Methode in Unterabschnitten durchlaufen werden.</span><span class="sxs-lookup"><span data-stu-id="f9193-141">Tables at risk of being very large, such as a contents table or even a recipients table, should be traversed in subsections using the [IMAPITable::QueryRows](imapitable-queryrows.md) method.</span></span> 
  
<span data-ttu-id="f9193-142">Wenn Tabelleneigenschaften nicht definiert sind, wenn **HrQueryAllRows** aufgerufen wird, werden Sie mit dem Eigenschaftentyp PT_NULL und dem EIGENSCHAFTENbezeichner PROP_ID_NULL</span><span class="sxs-lookup"><span data-stu-id="f9193-142">If any table properties are undefined when **HrQueryAllRows** is called, they are returned with property type PT_NULL and property identifier PROP_ID_NULL</span></span> 
  

