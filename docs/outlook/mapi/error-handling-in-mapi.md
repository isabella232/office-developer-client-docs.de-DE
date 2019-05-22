---
title: Fehlerbehandlung in MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99e2c485-af84-46f4-84b4-fca2117b5a21
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 98ee0856411cce3a3e9012185be6c30503de7779
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287280"
---
# <a name="error-handling-in-mapi"></a><span data-ttu-id="36b86-103">Fehlerbehandlung in MAPI</span><span class="sxs-lookup"><span data-stu-id="36b86-103">Error handling in MAPI</span></span>

<span data-ttu-id="36b86-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36b86-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36b86-105">Erfolgs-, Warnungs-und Fehlerwerte werden mithilfe einer 32-Bit-Zahl zurückgegeben, die als Ergebnis Handle oder HRESULT bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="36b86-105">Success, warning, and error values are returned using a 32-bit number known as a result handle, or HRESULT.</span></span> <span data-ttu-id="36b86-106">Ein HRESULT ist wirklich kein Handle für irgendetwas; Es handelt sich lediglich um einen 32-Bit-Wert mit mehreren Feldern, die im Wert codiert sind.</span><span class="sxs-lookup"><span data-stu-id="36b86-106">An HRESULT is really not a handle to anything; it is merely a 32-bit value with several fields encoded in the value.</span></span> <span data-ttu-id="36b86-107">Ein NULL-Ergebnis gibt den Erfolg an, und ein Ergebnis ungleich NULL gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="36b86-107">A zero result indicates success and a nonzero result indicates failure.</span></span>
  
<span data-ttu-id="36b86-108">MAPI auf 32-Bit-Plattformen funktioniert ausschließlich mit HRESULT-Werten.</span><span class="sxs-lookup"><span data-stu-id="36b86-108">MAPI on 32-bit platforms works solely with HRESULT values.</span></span>
  
<span data-ttu-id="36b86-109">In der folgenden Abbildung ist das HRESULT-Format für 32-Bit-Plattformen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="36b86-109">The following illustration shows the HRESULT format for 32-bit platforms.</span></span>
  
<span data-ttu-id="36b86-110">**HRESULT-Format**</span><span class="sxs-lookup"><span data-stu-id="36b86-110">**HRESULT format**</span></span>
  
<span data-ttu-id="36b86-111">![HRESULT-Format] (media/amapi_49.gif "HRESULT-Format")</span><span class="sxs-lookup"><span data-stu-id="36b86-111">![HRESULT format](media/amapi_49.gif "HRESULT format")</span></span>
  
<span data-ttu-id="36b86-112">Das hochwertige Bit im HRESULT gibt an, ob der Rückgabewert Erfolg oder Fehler darstellt.</span><span class="sxs-lookup"><span data-stu-id="36b86-112">The high order bit in the HRESULT indicates whether the return value represents success or failure.</span></span> <span data-ttu-id="36b86-113">Wenn dieser Wert auf NULL festgelegt ist, wird der Wert Success angegeben.</span><span class="sxs-lookup"><span data-stu-id="36b86-113">If set to zero, the value indicates success.</span></span> <span data-ttu-id="36b86-114">Wenn dieser Wert auf 1 festgelegt ist, wird ein Fehler angezeigt.</span><span class="sxs-lookup"><span data-stu-id="36b86-114">If set to 1, it indicates failure.</span></span>
  
<span data-ttu-id="36b86-115">Die Bits r, C, N und r sind im HRESULT reserviert.</span><span class="sxs-lookup"><span data-stu-id="36b86-115">The R, C, N, and r bits are reserved in the HRESULT.</span></span>
  
<span data-ttu-id="36b86-116">Das Feld "Facility" in beiden Versionen gibt den Verantwortungsbereich für den Fehler an.</span><span class="sxs-lookup"><span data-stu-id="36b86-116">The facility field in both versions indicates the area of responsibility for the error.</span></span> <span data-ttu-id="36b86-117">Es gibt mehrere Einrichtungen, aber die meisten MAPI-Fehler verwenden FACILITY_ITF, um Schnittstellenfehler darzustellen.</span><span class="sxs-lookup"><span data-stu-id="36b86-117">There are several facilities, but the vast majority of MAPI errors use FACILITY_ITF to represent interface errors.</span></span> <span data-ttu-id="36b86-118">Die derzeit gebräuchlichsten Einrichtungen sind: FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC und FACILITY_STORAGE.</span><span class="sxs-lookup"><span data-stu-id="36b86-118">The most common facilities that are currently used are: FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC, and FACILITY_STORAGE.</span></span> <span data-ttu-id="36b86-119">Wenn neue Einrichtungen erforderlich sind, werden Sie von Microsoft reserviert, da Sie eindeutig sein müssen.</span><span class="sxs-lookup"><span data-stu-id="36b86-119">If new facilities are necessary, Microsoft allocates them because they need to be unique.</span></span> <span data-ttu-id="36b86-120">In der folgenden Tabelle werden die verschiedenen Facility-Felder beschrieben.</span><span class="sxs-lookup"><span data-stu-id="36b86-120">The following table describes the various facility fields.</span></span>
  
