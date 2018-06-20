---
title: Benannte Eigenschaften MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 464b1297-9d90-47bd-afc4-3dc63b106cb7
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e755c18ef3cc32f9a00169f19cf336eace447a32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793025"
---
# <a name="mapi-named-properties"></a><span data-ttu-id="b47ee-103">Benannte Eigenschaften MAPI</span><span class="sxs-lookup"><span data-stu-id="b47ee-103">MAPI Named Properties</span></span>
 
<span data-ttu-id="b47ee-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b47ee-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b47ee-105">MAPI bietet die Möglichkeit zum Zuweisen von Namen zu Eigenschaften, um Managementsystems eindeutige Bezeichner zuzuordnen, sowie für diese Zuordnung persistent.</span><span class="sxs-lookup"><span data-stu-id="b47ee-105">MAPI provides a facility for assigning names to properties, for mapping these names to unique identifiers, and for making this mapping persistent.</span></span> <span data-ttu-id="b47ee-106">Beständigen Namen Bezeichner Zuordnung wird sichergestellt, dass Eigenschaftennamen in allen Sitzungen gültig.</span><span class="sxs-lookup"><span data-stu-id="b47ee-106">Persistent name to identifier mapping ensures that property names remain valid across sessions.</span></span>
  
<span data-ttu-id="b47ee-107">Zum Definieren einer benannten Eigenschaft ein Client oder Dienstanbieter bildet einen Namen und speichert sie in einer [MAPINAMEID](mapinameid.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="b47ee-107">To define a named property, a client or service provider makes up a name and stores it in a [MAPINAMEID](mapinameid.md) structure.</span></span> <span data-ttu-id="b47ee-108">Da Namen von einen global eindeutigen Bezeichner der 32-Bit, oder die GUID und entweder ein Unicode-Zeichen Zeichenfolge oder eines numerischen Wert vorgenommen werden, können Ersteller von benannten Eigenschaften aussagekräftige Namen des Duplizierung Wiederholungsversuchs erstellen.</span><span class="sxs-lookup"><span data-stu-id="b47ee-108">Because names are made up of a 32-bit globally unique identifier, or GUID, and either a Unicode character string or numeric value, creators of named properties can create meaningful names without fear of duplication.</span></span> <span data-ttu-id="b47ee-109">Namen sind eindeutig, und sie können verwendet werden, ohne dabei den Wert der ihre-IDs zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="b47ee-109">Names are unique and they can be used without regard to the value of their identifiers.</span></span> 
  
<span data-ttu-id="b47ee-110">Zur Unterstützung der benannter Eigenschaften auf ein Dienstanbieter implementiert zwei Methoden – [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) und [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) – übersetzen zwischen Namen und Bezeichner und seine [IMAPIProp::GetProps](imapiprop-getprops.md) [ ermöglichen IMAPIProp::SetProps](imapiprop-setprops.md) Methoden zum Abrufen und Ändern von Eigenschaften mit Bezeichnern im Bereich benannten Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b47ee-110">To support named properties, a service provider implements two methods — [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) and [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) — to translate between names and identifiers and to allow its [IMAPIProp::GetProps](imapiprop-getprops.md)[IMAPIProp::SetProps](imapiprop-setprops.md) methods to retrieve and modify properties with identifiers in the named property range.</span></span> <span data-ttu-id="b47ee-111">Der Bereich für benannte Eigenschaftenbezeichner liegt zwischen 0 x 8000 und 0xFFFE.</span><span class="sxs-lookup"><span data-stu-id="b47ee-111">The range for named property identifiers is between 0x8000 and 0xFFFE.</span></span> 
  
<span data-ttu-id="b47ee-112">Jedes Objekt, das die **IMAPIProp** -Schnittstelle implementiert wird, kann benannte Eigenschaften unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b47ee-112">Any object that implements the **IMAPIProp** interface can support named properties.</span></span> <span data-ttu-id="b47ee-113">Von adressbuchanbietern implementierte, die es ermöglichen, dass Einträge von anderen Anbietern in ihre Container und die Nachricht kopiert werden Anbieter speichern, die zum Erstellen von beliebigen Nachrichtentypen verwendet werden können sind erforderlich, um diese Unterstützung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b47ee-113">Address book providers that allow entries from other providers to be copied into their containers and message store providers that can be used to create arbitrary message types are required to supply this support.</span></span> <span data-ttu-id="b47ee-114">Es ist eine Option für alle anderen Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="b47ee-114">It is an option for all other service providers.</span></span> <span data-ttu-id="b47ee-115">Anbieter, die keine Unterstützung für benannte Eigenschaften MAPI_E_NO_SUPPORT aus den Methoden **GetIDsFromNames** und **GetNamesFromIDs** zurückzugeben und Eigenschaften mit IDs der 0 x 8000 oder höher, Rückgabe MAPI_E_UNEXPECTED festgelegt werden, in der **Verweigern SPropProblemarray**.</span><span class="sxs-lookup"><span data-stu-id="b47ee-115">Providers that do not support named properties return MAPI_E_NO_SUPPORT from the **GetIDsFromNames** and **GetNamesFromIDs** methods and refuse to set any properties with identifiers of 0x8000 or greater, returning MAPI_E_UNEXPECTED in the **SPropProblemarray**.</span></span>
  
<span data-ttu-id="b47ee-116">Erstellen von Namen für Eigenschaften ist eine Möglichkeit für Clients, um neue Eigenschaften für vorhandenen oder benutzerdefinierten Nachrichtenklassen definieren.</span><span class="sxs-lookup"><span data-stu-id="b47ee-116">Creating names for properties is one way for clients to define new properties for existing or custom message classes.</span></span> <span data-ttu-id="b47ee-117">Benannte Eigenschaften können Dienstanbieter um einzigartigen Merkmale von messaging-Systemen verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="b47ee-117">Service providers can use named properties to expose unique features of their messaging systems.</span></span> <span data-ttu-id="b47ee-118">Geben Sie eine alternative Möglichkeit zum Verweisen auf Eigenschaften mit Bezeichnern unter 0 x 8000 ist eine andere Verwendung für benannte Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b47ee-118">Yet another use for named properties is to provide an alternate way of referring to properties with identifiers below 0x8000.</span></span> 
  
<span data-ttu-id="b47ee-119">Beispielsweise konnte ein Client ähnlichen Code wie den folgenden Code verwenden, um die Namen aller benannten Eigenschaften eines Objekts abzurufen:</span><span class="sxs-lookup"><span data-stu-id="b47ee-119">For example, a client could use code similar to the following code to retrieve the names for all of an object's named properties:</span></span>
  
```cpp
LPSPropTagArray FAR *    lppPropTags = NULL;
LPGUID                   lpPropSetGuid = NULL;
ULONG FAR *              lpcPropNames;
LPMAPINAMEID FAR * FAR * lpppPropNames;
lpMAPIProp->GetNamesFromIDs (lppPropTags,
                             lpPropSetGuid,
                             0,
                             lpcPropNames,
                             lpppPropNames);
 
```

<span data-ttu-id="b47ee-120">Um die Namen aller aus dem Eigenschaftensatz PS_PUBLIC_STRINGS anzufordern, würde ein Client NULL in der Property Set-Parameters, PS_PUBLIC_STRINGS wie folgt ersetzen:</span><span class="sxs-lookup"><span data-stu-id="b47ee-120">To request all names from the PS_PUBLIC_STRINGS property set, a client would replace the NULL in the property set parameter to PS_PUBLIC_STRINGS as follows:</span></span> 
  
```cpp
LPSPropTagArray FAR *    lppPropTags = NULL;
LPGUID                   lpPropSetGuid = &PS_PUBLIC_STRINGS;
ULONG FAR *              lpcPropNames;
LPMAPINAMEID FAR * FAR * lpppPropNames;
lpMAPIProp->GetNamesFromIDs (lppPropTags,
                             lpPropSetGuid,
                             0,
                             lpcPropNames,
                             lpppPropNames);
 
```

## <a name="see-also"></a><span data-ttu-id="b47ee-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b47ee-121">See also</span></span>

- [<span data-ttu-id="b47ee-122">�bersicht �ber die MAPI-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b47ee-122">MAPI Property Overview</span></span>](mapi-property-overview.md)

