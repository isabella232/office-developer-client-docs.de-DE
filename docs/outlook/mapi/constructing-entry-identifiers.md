---
title: Konstruieren von Eintragsbezeichnern
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bc2a9116-948e-4da3-96b8-26d73bcd63c4
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1d38c0ac7ddbd24123dd51d7315644f3ad786d15
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791430"
---
# <a name="constructing-entry-identifiers"></a><span data-ttu-id="18b35-103">Konstruieren von Eintragsbezeichnern</span><span class="sxs-lookup"><span data-stu-id="18b35-103">Constructing Entry Identifiers</span></span>

  
  
<span data-ttu-id="18b35-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="18b35-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="18b35-105">Eintragsbezeichner werden mit der [ENTRYID](entryid.md) -Struktur erstellt.</span><span class="sxs-lookup"><span data-stu-id="18b35-105">Entry identifiers are constructed with the [ENTRYID](entryid.md) structure.</span></span> <span data-ttu-id="18b35-106">Die **ENTRYID** -Struktur besteht ein Flag, das die Attribute des Eintrags-ID und die tatsächlichen Eintrags-ID beschreibt.</span><span class="sxs-lookup"><span data-stu-id="18b35-106">The **ENTRYID** structure is composed of a flag that describes the attributes of the entry identifier and the actual entry identifier.</span></span> 
  
## <a name="entryid-structure"></a><span data-ttu-id="18b35-107">ENTRYID-Struktur</span><span class="sxs-lookup"><span data-stu-id="18b35-107">ENTRYID Structure</span></span>

<span data-ttu-id="18b35-108">Die **ENTRYID** -Struktur ist wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="18b35-108">The **ENTRYID** structure is defined as follows:</span></span> 
  
```cpp
typedef struct
{
    BYTE        abFlags[4];
    BYTE        ab[MAPI_DIM];
}  ENTRYID, FAR *LPENTRYID;
 
```

<span data-ttu-id="18b35-109">MAPI_DIM ist eine Konstante, die in der Headerdatei MapiDefs.h definiert ist.</span><span class="sxs-lookup"><span data-stu-id="18b35-109">MAPI_DIM is a constant that is defined in the MapiDefs.h header file.</span></span> 
  
<span data-ttu-id="18b35-110">Das erste Byte des Elements 4-Byte- **AbFlags** beschreibt die Art und Verwendung der Eintrags-ID und kann die folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="18b35-110">The first byte of the 4-byte **abFlags** member describes the type and use of the entry identifier and can have the following values:</span></span> 
  
- <span data-ttu-id="18b35-111">MAPI_NOTRECI – Gibt an, dass die Eintrags-ID kann nicht als Empfänger einer Nachricht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="18b35-111">MAPI_NOTRECI — Indicates the entry identifier cannot be used as a recipient on a message.</span></span>
    
- <span data-ttu-id="18b35-112">MAPI_NOTRESERVED – Gibt an, dass andere Benutzer die Eintrags-ID zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="18b35-112">MAPI_NOTRESERVED — Indicates that other users cannot access the entry identifier.</span></span>
    
- <span data-ttu-id="18b35-113">MAPI_NOW – Gibt an, dass die Eintrags-ID in anderen Fällen nicht verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="18b35-113">MAPI_NOW — Indicates that the entry identifier cannot be used at other times.</span></span>
    
- <span data-ttu-id="18b35-114">MAPI_SHORTTERM – Gibt an, dass die Eintrags-ID kurzfristige ist.</span><span class="sxs-lookup"><span data-stu-id="18b35-114">MAPI_SHORTTERM — Indicates that the entry identifier is short-term.</span></span> <span data-ttu-id="18b35-115">Alle anderen Werte in dieses Byte müssen festgelegt werden, es sei denn, weitere Verwendungsmöglichkeiten des Bezeichners Eintrag zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="18b35-115">All other values in this byte must be set unless other uses of the entry identifier are allowed.</span></span>
    
