---
title: EIGENSCHAFTEN DER MAPI-Zeichenfolge
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 63d7360a-e3a3-4365-9d46-50df1c715bde
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9720b649eadecc73d84d98926674a1786796ba70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431393"
---
# <a name="mapi-string-properties"></a><span data-ttu-id="fc7a3-103">EIGENSCHAFTEN DER MAPI-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="fc7a3-103">MAPI String Properties</span></span>

  
  
<span data-ttu-id="fc7a3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc7a3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc7a3-105">MAPI bietet drei verschiedene Eigenschaftstypen zum Beschreiben von Zeichenfolgeneigenschaften:</span><span class="sxs-lookup"><span data-stu-id="fc7a3-105">MAPI provides three different property types to describe string properties:</span></span>
  
<span data-ttu-id="fc7a3-106">PT_TSTRING</span><span class="sxs-lookup"><span data-stu-id="fc7a3-106">PT_TSTRING</span></span>
  
<span data-ttu-id="fc7a3-107">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="fc7a3-107">PT_STRING8</span></span>
  
<span data-ttu-id="fc7a3-108">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fc7a3-108">PT_UNICODE</span></span>
  
<span data-ttu-id="fc7a3-109">Zeichenfolgeneigenschaften werden am häufigsten als PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="fc7a3-109">String properties are most commonly defined as PT_TSTRING.</span></span> <span data-ttu-id="fc7a3-110">Der PT_TSTRING-Eigenschaftstyp wird abhängig davon, ob das UNICODE-Makro definiert wurde, bedingt in einen der anderen Zeichenfolgeneigenschaftstypen kompiliert.</span><span class="sxs-lookup"><span data-stu-id="fc7a3-110">The PT_TSTRING property type conditionally compiles to one of the other string property types, depending depending on whether the UNICODE macro has been defined.</span></span> <span data-ttu-id="fc7a3-111">PT_STRING8 beschreibt 8-Bit-Zeichenzeichenfolgen mit Null-Termin im ANSI-Format. PT_UNICODE beschreibt Zeichenfolgen mit Nullenendzeichen mit Doppel-Byte.</span><span class="sxs-lookup"><span data-stu-id="fc7a3-111">PT_STRING8 describes 8-bit null-terminated character strings in the ANSI format; PT_UNICODE describes double-byte null-terminated character strings.</span></span> 
  
<span data-ttu-id="fc7a3-112">Entweder ein Client oder ein Dienstanbieter, oder Client und Anbieter können Unicode-Zeichenzeichenfolgen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="fc7a3-112">Either a client or a service provider, or both client and provider can choose to support Unicode character strings.</span></span> <span data-ttu-id="fc7a3-113">Sie ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fc7a3-113">It is not required.</span></span> <span data-ttu-id="fc7a3-114">Ein Client, der nur PT_STRING8 Zeichenfolgen unterstützt, kann mit einem Anbieter arbeiten, der Unicode unterstützt und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="fc7a3-114">A client that supports only PT_STRING8 strings can operate with a provider that supports Unicode and vice versa.</span></span> <span data-ttu-id="fc7a3-115">Um diese Interoperabilität zu aktivieren, übergeben Clients und Dienstanbieter ein Flag, das MAPI_UNICODE-Flag, um anzugeben, dass Unicode in Methoden unterstützt wird, die den Austausch von Zeichenzeichenfolgen beinhalten.</span><span class="sxs-lookup"><span data-stu-id="fc7a3-115">To enable this interoperability, clients and service providers pass a flag, the MAPI_UNICODE flag, to indicate that Unicode is supported in methods that involve the exchange of character strings.</span></span> 
  
<span data-ttu-id="fc7a3-116">Angenommen, ein Client unterstützt Unicode und muss den Anzeigenamen eines Ordners abrufen.</span><span class="sxs-lookup"><span data-stu-id="fc7a3-116">For example, suppose a client supports Unicode and needs to retrieve the display name of a folder.</span></span> <span data-ttu-id="fc7a3-117">Alle Eigenschaften des Clients PT_TSTRING zum Eingeben von PT_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="fc7a3-117">All of the client's PT_TSTRING properties are compiled to type PT_UNICODE.</span></span> <span data-ttu-id="fc7a3-118">Wenn der Client die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des Ordners aufruft, um seine **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft abzurufen, übergibt er das MAPI_UNICODE-Flag, um an die Anforderung zu senden, dass die Anzeigenamenzeichenfolge im Unicode-Format zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fc7a3-118">When the client calls the folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, it passes the MAPI_UNICODE flag to request that the display name string be returned in the Unicode format.</span></span> 
  
