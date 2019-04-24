---
title: Erstellen von Eintrags Bezeichnern
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bc2a9116-948e-4da3-96b8-26d73bcd63c4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8d48c2584fa5b7e862102e401ea8165821607f77
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335091"
---
# <a name="constructing-entry-identifiers"></a><span data-ttu-id="8ded6-103">Erstellen von Eintrags Bezeichnern</span><span class="sxs-lookup"><span data-stu-id="8ded6-103">Constructing Entry Identifiers</span></span>

  
  
<span data-ttu-id="8ded6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8ded6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8ded6-105">Eintragsbezeichner werden mit der [Eintrags](entryid.md) -ID-Struktur erstellt.</span><span class="sxs-lookup"><span data-stu-id="8ded6-105">Entry identifiers are constructed with the [ENTRYID](entryid.md) structure.</span></span> <span data-ttu-id="8ded6-106">Die **Eintrags** -ID-Struktur besteht aus einem Flag, das die Attribute des Eintrags Bezeichners und des tatsächlichen Eintrags Bezeichners beschreibt.</span><span class="sxs-lookup"><span data-stu-id="8ded6-106">The **ENTRYID** structure is composed of a flag that describes the attributes of the entry identifier and the actual entry identifier.</span></span> 
  
## <a name="entryid-structure"></a><span data-ttu-id="8ded6-107">EINTRAGs-Struktur</span><span class="sxs-lookup"><span data-stu-id="8ded6-107">ENTRYID Structure</span></span>

<span data-ttu-id="8ded6-108">Die **Eintrags** -Struktur ist wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="8ded6-108">The **ENTRYID** structure is defined as follows:</span></span> 
  
```cpp
typedef struct
{
    BYTE        abFlags[4];
    BYTE        ab[MAPI_DIM];
}  ENTRYID, FAR *LPENTRYID;
 
```

<span data-ttu-id="8ded6-109">MAPI_DIM ist eine Konstante, die in der Headerdatei MapiDefs. h definiert ist.</span><span class="sxs-lookup"><span data-stu-id="8ded6-109">MAPI_DIM is a constant that is defined in the MapiDefs.h header file.</span></span> 
  
<span data-ttu-id="8ded6-110">Das erste Byte des 4-Byte- **abFlags** -Elements beschreibt den Typ und die Verwendung des Eintrags Bezeichners und kann die folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="8ded6-110">The first byte of the 4-byte **abFlags** member describes the type and use of the entry identifier and can have the following values:</span></span> 
  
- <span data-ttu-id="8ded6-111">MAPI_NOTRECI – gibt an, dass die Eintrags-ID nicht als Empfänger für eine Nachricht verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="8ded6-111">MAPI_NOTRECI — Indicates the entry identifier cannot be used as a recipient on a message.</span></span>
    
- <span data-ttu-id="8ded6-112">MAPI_NOTRESERVED – gibt an, dass andere Benutzer nicht auf die Eintrags-ID zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="8ded6-112">MAPI_NOTRESERVED — Indicates that other users cannot access the entry identifier.</span></span>
    
- <span data-ttu-id="8ded6-113">MAPI_NOW – gibt an, dass die Eintrags-ID nicht zu anderen Zeiten verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="8ded6-113">MAPI_NOW — Indicates that the entry identifier cannot be used at other times.</span></span>
    
- <span data-ttu-id="8ded6-114">MAPI_SHORTTERM – gibt an, dass die Eintrags-ID kurzfristig ist.</span><span class="sxs-lookup"><span data-stu-id="8ded6-114">MAPI_SHORTTERM — Indicates that the entry identifier is short-term.</span></span> <span data-ttu-id="8ded6-115">Alle anderen Werte in diesem Byte müssen festgelegt werden, es sei denn, andere Verwendungen der Eintrags-ID sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="8ded6-115">All other values in this byte must be set unless other uses of the entry identifier are allowed.</span></span>
    
