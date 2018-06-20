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
ms.openlocfilehash: 5c62e5919c6e605aa4b60f48072996ed1fd4c355
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791940"
---
# <a name="hrqueryallrows"></a><span data-ttu-id="7447c-103">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="7447c-103">HrQueryAllRows</span></span>

  
  
<span data-ttu-id="7447c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7447c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7447c-105">Ruft alle Zeilen einer Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="7447c-105">Retrieves all rows of a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7447c-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="7447c-106">Header file:</span></span>  <br/> |<span data-ttu-id="7447c-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="7447c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="7447c-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="7447c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7447c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7447c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7447c-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="7447c-110">Called by:</span></span>  <br/> |<span data-ttu-id="7447c-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="7447c-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="7447c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7447c-112">Parameters</span></span>

 <span data-ttu-id="7447c-113">_ptable_</span><span class="sxs-lookup"><span data-stu-id="7447c-113">_ptable_</span></span>
  
> <span data-ttu-id="7447c-114">[in] Zeiger auf die MAPI-Tabelle aus der Zeilen abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7447c-114">[in] Pointer to the MAPI table from which rows are retrieved.</span></span> 
    
 <span data-ttu-id="7447c-115">_ptaga_</span><span class="sxs-lookup"><span data-stu-id="7447c-115">_ptaga_</span></span>
  
> <span data-ttu-id="7447c-116">[in] Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die ein Array der-Eigenschaft enthält tags Tabellenspalten angibt.</span><span class="sxs-lookup"><span data-stu-id="7447c-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags indicating table columns.</span></span> <span data-ttu-id="7447c-117">Diese Tags dienen zum Auswählen der spezifischen Spalten abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7447c-117">These tags are used to select the specific columns to be retrieved.</span></span> <span data-ttu-id="7447c-118">Wenn der Parameter _Ptaga_ NULL ist, ruft **HrQueryAllRows** den gesamte Spaltensatz von der aktuellen Tabellenansicht im _Ptable_ -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="7447c-118">If the  _ptaga_ parameter is NULL, **HrQueryAllRows** retrieves the entire column set of the current table view passed in the  _ptable_ parameter.</span></span> 
    
 <span data-ttu-id="7447c-119">_Pres_</span><span class="sxs-lookup"><span data-stu-id="7447c-119">_pres_</span></span>
  
> <span data-ttu-id="7447c-120">[in] Zeiger auf eine [SRestriction](srestriction.md) -Struktur, die Retrieval Einschränkungen enthält.</span><span class="sxs-lookup"><span data-stu-id="7447c-120">[in] Pointer to an [SRestriction](srestriction.md) structure that contains retrieval restrictions.</span></span> <span data-ttu-id="7447c-121">Wenn der Parameter _Pres_ NULL ist, wird **HrQueryAllRows** ohne Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="7447c-121">If the  _pres_ parameter is NULL, **HrQueryAllRows** makes no restrictions.</span></span> 
    
 <span data-ttu-id="7447c-122">_PSOs_</span><span class="sxs-lookup"><span data-stu-id="7447c-122">_psos_</span></span>
  
> <span data-ttu-id="7447c-123">[in] Zeiger auf eine [SSortOrderSet](ssortorderset.md) -Struktur, identifiziert die Sortierreihenfolge der Spalten abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7447c-123">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure identifying the sort order of the columns to be retrieved.</span></span> <span data-ttu-id="7447c-124">Wenn der Parameter _Psos_ NULL ist, wird die standardmäßige Sortierreihenfolge für die Tabelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="7447c-124">If the  _psos_ parameter is NULL, the default sort order for the table is used.</span></span> 
    
 <span data-ttu-id="7447c-125">_crowsMax_</span><span class="sxs-lookup"><span data-stu-id="7447c-125">_crowsMax_</span></span>
  
> <span data-ttu-id="7447c-126">[in] Maximale Anzahl von Zeilen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7447c-126">[in] Maximum number of rows to be retrieved.</span></span> <span data-ttu-id="7447c-127">Wenn der Wert des Parameters _CrowsMax_ gleich NULL ist, wird keine Begrenzung für die Anzahl der abgerufenen Zeilen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7447c-127">If the value of the  _crowsMax_ parameter is zero, no limit on the number of rows retrieved is set.</span></span> 
    
 <span data-ttu-id="7447c-128">_ppRows_</span><span class="sxs-lookup"><span data-stu-id="7447c-128">_pprows_</span></span>
  