|<span data-ttu-id="36b86-121">Facility</span><span class="sxs-lookup"><span data-stu-id="36b86-121">Facility</span></span>|<span data-ttu-id="36b86-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="36b86-122">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="36b86-123">FACILITY_NULL</span><span class="sxs-lookup"><span data-stu-id="36b86-123">FACILITY_NULL</span></span>  <br/> |<span data-ttu-id="36b86-124">Für allgemein gültige allgemeine Statuscodes wie S_OK oder E_OUTOF_MEMORY; der Wert ist NULL.</span><span class="sxs-lookup"><span data-stu-id="36b86-124">For broadly applicable common status codes such as S_OK or E_OUTOF_MEMORY; the value is zero.</span></span>  <br/> |
|<span data-ttu-id="36b86-125">FACILITY_ITF</span><span class="sxs-lookup"><span data-stu-id="36b86-125">FACILITY_ITF</span></span>  <br/> |<span data-ttu-id="36b86-126">Für die meisten Statuscodes, die von Schnittstellenmethoden zurückgegeben werden; der Wert wird durch die Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="36b86-126">For most status codes returned from interface methods; the value is defined by the interface.</span></span> <span data-ttu-id="36b86-127">Das heißt, zwei HRESULT-Werte mit genau dem gleichen 32-Bit-Wert, der von zwei unterschiedlichen Schnittstellen zurückgegeben wird, können unterschiedliche Bedeutungen haben.</span><span class="sxs-lookup"><span data-stu-id="36b86-127">That is, two HRESULT values with exactly the same 32-bit value returned from two different interfaces might have different meanings.</span></span>  <br/> |
|<span data-ttu-id="36b86-128">FACILITY_DISPATCH</span><span class="sxs-lookup"><span data-stu-id="36b86-128">FACILITY_DISPATCH</span></span>  <br/> |<span data-ttu-id="36b86-129">Für [IDispatch](https://msdn.microsoft.com/library/ms221608.aspx) -Schnittstellenfehler für späte Bindung.</span><span class="sxs-lookup"><span data-stu-id="36b86-129">For late binding [IDispatch](https://msdn.microsoft.com/library/ms221608.aspx) interface errors.</span></span>  <br/> |
|<span data-ttu-id="36b86-130">FACILITY_RPC</span><span class="sxs-lookup"><span data-stu-id="36b86-130">FACILITY_RPC</span></span>  <br/> |<span data-ttu-id="36b86-131">Für Statuscodes, die von Remoteprozeduraufrufen zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="36b86-131">For status codes returned from remote procedure calls.</span></span>  <br/> |
|<span data-ttu-id="36b86-132">FACILITY_STORAGE</span><span class="sxs-lookup"><span data-stu-id="36b86-132">FACILITY_STORAGE</span></span>  <br/> |<span data-ttu-id="36b86-133">Für Statuscodes, die von [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) -oder [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) -Methoden aufrufen im Zusammenhang mit dem strukturierten Speicher zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="36b86-133">For status codes returned from [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) or [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) method calls relating to structured storage.</span></span> <span data-ttu-id="36b86-134">Status Codes mit Code (untere 16 Bit) im Bereich der Windows-Fehlercodes (also weniger als 256) haben die gleiche Bedeutung wie die entsprechenden Windows-Fehler.</span><span class="sxs-lookup"><span data-stu-id="36b86-134">Status codes with code (lower 16 bits) values in the range of Windows error codes (that is, less than 256) have the same meaning as the corresponding Windows errors.</span></span>  <br/> |
   
<span data-ttu-id="36b86-135">Das Feld Code ist eine eindeutige Nummer, die dem Fehler oder der Warnung zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="36b86-135">The code field is a unique number that is assigned to represent the error or warning.</span></span>
  