<span data-ttu-id="fc7a3-119">Clients und Dienstanbieter müssen beachten, dass das Angeben eines Zeichensatzs in einem Methodenaufruf nur eine Anforderung ist.</span><span class="sxs-lookup"><span data-stu-id="fc7a3-119">Clients and service providers need to be aware that specifying a character set in a method call is only a request.</span></span> <span data-ttu-id="fc7a3-120">Die Unterstützung eines oder beider Zeichensätze liegt beim Implementier des Objekts.</span><span class="sxs-lookup"><span data-stu-id="fc7a3-120">Supporting one or both character sets is up to the implementer of the object.</span></span> <span data-ttu-id="fc7a3-121">Dienstanbieter werden jedoch ermutigt, beide Zeichensätze zu unterstützen, da sie dadurch eine breitere Verteilung erzielen können als Anbieter, die nur einen Satz unterstützen.</span><span class="sxs-lookup"><span data-stu-id="fc7a3-121">However, service providers are encouraged to support both character sets because it allows them to achieve more widespread distribution than providers that support only one set.</span></span> 
  
<span data-ttu-id="fc7a3-122">Zeichenfolgeneigenschaften können relativ groß werden, ebenso wie binäre Eigenschaften – Eigenschaften, die den Eigenschaftentyp PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="fc7a3-122">String properties can grow to be quite large as can binary properties — properties that use the property type PT_BINARY.</span></span> <span data-ttu-id="fc7a3-123">Um das Arbeiten mit großen Eigenschaften zu erleichtern, ermöglicht MAPI Dienstanbietern das Festlegen dieser Eigenschaften, um Größenbeschränkungen zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="fc7a3-123">To ease working with large properties, MAPI allows service providers setting these properties to enforce size limits.</span></span> <span data-ttu-id="fc7a3-124">Diese Grenzwerte können je nach Folgenden variieren:</span><span class="sxs-lookup"><span data-stu-id="fc7a3-124">These limits can vary, depending on:</span></span>
  
- <span data-ttu-id="fc7a3-125">Gibt an, ob die Eigenschaften gelesen oder geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="fc7a3-125">Whether the properties are being read or written.</span></span>
    
- <span data-ttu-id="fc7a3-126">Implementierung der **IMAPIProp-Methoden** durch den Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="fc7a3-126">How the service provider implements the **IMAPIProp** methods.</span></span> 
    
- <span data-ttu-id="fc7a3-127">Überlegungen zur Laufzeit, z. B. Speichereinschränkungen.</span><span class="sxs-lookup"><span data-stu-id="fc7a3-127">Runtime considerations, such as memory constraints.</span></span>
    
- <span data-ttu-id="fc7a3-128">Übersetzungsprobleme mit Zeichensatz.</span><span class="sxs-lookup"><span data-stu-id="fc7a3-128">Character set translation issues.</span></span> 
    
<span data-ttu-id="fc7a3-129">Größenbeschränkungen können auch für Zeichenfolgen- und Binäreigenschaften festgelegt werden, wenn sie im Spaltensatz einer Tabelle verwendet werden, da es manchmal unmöglich ist, den Wert einer großen Eigenschaft sichtbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="fc7a3-129">Size limits can also be placed on string and binary properties when they are used in the column set of a table because it is sometimes impossible to make all of a large property's value visible.</span></span> <span data-ttu-id="fc7a3-130">Viele Dienstanbieter kürzen große Zeichenfolgen- oder Binäreigenschaften, die in Tabellen verwendet werden, auf 255 Byte.</span><span class="sxs-lookup"><span data-stu-id="fc7a3-130">Many service providers truncate large string or binary properties that are used in tables to 255 bytes.</span></span> 
  
<span data-ttu-id="fc7a3-131">Wenn ein Client die **GetProps-** oder **SetProps-Methode** eines Objekts aufruft, um mit einer großen Zeichenfolge oder binären Eigenschaft zu arbeiten, und der Aufruf aufgrund der Eigenschaftsgröße fehlschlägt, gibt die Methode den Fehlerwert MAPI_E_NOT_ENOUGH_MEMORY.</span><span class="sxs-lookup"><span data-stu-id="fc7a3-131">When a client calls an object's **GetProps** or **SetProps** method to work with a large string or binary property and the call fails because of the property size, the method returns the error value MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="fc7a3-132">Wenn **getProps** für eine bestimmte Eigenschaft einen Fehler hat, kann der Client wiederhergestellt werden, indem [er IMAPIProp::OpenProperty](imapiprop-openproperty.md) aufruft und den **IStream** für den Zugriff anfordert, indem IID_IStream als Schnittstellenbezeichner angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fc7a3-132">If it is **GetProps** that is failing for a specific property, the client can recover by calling [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and requesting the **IStream** for access by specifying IID_IStream as the interface identifier.</span></span> <span data-ttu-id="fc7a3-133">Mithilfe **von OpenProperty** kann der Client eine große Eigenschaft über eine Schnittstelle wie **IStream** abrufen, die besser für das Arbeiten mit großen Eigenschaften geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="fc7a3-133">Using **OpenProperty**, the client can retrieve a large property using an interface such as **IStream** that is better suited for working with large properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fc7a3-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc7a3-134">See also</span></span>



[<span data-ttu-id="fc7a3-135">Übersicht über die MAPI-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="fc7a3-135">MAPI Property Overview</span></span>](mapi-property-overview.md)