- <span data-ttu-id="18b35-116">MAPI_THISSESSION – Gibt an, dass die Eintrags-ID für andere-Sitzungen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="18b35-116">MAPI_THISSESSION — Indicates that the entry identifier cannot be used on other sessions.</span></span>
    
- <span data-ttu-id="18b35-117">MAPI_NOTRESERVED – Gibt an, dass die Eintrags-ID für andere Objekte von anderen Dienstanbietern verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="18b35-117">MAPI_NOTRESERVED — Indicates that the entry identifier can be used by other service providers for other objects.</span></span>
    
<span data-ttu-id="18b35-118">Das **Ab** Element Eintragsbezeichner, die Zeichenfolgeneigenschaften Address Book und Nachricht erstellt wird besteht aus zwei Teilen: eine 16-Byte- [MAPIUID](mapiuid.md) -Struktur, die der Dienstanbieter und ein Inhaltselement, um das Objekt zu identifizieren identifiziert.</span><span class="sxs-lookup"><span data-stu-id="18b35-118">The **ab** member of entry identifiers that is created by address book and message store providers is composed of two pieces: a 16-byte [MAPIUID](mapiuid.md) structure that identifies the service provider, and a piece to identify the object.</span></span> <span data-ttu-id="18b35-119">**MAPIUID** ist eine Struktur, die einen global eindeutigen Bezeichner oder eine GUID enthält.</span><span class="sxs-lookup"><span data-stu-id="18b35-119">**MAPIUID** is a structure that contains a globally unique identifier, or GUID.</span></span> <span data-ttu-id="18b35-120">Eine GUID ist eine Byte-Reihenfolge-unabhängigen-ID, die erstellt werden können, mit der Microsoft Visual Studio-*GUID erstellen*\* Tool.</span><span class="sxs-lookup"><span data-stu-id="18b35-120">A GUID is a byte-order-independent identifier that can be created by using the Microsoft Visual Studio*Create GUID*\* tool.</span></span> 
  
