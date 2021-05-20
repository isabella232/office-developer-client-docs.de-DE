---
title: Erstellen von Eintragsbezeichnern
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bc2a9116-948e-4da3-96b8-26d73bcd63c4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8d48c2584fa5b7e862102e401ea8165821607f77
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427948"
---
# <a name="constructing-entry-identifiers"></a><span data-ttu-id="9039f-103">Erstellen von Eintragsbezeichnern</span><span class="sxs-lookup"><span data-stu-id="9039f-103">Constructing Entry Identifiers</span></span>

  
  
<span data-ttu-id="9039f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9039f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9039f-105">Eintragsbezeichner werden mit der [ENTRYID-Struktur](entryid.md) erstellt.</span><span class="sxs-lookup"><span data-stu-id="9039f-105">Entry identifiers are constructed with the [ENTRYID](entryid.md) structure.</span></span> <span data-ttu-id="9039f-106">Die **ENTRYID-Struktur** besteht aus einem Flag, das die Attribute des Eintragsbezeichners und des tatsächlichen Eintragsbezeichners beschreibt.</span><span class="sxs-lookup"><span data-stu-id="9039f-106">The **ENTRYID** structure is composed of a flag that describes the attributes of the entry identifier and the actual entry identifier.</span></span> 
  
## <a name="entryid-structure"></a><span data-ttu-id="9039f-107">ENTRYID-Struktur</span><span class="sxs-lookup"><span data-stu-id="9039f-107">ENTRYID Structure</span></span>

<span data-ttu-id="9039f-108">Die **ENTRYID-Struktur** ist wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="9039f-108">The **ENTRYID** structure is defined as follows:</span></span> 
  
```cpp
typedef struct
{
    BYTE        abFlags[4];
    BYTE        ab[MAPI_DIM];
}  ENTRYID, FAR *LPENTRYID;
 
```

<span data-ttu-id="9039f-109">MAPI_DIM ist eine Konstante, die in der MapiDefs.h-Headerdatei definiert ist.</span><span class="sxs-lookup"><span data-stu-id="9039f-109">MAPI_DIM is a constant that is defined in the MapiDefs.h header file.</span></span> 
  
<span data-ttu-id="9039f-110">Das erste Byte des 4-Byte-AbFlags-Mitglieds beschreibt den Typ und die Verwendung der Eintrags-ID und kann die folgenden Werte haben: </span><span class="sxs-lookup"><span data-stu-id="9039f-110">The first byte of the 4-byte **abFlags** member describes the type and use of the entry identifier and can have the following values:</span></span> 
  
- <span data-ttu-id="9039f-111">MAPI_NOTRECI – Gibt an, dass der Eintragsbezeichner nicht als Empfänger für eine Nachricht verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="9039f-111">MAPI_NOTRECI — Indicates the entry identifier cannot be used as a recipient on a message.</span></span>
    
- <span data-ttu-id="9039f-112">MAPI_NOTRESERVED – Gibt an, dass andere Benutzer nicht auf die Eintrags-ID zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="9039f-112">MAPI_NOTRESERVED — Indicates that other users cannot access the entry identifier.</span></span>
    
- <span data-ttu-id="9039f-113">MAPI_NOW – Gibt an, dass der Eintragsbezeichner zu anderen Zeiten nicht verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="9039f-113">MAPI_NOW — Indicates that the entry identifier cannot be used at other times.</span></span>
    
- <span data-ttu-id="9039f-114">MAPI_SHORTTERM – Gibt an, dass der Eintragsbezeichner kurzfristig ist.</span><span class="sxs-lookup"><span data-stu-id="9039f-114">MAPI_SHORTTERM — Indicates that the entry identifier is short-term.</span></span> <span data-ttu-id="9039f-115">Alle anderen Werte in diesem Byte müssen festgelegt werden, es sei denn, andere Verwendungen der Eintrags-ID sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="9039f-115">All other values in this byte must be set unless other uses of the entry identifier are allowed.</span></span>
    