- <span data-ttu-id="8ded6-116">MAPI_THISSESSION – gibt an, dass die Eintrags-ID nicht in anderen Sitzungen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="8ded6-116">MAPI_THISSESSION — Indicates that the entry identifier cannot be used on other sessions.</span></span>
    
- <span data-ttu-id="8ded6-117">MAPI_NOTRESERVED – gibt an, dass die Eintrags-ID von anderen Dienstanbietern für andere Objekte verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="8ded6-117">MAPI_NOTRESERVED — Indicates that the entry identifier can be used by other service providers for other objects.</span></span>
    
<span data-ttu-id="8ded6-118">Das **ab** -Element von Eintrags-IDs, das von Adressbuch-und Nachrichtenspeicher Anbietern erstellt wird, besteht aus zwei Teilen: eine 16-Byte- [MAPIUID](mapiuid.md) -Struktur, die den Dienstanbieter identifiziert, und ein Stück zur Identifizierung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="8ded6-118">The **ab** member of entry identifiers that is created by address book and message store providers is composed of two pieces: a 16-byte [MAPIUID](mapiuid.md) structure that identifies the service provider, and a piece to identify the object.</span></span> <span data-ttu-id="8ded6-119">**MAPIUID** ist eine Struktur, die einen global eindeutigen Bezeichner oder eine GUID enthält.</span><span class="sxs-lookup"><span data-stu-id="8ded6-119">**MAPIUID** is a structure that contains a globally unique identifier, or GUID.</span></span> <span data-ttu-id="8ded6-120">Eine GUID ist ein Bytereihenfolge-unabhängiger Bezeichner, der mithilfe des Microsoft Visual Studio\*Create GUID\*\*-Tools erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="8ded6-120">A GUID is a byte-order-independent identifier that can be created by using the Microsoft Visual Studio*Create GUID*\* tool.</span></span> 
  
<span data-ttu-id="8ded6-121">Ein Dienstanbieter registriert seine **MAPIUID** -Struktur während des Anmeldevorgangs bei einem Aufruf der [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) -Methode mit MAPI.</span><span class="sxs-lookup"><span data-stu-id="8ded6-121">A service provider registers its **MAPIUID** structure with MAPI during the logon process in a call to the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method.</span></span> <span data-ttu-id="8ded6-122">Wenn ein Client eine **OpenEntry** -Methode für den Zugriff auf ein Objekt aufruft, bestimmt MAPI mithilfe der **MAPIUID** -Struktur, welcher Dienstanbieter diesen Zugriff bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="8ded6-122">When a client calls an **OpenEntry** method to access an object, MAPI uses the **MAPIUID** structure to determine which service provider can provide that access.</span></span> <span data-ttu-id="8ded6-123">Dienstanbieter sollten dieselbe **MAPIUID** -Struktur für alle Versionen Ihrer dll verwenden.</span><span class="sxs-lookup"><span data-stu-id="8ded6-123">Service providers should use the same **MAPIUID** structure for all versions of their DLL.</span></span> <span data-ttu-id="8ded6-124">Auf diese Weise können Clients mit der neueren Version auf Nachrichten Antworten, die mit der älteren Version gesendet und gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="8ded6-124">This enables clients with the newer version to respond to messages sent and saved with the older version.</span></span> 
  