<span data-ttu-id="18b35-121">Ein Dienstanbieter registriert seine **MAPIUID** Struktur mit MAPI während des Anmeldevorgangs in einem Aufruf der [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="18b35-121">A service provider registers its **MAPIUID** structure with MAPI during the logon process in a call to the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method.</span></span> <span data-ttu-id="18b35-122">Wenn ein Client eine Methode **OpenEntry** Zugriff auf ein Objekt aufruft, verwendet MAPI die **MAPIUID** -Struktur, um zu bestimmen, welcher Dienst Anbieter, dass der Zugriff bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="18b35-122">When a client calls an **OpenEntry** method to access an object, MAPI uses the **MAPIUID** structure to determine which service provider can provide that access.</span></span> <span data-ttu-id="18b35-123">Dienstanbieter sollten die gleiche **MAPIUID** -Struktur für alle Versionen von ihrer DLL verwenden.</span><span class="sxs-lookup"><span data-stu-id="18b35-123">Service providers should use the same **MAPIUID** structure for all versions of their DLL.</span></span> <span data-ttu-id="18b35-124">Auf diese Weise können Clients durch die neuere Version Antworten auf Nachrichten gesendet und mit der älteren Version gespeichert.</span><span class="sxs-lookup"><span data-stu-id="18b35-124">This enables clients with the newer version to respond to messages sent and saved with the older version.</span></span> 
  
<span data-ttu-id="18b35-125">Der Rest des Elements **Ab** , nachdem die 16-Byte- **MAPIUID** Service-anbieterspezifische Binärdaten zum Identifizieren von bestimmter Objekten enthält.</span><span class="sxs-lookup"><span data-stu-id="18b35-125">The rest of the **ab** member after the 16-byte **MAPIUID** contains service-provider-specific binary data for identifying particular objects.</span></span> <span data-ttu-id="18b35-126">Es ist keine fester Größe für dieses Teils des Eintrags-ID ein.</span><span class="sxs-lookup"><span data-stu-id="18b35-126">There is no fixed size for this portion of the entry identifier.</span></span> <span data-ttu-id="18b35-127">Beliebiger Größe innerhalb Grund kann sein.</span><span class="sxs-lookup"><span data-stu-id="18b35-127">It can be any size, within reason.</span></span> <span data-ttu-id="18b35-128">Ein Dienstanbieter umfasst in der Regel die folgende Informationen in diesem Teil seiner Eintragsbezeichner:</span><span class="sxs-lookup"><span data-stu-id="18b35-128">A service provider typically includes the following information in this part of its entry identifiers:</span></span> 
  
- <span data-ttu-id="18b35-129">Versionsinformationen –, da es für einen Dienstanbieter, ändern Sie das Format der seine Eintragsbezeichner von Version zu Version üblich ist, Speichern von Informationen zur Version ermöglicht schnell ermitteln, wie Sie eine beliebige Eintrags-ID zu entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="18b35-129">Version information — Because it is common for a service provider to change the format of its entry identifiers from version to version, storing version information makes it possible to quickly determine how to decipher any entry identifier.</span></span>
    
- <span data-ttu-id="18b35-130">Standortinformationen – Standortinformationen sind Daten, die einem Dienstanbieter ein Symbol zum Objekt dargestellt durch die Eintrags-ID gefunden werden können.</span><span class="sxs-lookup"><span data-stu-id="18b35-130">Location information — Location information is data that gives a service provider an indicator of how to locate the object represented by the entry identifier.</span></span> <span data-ttu-id="18b35-131">Beispielsweise kann ein Dienstanbieter bewahren Sie die Diskette offset für die letzte Stelle in einer Datendatei, dass das Objekt gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="18b35-131">For example, a service provider can store the disk offset for the last place in a data file that the object was stored.</span></span> <span data-ttu-id="18b35-132">Da diese Art von Informationen mit der Zeit ändern kann, sollten Dienstanbieter für die Suche nach Objekten in ihren Eintragsbezeichner verschiedene Arten bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="18b35-132">Because this type of information can change over time, service providers should provide multiple ways for locating objects in their entry identifiers.</span></span>
    
<span data-ttu-id="18b35-133">Zwar Dienstanbieter ihre Eintragsbezeichner wiederverwendet werden können, sollten sie dieses Verfahren vermeiden.</span><span class="sxs-lookup"><span data-stu-id="18b35-133">Although service providers can recycle their entry identifiers, they should avoid this practice.</span></span> <span data-ttu-id="18b35-134">Wenn es eine Eintrags-ID wiederverwenden erforderlich ist, sollten-Dienstanbieter den Zeitraum an, die verstreicht, zwischen dem zum ersten Mal verwenden und die Wiederverwendung so lange wie möglich.</span><span class="sxs-lookup"><span data-stu-id="18b35-134">If it is necessary to reuse an entry identifier, service providers should make the time period that elapses between the initial use and the reuse as long as possible.</span></span> <span data-ttu-id="18b35-135">Darüber hinaus sollten die Eintrags-ID in ein anderes Objekt des gleichen Typs neu zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="18b35-135">Also, the entry identifier should be reassigned to another object of the same type.</span></span> <span data-ttu-id="18b35-136">D. h., sollte ein bestimmten Eintrag Bezeichner nicht zuerst mit einer Meldung, und klicken Sie dann mit einem Ordner verknüpft sein.</span><span class="sxs-lookup"><span data-stu-id="18b35-136">That is, a particular entry identifier should not be associated first with a message and then with a folder.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="18b35-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18b35-137">See also</span></span>



[<span data-ttu-id="18b35-138">MAPI-Eintragsbezeichner</span><span class="sxs-lookup"><span data-stu-id="18b35-138">MAPI Entry Identifiers</span></span>](mapi-entry-identifiers.md)

