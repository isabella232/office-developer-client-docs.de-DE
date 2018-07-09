---
title: Fehlerbehandlung in MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99e2c485-af84-46f4-84b4-fca2117b5a21
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6f0ebd2112b65140a106a1376896f6de9c00da1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791636"
---
# <a name="error-handling-in-mapi"></a><span data-ttu-id="43454-103">Fehlerbehandlung in MAPI</span><span class="sxs-lookup"><span data-stu-id="43454-103">Error handling in MAPI</span></span>

<span data-ttu-id="43454-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="43454-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="43454-105">Erfolg, Warnung und Fehler-Werte werden unter Verwendung einer 32-Bit-Version bekannte dementsprechend Handle oder HRESULT zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="43454-105">Success, warning, and error values are returned using a 32-bit number known as a result handle, or HRESULT.</span></span> <span data-ttu-id="43454-106">Ein HRESULT ist nicht wirklich ein Handle auf einen anderen Wert. Es wird lediglich eine 32-Bit-Wert mit mehrere Felder in den Wert codiert.</span><span class="sxs-lookup"><span data-stu-id="43454-106">An HRESULT is really not a handle to anything; it is merely a 32-bit value with several fields encoded in the value.</span></span> <span data-ttu-id="43454-107">Ein NULL-Ergebnis zeigt Erfolg und ein ungleich NULL Ergebnis Fehler.</span><span class="sxs-lookup"><span data-stu-id="43454-107">A zero result indicates success and a nonzero result indicates failure.</span></span>
  
<span data-ttu-id="43454-108">MAPI auf 32-Bit-Plattformen funktioniert nur mit HRESULT-Werte.</span><span class="sxs-lookup"><span data-stu-id="43454-108">MAPI on 32-bit platforms works solely with HRESULT values.</span></span>
  
<span data-ttu-id="43454-109">Die folgende Abbildung zeigt das HRESULT-Format für 32-Bit-Plattformen.</span><span class="sxs-lookup"><span data-stu-id="43454-109">The following illustration shows the HRESULT format for 32-bit platforms.</span></span>
  
<span data-ttu-id="43454-110">**HRESULT-format**</span><span class="sxs-lookup"><span data-stu-id="43454-110">**HRESULT format**</span></span>
  
<span data-ttu-id="43454-111">![HRESULT-format] (media/amapi_49.gif "HRESULT-format")</span><span class="sxs-lookup"><span data-stu-id="43454-111">![HRESULT format](media/amapi_49.gif "HRESULT format")</span></span>
  
<span data-ttu-id="43454-112">Das hohe Bit in der HRESULT gibt an, ob der Rückgabewert Erfolg oder Fehler darstellt.</span><span class="sxs-lookup"><span data-stu-id="43454-112">The high order bit in the HRESULT indicates whether the return value represents success or failure.</span></span> <span data-ttu-id="43454-113">Wenn der Wert Erfolg gibt 0 (null) festgelegt, an.</span><span class="sxs-lookup"><span data-stu-id="43454-113">If set to zero, the value indicates success.</span></span> <span data-ttu-id="43454-114">Wenn auf 1 festgelegt, es einen Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="43454-114">If set to 1, it indicates failure.</span></span>
  
<span data-ttu-id="43454-115">Die R, C, N und R Bits sind in der HRESULT reserviert.</span><span class="sxs-lookup"><span data-stu-id="43454-115">The R, C, N, and r bits are reserved in the HRESULT.</span></span>
  
<span data-ttu-id="43454-116">Das Feld Facility in beiden Versionen gibt den Bereich der Verantwortung für den Fehler.</span><span class="sxs-lookup"><span data-stu-id="43454-116">The facility field in both versions indicates the area of responsibility for the error.</span></span> <span data-ttu-id="43454-117">Es gibt verschiedene Funktionen, aber die Mehrheit der MAPI-Fehler verwenden FACILITY_ITF Benutzeroberflächenfehler darstellen.</span><span class="sxs-lookup"><span data-stu-id="43454-117">There are several facilities, but the vast majority of MAPI errors use FACILITY_ITF to represent interface errors.</span></span> <span data-ttu-id="43454-118">Werden die am häufigsten verwendeten Funktionen, die derzeit verwendet werden: FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC und FACILITY_STORAGE.</span><span class="sxs-lookup"><span data-stu-id="43454-118">The most common facilities that are currently used are: FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC, and FACILITY_STORAGE.</span></span> <span data-ttu-id="43454-119">Wenn neue Funktionen erforderlich sind, weist Microsoft sie, da sie eindeutig sein müssen.</span><span class="sxs-lookup"><span data-stu-id="43454-119">If new facilities are necessary, Microsoft allocates them because they need to be unique.</span></span> <span data-ttu-id="43454-120">In der folgenden Tabelle werden die verschiedenen Facility Felder beschrieben.</span><span class="sxs-lookup"><span data-stu-id="43454-120">The following table describes the various facility fields.</span></span>
  