<span data-ttu-id="8ded6-125">Der Rest des **ab** -Elements nach der 16-Byte- **MAPIUID** enthält Dienstanbieter spezifische Binärdaten zum Identifizieren bestimmter Objekte.</span><span class="sxs-lookup"><span data-stu-id="8ded6-125">The rest of the **ab** member after the 16-byte **MAPIUID** contains service-provider-specific binary data for identifying particular objects.</span></span> <span data-ttu-id="8ded6-126">Für diesen Teil der Eintrags-ID gibt es keine feste Größe.</span><span class="sxs-lookup"><span data-stu-id="8ded6-126">There is no fixed size for this portion of the entry identifier.</span></span> <span data-ttu-id="8ded6-127">Es kann eine beliebige Größe innerhalb der Grund sein.</span><span class="sxs-lookup"><span data-stu-id="8ded6-127">It can be any size, within reason.</span></span> <span data-ttu-id="8ded6-128">Ein Dienstanbieter enthält in der Regel die folgenden Informationen in diesem Teil seiner Eintrags-IDs:</span><span class="sxs-lookup"><span data-stu-id="8ded6-128">A service provider typically includes the following information in this part of its entry identifiers:</span></span> 
  
- <span data-ttu-id="8ded6-129">Versionsinformationen – da es für einen Dienstanbieter üblich ist, das Format seiner Eintrags-IDs von Version zu Version zu ändern, ermöglicht das Speichern von Versionsinformationen, schnell festzustellen, wie jeder Eintragsbezeichner entschlüsselt werden kann.</span><span class="sxs-lookup"><span data-stu-id="8ded6-129">Version information — Because it is common for a service provider to change the format of its entry identifiers from version to version, storing version information makes it possible to quickly determine how to decipher any entry identifier.</span></span>
    
- <span data-ttu-id="8ded6-130">Standortinformationen – Speicherortinformationen sind Daten, die einem Dienstanbieter einen Indikator für das Auffinden des durch die Eintrags-ID dargestellten Objekts geben.</span><span class="sxs-lookup"><span data-stu-id="8ded6-130">Location information — Location information is data that gives a service provider an indicator of how to locate the object represented by the entry identifier.</span></span> <span data-ttu-id="8ded6-131">Ein Dienstanbieter kann beispielsweise den Datenträger Offset für die letzte Position in einer Datendatei speichern, die das Objekt gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="8ded6-131">For example, a service provider can store the disk offset for the last place in a data file that the object was stored.</span></span> <span data-ttu-id="8ded6-132">Da diese Art von Informationen sich im Lauf der Zeit ändern kann, sollten Dienstanbieter mehrere Möglichkeiten bieten, Objekte in ihren Eintrags Bezeichnern zu suchen.</span><span class="sxs-lookup"><span data-stu-id="8ded6-132">Because this type of information can change over time, service providers should provide multiple ways for locating objects in their entry identifiers.</span></span>
    
<span data-ttu-id="8ded6-133">Obwohl Dienstanbieter Ihre Eintrags-IDs wieder verwenden können, sollten Sie diese Vorgehensweise vermeiden.</span><span class="sxs-lookup"><span data-stu-id="8ded6-133">Although service providers can recycle their entry identifiers, they should avoid this practice.</span></span> <span data-ttu-id="8ded6-134">Wenn eine Eintrags-ID wieder verwendet werden muss, sollten Dienstanbieter den Zeitraum zwischen der anfänglichen Verwendung und der Wiederverwendung so lange wie möglich verstreichen lassen.</span><span class="sxs-lookup"><span data-stu-id="8ded6-134">If it is necessary to reuse an entry identifier, service providers should make the time period that elapses between the initial use and the reuse as long as possible.</span></span> <span data-ttu-id="8ded6-135">Außerdem sollte die Eintrags-ID einem anderen Objekt desselben Typs erneut zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="8ded6-135">Also, the entry identifier should be reassigned to another object of the same type.</span></span> <span data-ttu-id="8ded6-136">Das heißt, eine bestimmte Eintrags-ID sollte nicht zuerst einer Nachricht und dann mit einem Ordner zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="8ded6-136">That is, a particular entry identifier should not be associated first with a message and then with a folder.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8ded6-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ded6-137">See also</span></span>



[<span data-ttu-id="8ded6-138">MAPI-Eintrags-IDs</span><span class="sxs-lookup"><span data-stu-id="8ded6-138">MAPI Entry Identifiers</span></span>](mapi-entry-identifiers.md)

