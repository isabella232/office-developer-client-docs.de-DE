---
title: MAPI-Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 63d7360a-e3a3-4365-9d46-50df1c715bde
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3e16a373ec35696f6d1a8ccc52263a1cf8570cfc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572326"
---
# <a name="mapi-string-properties"></a><span data-ttu-id="384cf-103">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="384cf-103">MAPI String Properties</span></span>

  
  
<span data-ttu-id="384cf-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="384cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="384cf-105">MAPI bietet drei verschiedene Eigenschaftstypen um Zeichenfolgeneigenschaften beschrieben:</span><span class="sxs-lookup"><span data-stu-id="384cf-105">MAPI provides three different property types to describe string properties:</span></span>
  
<span data-ttu-id="384cf-106">PT_TSTRING</span><span class="sxs-lookup"><span data-stu-id="384cf-106">PT_TSTRING</span></span>
  
<span data-ttu-id="384cf-107">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="384cf-107">PT_STRING8</span></span>
  
<span data-ttu-id="384cf-108">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="384cf-108">PT_UNICODE</span></span>
  
<span data-ttu-id="384cf-109">Zeichenfolgeneigenschaften werden am häufigsten als PT_TSTRING definiert.</span><span class="sxs-lookup"><span data-stu-id="384cf-109">String properties are most commonly defined as PT_TSTRING.</span></span> <span data-ttu-id="384cf-110">Der Eigenschaftentyp PT_TSTRING kompiliert bedingt auf eine der anderen Zeichenfolge Eigenschaftentypen, je nachdem, je nachdem, ob das Unicode-Makro definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="384cf-110">The PT_TSTRING property type conditionally compiles to one of the other string property types, depending depending on whether the UNICODE macro has been defined.</span></span> <span data-ttu-id="384cf-111">PT_STRING8 beschreibt 8-Bit-Null endende Zeichenfolgen in ANSI-Format. PT_UNICODE beschreibt Doppelbyte-Null endende Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="384cf-111">PT_STRING8 describes 8-bit null-terminated character strings in the ANSI format; PT_UNICODE describes double-byte null-terminated character strings.</span></span> 
  
<span data-ttu-id="384cf-112">Zur Unterstützung von Unicode-Zeichenfolgen können entweder ein Client oder einem-Dienstanbieter oder sowohl Client und Anbieter auswählen.</span><span class="sxs-lookup"><span data-stu-id="384cf-112">Either a client or a service provider, or both client and provider can choose to support Unicode character strings.</span></span> <span data-ttu-id="384cf-113">Es ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="384cf-113">It is not required.</span></span> <span data-ttu-id="384cf-114">Ein Client, der nur für Zeichenfolgen PT_STRING8 unterstützt, kann mit einem Anbieter ausgeführt werden, der Unicode und umgekehrt unterstützt.</span><span class="sxs-lookup"><span data-stu-id="384cf-114">A client that supports only PT_STRING8 strings can operate with a provider that supports Unicode and vice versa.</span></span> <span data-ttu-id="384cf-115">Um diese Interoperabilität zu aktivieren, übergeben Sie Clients und Dienstanbieter ein Kennzeichen, die Option MAPI_UNICODE, um anzugeben, dass Unicode in Methoden unterstützt wird, die den Austausch von Zeichenfolgen betreffen.</span><span class="sxs-lookup"><span data-stu-id="384cf-115">To enable this interoperability, clients and service providers pass a flag, the MAPI_UNICODE flag, to indicate that Unicode is supported in methods that involve the exchange of character strings.</span></span> 
  
<span data-ttu-id="384cf-116">Nehmen wir beispielsweise bei einem Client unterstützt Unicode und den Anzeigenamen eines Ordners abrufen muss.</span><span class="sxs-lookup"><span data-stu-id="384cf-116">For example, suppose a client supports Unicode and needs to retrieve the display name of a folder.</span></span> <span data-ttu-id="384cf-117">Alle Eigenschaften für den Client PT_TSTRING werden zur Eingabe von PT_UNICODE kompiliert.</span><span class="sxs-lookup"><span data-stu-id="384cf-117">All of the client's PT_TSTRING properties are compiled to type PT_UNICODE.</span></span> <span data-ttu-id="384cf-118">Wenn der Client den Ordner [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode zum Abrufen von dessen **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft aufruft, übergibt sie die Option MAPI_UNICODE um anzufordern, dass die Zeichenfolge des Anzeigenamens in das Unicode-Format zurückgegeben werden soll .</span><span class="sxs-lookup"><span data-stu-id="384cf-118">When the client calls the folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, it passes the MAPI_UNICODE flag to request that the display name string be returned in the Unicode format.</span></span> 
  