|<span data-ttu-id="43454-121">Einrichtung</span><span class="sxs-lookup"><span data-stu-id="43454-121">Facility</span></span>|<span data-ttu-id="43454-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="43454-122">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="43454-123">FACILITY_NULL</span><span class="sxs-lookup"><span data-stu-id="43454-123">FACILITY_NULL</span></span>  <br/> |<span data-ttu-id="43454-124">Für umfassend anwendbaren allgemeine Statuscodes wie S_OK oder E_OUTOF_MEMORY; der Wert ist NULL.</span><span class="sxs-lookup"><span data-stu-id="43454-124">For broadly applicable common status codes such as S_OK or E_OUTOF_MEMORY; the value is zero.</span></span>  <br/> |
|<span data-ttu-id="43454-125">FACILITY_ITF</span><span class="sxs-lookup"><span data-stu-id="43454-125">FACILITY_ITF</span></span>  <br/> |<span data-ttu-id="43454-126">Für die meisten Statuscodes von Schnittstellenmethoden zurückgegeben; der Wert wird von der Benutzeroberfläche definiert.</span><span class="sxs-lookup"><span data-stu-id="43454-126">For most status codes returned from interface methods; the value is defined by the interface.</span></span> <span data-ttu-id="43454-127">D. h., möglicherweise zwei HRESULT-Werte mit genau die gleiche 32-Bit-Wert zurückgegeben von zwei verschiedenen Schnittstellen verschiedene Bedeutungen haben.</span><span class="sxs-lookup"><span data-stu-id="43454-127">That is, two HRESULT values with exactly the same 32-bit value returned from two different interfaces might have different meanings.</span></span>  <br/> |
|<span data-ttu-id="43454-128">FACILITY_DISPATCH</span><span class="sxs-lookup"><span data-stu-id="43454-128">FACILITY_DISPATCH</span></span>  <br/> |<span data-ttu-id="43454-129">Für späte Bindung [IDispatch](http://msdn.microsoft.com/de-de/library/ms221608.aspx) -Schnittstelle Fehler.</span><span class="sxs-lookup"><span data-stu-id="43454-129">For late binding [IDispatch](http://msdn.microsoft.com/de-de/library/ms221608.aspx) interface errors.</span></span>  <br/> |
|<span data-ttu-id="43454-130">FACILITY_RPC</span><span class="sxs-lookup"><span data-stu-id="43454-130">FACILITY_RPC</span></span>  <br/> |<span data-ttu-id="43454-131">Für Statuscodes von Remoteprozeduraufrufe zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="43454-131">For status codes returned from remote procedure calls.</span></span>  <br/> |
|<span data-ttu-id="43454-132">FACILITY_STORAGE</span><span class="sxs-lookup"><span data-stu-id="43454-132">FACILITY_STORAGE</span></span>  <br/> |<span data-ttu-id="43454-133">Für Statuscodes [IStorage](http://msdn.microsoft.com/de-de/library/aa380015%28VS.85%29.aspx) oder [IStream](http://msdn.microsoft.com/de-de/library/aa380034%28VS.85%29.aspx) Aufrufe von Methoden für strukturierte Speicher zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="43454-133">For status codes returned from [IStorage](http://msdn.microsoft.com/de-de/library/aa380015%28VS.85%29.aspx) or [IStream](http://msdn.microsoft.com/de-de/library/aa380034%28VS.85%29.aspx) method calls relating to structured storage.</span></span> <span data-ttu-id="43454-134">Statuscodes Code (unteren 16 Bit) Werte im Bereich von Windows-Fehlercodes (d. h., kleiner als 256) haben dieselbe Bedeutung wie die entsprechende Windows-Fehler.</span><span class="sxs-lookup"><span data-stu-id="43454-134">Status codes with code (lower 16 bits) values in the range of Windows error codes (that is, less than 256) have the same meaning as the corresponding Windows errors.</span></span>  <br/> |
   
<span data-ttu-id="43454-135">Das Feld ist eine eindeutige Zahl, die zum Darstellen der Fehlermeldung oder einer Warnung zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="43454-135">The code field is a unique number that is assigned to represent the error or warning.</span></span>
  