> <span data-ttu-id="7447c-129">[out] Zeiger auf einen Zeiger auf das zurückgegebene [SRowSet](srowset.md) -Struktur, die ein Array von Zeigern für die abgerufenen Zeilen enthält.</span><span class="sxs-lookup"><span data-stu-id="7447c-129">[out] Pointer to a pointer to the returned [SRowSet](srowset.md) structure that contains an array of pointers to the retrieved table rows.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7447c-130">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="7447c-130">Return value</span></span>

<span data-ttu-id="7447c-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="7447c-131">S_OK</span></span> 
  
> <span data-ttu-id="7447c-132">Der Anruf abgerufen, die erwarteten Zeilen einer Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7447c-132">The call retrieved the expected rows of a table.</span></span> 
    
<span data-ttu-id="7447c-133">KEINE</span><span class="sxs-lookup"><span data-stu-id="7447c-133">MAPI_E_TABLE_TOO_BIG</span></span> 
  
> <span data-ttu-id="7447c-134">Die Anzahl der Zeilen in der Tabelle ist größer als die Anzahl für den _CrowsMax_ -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="7447c-134">The number of rows in the table is larger than the number passed for the  _crowsMax_ parameter.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7447c-135">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7447c-135">Remarks</span></span>

<span data-ttu-id="7447c-136">Eine Clientanwendung oder Dienstanbieter hat keine Kontrolle über die Anzahl der Zeilen, die **HrQueryAllRows** versucht, abrufen, außer durch die Festlegung einer Einschränkung mit durch den Parameter _Pres_ gezeigt.</span><span class="sxs-lookup"><span data-stu-id="7447c-136">A client application or service provider has no control over the number of rows **HrQueryAllRows** attempts to retrieve, other than by imposing a restriction pointed to by the  _pres_ parameter.</span></span> <span data-ttu-id="7447c-137">Der Parameter _CrowsMax_ schränkt nicht das Abrufen auf eine bestimmte Anzahl von Zeilen der Tabelle, aber vielmehr definiert eine maximale Größe des Arbeitsspeichers zur Verfügung, die alle abgerufene Zeilen enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="7447c-137">The  _crowsMax_ parameter does not limit the retrieval to a certain number of table rows, but rather defines a maximum amount of memory available to hold all retrieved rows.</span></span> <span data-ttu-id="7447c-138">Der einzige Schutz gegen Speicher Überlauf ist die stetig Funktion _CrowsMax_festlegen.</span><span class="sxs-lookup"><span data-stu-id="7447c-138">The only protection against massive memory overflow is the stopgap feature provided by setting  _crowsMax_.</span></span> <span data-ttu-id="7447c-139">Die Rendite der Fehler, die bedeutet, die Tabelle dass enthält zu viele Zeilen, die alle gleichzeitig im Speicher aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="7447c-139">The error return MAPI_E_TABLE_TOO_BIG means the table contains too many rows to be held all at once in memory.</span></span> 
  
<span data-ttu-id="7447c-140">Tabellen, die in der Regel klein, wie eine Nachricht Store Tabelle oder einer Tabelle Anbieter können in der Regel sicher mit **HrQueryAllRows**abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7447c-140">Tables that are typically small, such as a message store table or a provider table, usually can be safely retrieved with **HrQueryAllRows**.</span></span> <span data-ttu-id="7447c-141">Tabellen Risiko, wird sehr groß sein, wie etwa eine Inhalt oder sogar eine Tabelle Empfänger, sollte in [der QueryRows](imapitable-queryrows.md) mit Unterabschnitten durchlaufen werden.</span><span class="sxs-lookup"><span data-stu-id="7447c-141">Tables at risk of being very large, such as a contents table or even a recipients table, should be traversed in subsections using the [IMAPITable::QueryRows](imapitable-queryrows.md) method.</span></span> 
  
<span data-ttu-id="7447c-142">Wenn alle Tabelleneigenschaften **HrQueryAllRows** aufgerufen wird nicht definiert sind, werden diese mit Eigenschaftentyp PT_NULL und Eigenschaftenbezeichner PROP_ID_NULL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7447c-142">If any table properties are undefined when **HrQueryAllRows** is called, they are returned with property type PT_NULL and property identifier PROP_ID_NULL</span></span> 
  