<span data-ttu-id="384cf-119">Clients und -Dienstanbieter müssen berücksichtigen, die Angabe eines Zeichensatzes in einem Methodenaufruf wird nur eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="384cf-119">Clients and service providers need to be aware that specifying a character set in a method call is only a request.</span></span> <span data-ttu-id="384cf-120">Unterstützung einer oder beide Zeichensätze ist die Implementierung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="384cf-120">Supporting one or both character sets is up to the implementer of the object.</span></span> <span data-ttu-id="384cf-121">Dienstanbieter werden jedoch empfohlen, beide Zeichensätze, da es ermöglicht es ihnen, mehr Verbreitung als Anbieter zu erzielen, die nur einen Satz zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="384cf-121">However, service providers are encouraged to support both character sets because it allows them to achieve more widespread distribution than providers that support only one set.</span></span> 
  
<span data-ttu-id="384cf-122">Zeichenfolgeneigenschaften anwachsen können sehr groß sein, da binäre Eigenschaften können – Geben Sie PT_BINARY Eigenschaften, die die-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="384cf-122">String properties can grow to be quite large as can binary properties — properties that use the property type PT_BINARY.</span></span> <span data-ttu-id="384cf-123">Zum Vereinfachen der Arbeit mit großen Eigenschaften kann MAPI-Dienstanbieter Festlegen dieser Eigenschaften zum Erzwingen von größenbeschränkungen für Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="384cf-123">To ease working with large properties, MAPI allows service providers setting these properties to enforce size limits.</span></span> <span data-ttu-id="384cf-124">Diese Grenzwerte können variieren je nach:</span><span class="sxs-lookup"><span data-stu-id="384cf-124">These limits can vary, depending on:</span></span>
  
- <span data-ttu-id="384cf-125">Gibt an, ob die Eigenschaften werden gelesenen oder geschriebenen.</span><span class="sxs-lookup"><span data-stu-id="384cf-125">Whether the properties are being read or written.</span></span>
    
- <span data-ttu-id="384cf-126">Wie der Dienstanbieter die **IMAPIProp** Methoden implementiert.</span><span class="sxs-lookup"><span data-stu-id="384cf-126">How the service provider implements the **IMAPIProp** methods.</span></span> 
    
- <span data-ttu-id="384cf-127">Common Language Runtime Aspekte wie Speicherkapazität.</span><span class="sxs-lookup"><span data-stu-id="384cf-127">Runtime considerations, such as memory constraints.</span></span>
    
- <span data-ttu-id="384cf-128">Zeichensatz Übersetzungsfehler.</span><span class="sxs-lookup"><span data-stu-id="384cf-128">Character set translation issues.</span></span> 
    
<span data-ttu-id="384cf-129">Größenbeschränkungen für Nachrichten auch auf Zeichenfolge platziert werden können und binäre Eigenschaften, wenn sie in der Spalte verwendet werden Festlegen einer Tabelle, da es in einigen Fällen nicht möglich, alle große den Wert einer Eigenschaft sichtbar zu machen ist.</span><span class="sxs-lookup"><span data-stu-id="384cf-129">Size limits can also be placed on string and binary properties when they are used in the column set of a table because it is sometimes impossible to make all of a large property's value visible.</span></span> <span data-ttu-id="384cf-130">Viele Dienstanbieter Abschneiden großen Zeichenfolge oder binäre Eigenschaften, die in den Tabellen auf 255 Byte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="384cf-130">Many service providers truncate large string or binary properties that are used in tables to 255 bytes.</span></span> 
  
<span data-ttu-id="384cf-131">Wenn ein Client ein Objekt **GetProps** oder **SetProps** -Methode zum Arbeiten mit einer großen Zeichenfolge oder eine binäre Eigenschaft ruft und der Aufruf, aufgrund der Eigenschaftsgröße fehlschlägt, gibt die Methode den Fehlerwert MAPI_E_NOT_ENOUGH_MEMORY zurück.</span><span class="sxs-lookup"><span data-stu-id="384cf-131">When a client calls an object's **GetProps** or **SetProps** method to work with a large string or binary property and the call fails because of the property size, the method returns the error value MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="384cf-132">Wenn es **GetProps** , die für eine bestimmte Eigenschaft ein Fehler aufgetreten ist ist, kann der Client wiederhergestellt werden durch Aufrufen von [IMAPIProp::OpenProperty](imapiprop-openproperty.md) und **IStream** für den Zugriff durch Angeben von IID_IStream als Schnittstellenbezeichner anfordern.</span><span class="sxs-lookup"><span data-stu-id="384cf-132">If it is **GetProps** that is failing for a specific property, the client can recover by calling [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and requesting the **IStream** for access by specifying IID_IStream as the interface identifier.</span></span> <span data-ttu-id="384cf-133">**OpenProperty**verwenden, kann der Client abrufen eine große Eigenschaft über die eine Schnittstelle wie **IStream** , der besser für das Arbeiten mit großen Eigenschaften geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="384cf-133">Using **OpenProperty**, the client can retrieve a large property using an interface such as **IStream** that is better suited for working with large properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="384cf-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="384cf-134">See also</span></span>



[<span data-ttu-id="384cf-135">Übersicht über die MAPI-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="384cf-135">MAPI Property Overview</span></span>](mapi-property-overview.md)

