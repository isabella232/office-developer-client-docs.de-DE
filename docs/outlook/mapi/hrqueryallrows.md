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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0f09304f21180d9ebc2a1e1dcc54ebadd3622804
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422894"
---
# <a name="hrqueryallrows"></a><span data-ttu-id="c7502-103">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="c7502-103">HrQueryAllRows</span></span>

  
  
<span data-ttu-id="c7502-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c7502-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c7502-105">Ruft alle Zeilen einer Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="c7502-105">Retrieves all rows of a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c7502-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="c7502-106">Header file:</span></span>  <br/> |<span data-ttu-id="c7502-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="c7502-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="c7502-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="c7502-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c7502-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c7502-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c7502-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="c7502-110">Called by:</span></span>  <br/> |<span data-ttu-id="c7502-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="c7502-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="c7502-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7502-112">Parameters</span></span>

 <span data-ttu-id="c7502-113">_ptable_</span><span class="sxs-lookup"><span data-stu-id="c7502-113">_ptable_</span></span>
  
> <span data-ttu-id="c7502-114">[in] Zeiger auf die MAPI-Tabelle, aus der Zeilen abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c7502-114">[in] Pointer to the MAPI table from which rows are retrieved.</span></span> 
    
 <span data-ttu-id="c7502-115">_ptaga_</span><span class="sxs-lookup"><span data-stu-id="c7502-115">_ptaga_</span></span>
  
> <span data-ttu-id="c7502-116">[in] Zeiger auf eine [SPropTagArray-Struktur,](sproptagarray.md) die ein Array von Eigenschaftstags enthält, die Tabellenspalten angeben.</span><span class="sxs-lookup"><span data-stu-id="c7502-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags indicating table columns.</span></span> <span data-ttu-id="c7502-117">Diese Tags werden verwendet, um die spezifischen Spalten auszuwählen, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c7502-117">These tags are used to select the specific columns to be retrieved.</span></span> <span data-ttu-id="c7502-118">Wenn der  _ptaga-Parameter_ NULL ist, **ruft HrQueryAllRows** den gesamten Spaltensatz der aktuellen Tabellenansicht ab, die im  _ptable-Parameter übergeben_ wird.</span><span class="sxs-lookup"><span data-stu-id="c7502-118">If the  _ptaga_ parameter is NULL, **HrQueryAllRows** retrieves the entire column set of the current table view passed in the  _ptable_ parameter.</span></span> 
    
 <span data-ttu-id="c7502-119">_pres_</span><span class="sxs-lookup"><span data-stu-id="c7502-119">_pres_</span></span>
  
> <span data-ttu-id="c7502-120">[in] Zeiger auf eine [SRestriction-Struktur,](srestriction.md) die Abrufeinschränkungen enthält.</span><span class="sxs-lookup"><span data-stu-id="c7502-120">[in] Pointer to an [SRestriction](srestriction.md) structure that contains retrieval restrictions.</span></span> <span data-ttu-id="c7502-121">Wenn der  _parameter pres_ NULL ist, **macht HrQueryAllRows** keine Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="c7502-121">If the  _pres_ parameter is NULL, **HrQueryAllRows** makes no restrictions.</span></span> 
    
 <span data-ttu-id="c7502-122">_psos_</span><span class="sxs-lookup"><span data-stu-id="c7502-122">_psos_</span></span>
  
> <span data-ttu-id="c7502-123">[in] Zeiger auf eine [SSortOrderSet-Struktur,](ssortorderset.md) die die Sortierreihenfolge der abzurufenden Spalten identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c7502-123">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure identifying the sort order of the columns to be retrieved.</span></span> <span data-ttu-id="c7502-124">Wenn der  _psos-Parameter_ NULL ist, wird die Standardsortierungsreihenfolge für die Tabelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="c7502-124">If the  _psos_ parameter is NULL, the default sort order for the table is used.</span></span> 
    
 <span data-ttu-id="c7502-125">_krähenMax_</span><span class="sxs-lookup"><span data-stu-id="c7502-125">_crowsMax_</span></span>
  
> <span data-ttu-id="c7502-126">[in] Maximale Anzahl der abzurufende Zeilen.</span><span class="sxs-lookup"><span data-stu-id="c7502-126">[in] Maximum number of rows to be retrieved.</span></span> <span data-ttu-id="c7502-127">Wenn der Wert des  _Parameters "krähenMax"_ null ist, wird kein Grenzwert für die Anzahl der abgerufenen Zeilen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c7502-127">If the value of the  _crowsMax_ parameter is zero, no limit on the number of rows retrieved is set.</span></span> 
    
 <span data-ttu-id="c7502-128">_pprows_</span><span class="sxs-lookup"><span data-stu-id="c7502-128">_pprows_</span></span>
  