- <span data-ttu-id="9039f-116">MAPI_THISSESSION – Gibt an, dass der Eintragsbezeichner nicht für andere Sitzungen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="9039f-116">MAPI_THISSESSION — Indicates that the entry identifier cannot be used on other sessions.</span></span>
    
- <span data-ttu-id="9039f-117">MAPI_NOTRESERVED – Gibt an, dass der Eintragsbezeichner von anderen Dienstanbietern für andere Objekte verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="9039f-117">MAPI_NOTRESERVED — Indicates that the entry identifier can be used by other service providers for other objects.</span></span>
    
<span data-ttu-id="9039f-118">Das **ab-Element** von Eintragsbezeichnern, die von Adressbuch- und Nachrichtenspeicheranbietern erstellt werden, besteht aus zwei Teilen: einer [MAPIUID-Struktur](mapiuid.md) mit 16 Byte, die den Dienstanbieter identifiziert, und einem Element zum Identifizieren des Objekts.</span><span class="sxs-lookup"><span data-stu-id="9039f-118">The **ab** member of entry identifiers that is created by address book and message store providers is composed of two pieces: a 16-byte [MAPIUID](mapiuid.md) structure that identifies the service provider, and a piece to identify the object.</span></span> <span data-ttu-id="9039f-119">**MAPIUID** ist eine Struktur, die einen global eindeutigen Bezeichner oder eine GUID enthält.</span><span class="sxs-lookup"><span data-stu-id="9039f-119">**MAPIUID** is a structure that contains a globally unique identifier, or GUID.</span></span> <span data-ttu-id="9039f-120">Eine GUID ist ein bytereihenfolgeunabhängiger Bezeichner, der mithilfe des Tools Microsoft Visual Studio *GUID*\* erstellen erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="9039f-120">A GUID is a byte-order-independent identifier that can be created by using the Microsoft Visual Studio *Create GUID*\* tool.</span></span> 
  
<span data-ttu-id="9039f-121">Ein Dienstanbieter registriert seine **MAPIUID-Struktur** bei MAPI während des Anmeldevorgangs in einem Aufruf der [IMAPISupport::SetProviderUID-Methode.](imapisupport-setprovideruid.md)</span><span class="sxs-lookup"><span data-stu-id="9039f-121">A service provider registers its **MAPIUID** structure with MAPI during the logon process in a call to the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method.</span></span> <span data-ttu-id="9039f-122">Wenn ein Client eine **OpenEntry-Methode** aufruft, um auf ein Objekt zu zugreifen, verwendet MAPI die **MAPIUID-Struktur,** um zu bestimmen, welcher Dienstanbieter diesen Zugriff bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="9039f-122">When a client calls an **OpenEntry** method to access an object, MAPI uses the **MAPIUID** structure to determine which service provider can provide that access.</span></span> <span data-ttu-id="9039f-123">Dienstanbieter sollten dieselbe **MAPIUID-Struktur** für alle Versionen ihrer DLL verwenden.</span><span class="sxs-lookup"><span data-stu-id="9039f-123">Service providers should use the same **MAPIUID** structure for all versions of their DLL.</span></span> <span data-ttu-id="9039f-124">Dadurch können Clients mit der neueren Version auf Nachrichten reagieren, die mit der älteren Version gesendet und gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="9039f-124">This enables clients with the newer version to respond to messages sent and saved with the older version.</span></span> 
  