> <span data-ttu-id="c7502-129">[out] Zeiger auf einen Zeiger auf die zurückgegebene [SRowSet-Struktur,](srowset.md) die ein Array von Zeigern auf die abgerufenen Tabellenzeilen enthält.</span><span class="sxs-lookup"><span data-stu-id="c7502-129">[out] Pointer to a pointer to the returned [SRowSet](srowset.md) structure that contains an array of pointers to the retrieved table rows.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c7502-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c7502-130">Return value</span></span>

<span data-ttu-id="c7502-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="c7502-131">S_OK</span></span> 
  
> <span data-ttu-id="c7502-132">Der Aufruf hat die erwarteten Zeilen einer Tabelle abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c7502-132">The call retrieved the expected rows of a table.</span></span> 
    
<span data-ttu-id="c7502-133">MAPI_E_TABLE_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="c7502-133">MAPI_E_TABLE_TOO_BIG</span></span> 
  
> <span data-ttu-id="c7502-134">Die Anzahl der Zeilen in der Tabelle ist größer als die für den  _Parameter "krähenMax" übergebene_ Anzahl.</span><span class="sxs-lookup"><span data-stu-id="c7502-134">The number of rows in the table is larger than the number passed for the  _crowsMax_ parameter.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c7502-135">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c7502-135">Remarks</span></span>

<span data-ttu-id="c7502-136">Eine Clientanwendung oder ein Dienstanbieter hat keine Kontrolle über die Anzahl der Zeilen, die **HrQueryAllRows** abzurufen versucht, es sei denn, es wird eine Einschränkung festgelegt, auf die der  _parameter pres_ verweist.</span><span class="sxs-lookup"><span data-stu-id="c7502-136">A client application or service provider has no control over the number of rows **HrQueryAllRows** attempts to retrieve, other than by imposing a restriction pointed to by the  _pres_ parameter.</span></span> <span data-ttu-id="c7502-137">Der  _parameter "krähesMax"_ begrenzt den Abruf nicht auf eine bestimmte Anzahl von Tabellenzeilen, sondern definiert eine maximale Menge an Arbeitsspeicher, die für alle abgerufenen Zeilen verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="c7502-137">The  _crowsMax_ parameter does not limit the retrieval to a certain number of table rows, but rather defines a maximum amount of memory available to hold all retrieved rows.</span></span> <span data-ttu-id="c7502-138">Der einzige Schutz vor massivem Speicherüberlauf ist das Stopgap-Feature, das durch Festlegen von _"krähenMax" bereitgestellt wird._</span><span class="sxs-lookup"><span data-stu-id="c7502-138">The only protection against massive memory overflow is the stopgap feature provided by setting  _crowsMax_.</span></span> <span data-ttu-id="c7502-139">Der Fehlerrücklauf MAPI_E_TABLE_TOO_BIG bedeutet, dass die Tabelle zu viele Zeilen enthält, um alle gleichzeitig im Arbeitsspeicher gespeichert zu werden.</span><span class="sxs-lookup"><span data-stu-id="c7502-139">The error return MAPI_E_TABLE_TOO_BIG means the table contains too many rows to be held all at once in memory.</span></span> 
  
<span data-ttu-id="c7502-140">Tabellen, die in der Regel klein sind, z. B. eine Nachrichtenspeichertabelle oder eine Anbietertabelle, können in der Regel mit **HrQueryAllRows** sicher abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c7502-140">Tables that are typically small, such as a message store table or a provider table, usually can be safely retrieved with **HrQueryAllRows**.</span></span> <span data-ttu-id="c7502-141">Tabellen, bei der das Risiko besteht, dass sie sehr groß sind, z. B. eine Inhaltstabelle oder sogar eine Empfängertabelle, sollten mithilfe der [IMAPITable::QueryRows-Methode](imapitable-queryrows.md) in Unterabschnitten durchlaufen werden.</span><span class="sxs-lookup"><span data-stu-id="c7502-141">Tables at risk of being very large, such as a contents table or even a recipients table, should be traversed in subsections using the [IMAPITable::QueryRows](imapitable-queryrows.md) method.</span></span> 
  
<span data-ttu-id="c7502-142">Wenn Tabelleneigenschaften nicht definiert sind, wenn **HrQueryAllRows** aufgerufen wird, werden sie mit dem Eigenschaftentyp PT_NULL und eigenschaftsbezeichner PROP_ID_NULL</span><span class="sxs-lookup"><span data-stu-id="c7502-142">If any table properties are undefined when **HrQueryAllRows** is called, they are returned with property type PT_NULL and property identifier PROP_ID_NULL</span></span> 
  