<span data-ttu-id="9039f-125">Der Rest des **ab-Mitglieds** nach dem 16-Byte-MAPIUID enthält dienstanbieterspezifische Binärdaten zum Identifizieren bestimmter Objekte. </span><span class="sxs-lookup"><span data-stu-id="9039f-125">The rest of the **ab** member after the 16-byte **MAPIUID** contains service-provider-specific binary data for identifying particular objects.</span></span> <span data-ttu-id="9039f-126">Für diesen Teil der Eintrags-ID gibt es keine feste Größe.</span><span class="sxs-lookup"><span data-stu-id="9039f-126">There is no fixed size for this portion of the entry identifier.</span></span> <span data-ttu-id="9039f-127">Es kann eine beliebige Größe sein, innerhalb der Grund.</span><span class="sxs-lookup"><span data-stu-id="9039f-127">It can be any size, within reason.</span></span> <span data-ttu-id="9039f-128">Ein Dienstanbieter enthält in der Regel die folgenden Informationen in diesem Teil seiner Eintragsbezeichner:</span><span class="sxs-lookup"><span data-stu-id="9039f-128">A service provider typically includes the following information in this part of its entry identifiers:</span></span> 
  
- <span data-ttu-id="9039f-129">Versionsinformationen – Da es für einen Dienstanbieter üblich ist, das Format seiner Eintragsbezeichner von Version zu Version zu ändern, können Durch das Speichern von Versionsinformationen schnell bestimmt werden, wie jeder Eintragsbezeichner entschlüsselt werden kann.</span><span class="sxs-lookup"><span data-stu-id="9039f-129">Version information — Because it is common for a service provider to change the format of its entry identifiers from version to version, storing version information makes it possible to quickly determine how to decipher any entry identifier.</span></span>
    
- <span data-ttu-id="9039f-130">Standortinformationen – Standortinformationen sind Daten, die einem Dienstanbieter einen Indikator dafür geben, wie das durch den Eintragsbezeichner dargestellte Objekt gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="9039f-130">Location information — Location information is data that gives a service provider an indicator of how to locate the object represented by the entry identifier.</span></span> <span data-ttu-id="9039f-131">Beispielsweise kann ein Dienstanbieter den Datenträgerversatz für den letzten Ort in einer Datendatei speichern, in der das Objekt gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="9039f-131">For example, a service provider can store the disk offset for the last place in a data file that the object was stored.</span></span> <span data-ttu-id="9039f-132">Da sich diese Art von Informationen im Laufe der Zeit ändern kann, sollten Dienstanbieter mehrere Möglichkeiten zum Auffinden von Objekten in ihren Eintragsbezeichnern bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="9039f-132">Because this type of information can change over time, service providers should provide multiple ways for locating objects in their entry identifiers.</span></span>
    
<span data-ttu-id="9039f-133">Obwohl Dienstanbieter ihre Eintrags-ID wiederverwenden können, sollten sie diese Vorgehensweise vermeiden.</span><span class="sxs-lookup"><span data-stu-id="9039f-133">Although service providers can recycle their entry identifiers, they should avoid this practice.</span></span> <span data-ttu-id="9039f-134">Wenn eine Eintrags-ID wiederverwendet werden muss, sollten Dienstanbieter den Zeitraum zwischen der anfänglichen Verwendung und der Wiederverwendung so lange wie möglich angeben.</span><span class="sxs-lookup"><span data-stu-id="9039f-134">If it is necessary to reuse an entry identifier, service providers should make the time period that elapses between the initial use and the reuse as long as possible.</span></span> <span data-ttu-id="9039f-135">Außerdem sollte der Eintragsbezeichner einem anderen Objekt desselben Typs neu zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="9039f-135">Also, the entry identifier should be reassigned to another object of the same type.</span></span> <span data-ttu-id="9039f-136">Das heißt, eine bestimmte Eintrags-ID sollte nicht zuerst einer Nachricht und dann einem Ordner zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="9039f-136">That is, a particular entry identifier should not be associated first with a message and then with a folder.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9039f-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9039f-137">See also</span></span>



[<span data-ttu-id="9039f-138">MAPI-Eintragsbezeichner</span><span class="sxs-lookup"><span data-stu-id="9039f-138">MAPI Entry Identifiers</span></span>](mapi-entry-identifiers.md)

