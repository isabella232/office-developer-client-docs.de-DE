---
title: Benannte Eigenschaften MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 464b1297-9d90-47bd-afc4-3dc63b106cb7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d83b98b4f06c648676852673a694a63b78f568b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435047"
---
# <a name="mapi-named-properties"></a><span data-ttu-id="c5eeb-103">Benannte Eigenschaften MAPI</span><span class="sxs-lookup"><span data-stu-id="c5eeb-103">MAPI Named Properties</span></span>
 
<span data-ttu-id="c5eeb-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c5eeb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c5eeb-105">MAPI bietet eine Möglichkeit zum Zuweisen von Namen zu Eigenschaften, um diese Namen eindeutigen Bezeichnern zuzuordnen und diese Zuordnung persistent zu machen.</span><span class="sxs-lookup"><span data-stu-id="c5eeb-105">MAPI provides a facility for assigning names to properties, for mapping these names to unique identifiers, and for making this mapping persistent.</span></span> <span data-ttu-id="c5eeb-106">Persistent Name to Identifier Mapping stellt sicher, dass Eigenschaftsnamen in allen Sitzungen gültig bleiben.</span><span class="sxs-lookup"><span data-stu-id="c5eeb-106">Persistent name to identifier mapping ensures that property names remain valid across sessions.</span></span>
  
<span data-ttu-id="c5eeb-107">Zum Definieren einer benannten Eigenschaft erstellt ein Client oder Dienstanbieter einen Namen und speichert ihn in einer [MAPINAMEID](mapinameid.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="c5eeb-107">To define a named property, a client or service provider makes up a name and stores it in a [MAPINAMEID](mapinameid.md) structure.</span></span> <span data-ttu-id="c5eeb-108">Da Namen aus einem global eindeutigen 32-Bit-Bezeichner oder einer GUID und entweder einer Unicode-Zeichenfolge oder einem numerischen Wert bestehen, können Ersteller benannter Eigenschaften aussagekräftige Namen erstellen, ohne dass eine Duplizierung vorliegt.</span><span class="sxs-lookup"><span data-stu-id="c5eeb-108">Because names are made up of a 32-bit globally unique identifier, or GUID, and either a Unicode character string or numeric value, creators of named properties can create meaningful names without fear of duplication.</span></span> <span data-ttu-id="c5eeb-109">Namen sind eindeutig und können unabhängig vom Wert ihrer Bezeichner verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c5eeb-109">Names are unique and they can be used without regard to the value of their identifiers.</span></span> 
  
<span data-ttu-id="c5eeb-110">Zur Unterstützung benannter Eigenschaften implementiert ein Dienstanbieter zwei Methoden – [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) und [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md) –, um zwischen Namen und Bezeichnern zu übersetzen und ihre IMAPIProp zu ermöglichen [:: GetProps](imapiprop-getprops.md) [ IMAPIProp::](imapiprop-setprops.md) SetProps-Methoden zum Abrufen und Ändern von Eigenschaften mit Bezeichnern im benannten Eigenschaftenbereich.</span><span class="sxs-lookup"><span data-stu-id="c5eeb-110">To support named properties, a service provider implements two methods — [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) and [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) — to translate between names and identifiers and to allow its [IMAPIProp::GetProps](imapiprop-getprops.md)[IMAPIProp::SetProps](imapiprop-setprops.md) methods to retrieve and modify properties with identifiers in the named property range.</span></span> <span data-ttu-id="c5eeb-111">Der Range für benannte Eigenschaftsbezeichner liegt zwischen 0X8000 und 0xFFFE.</span><span class="sxs-lookup"><span data-stu-id="c5eeb-111">The range for named property identifiers is between 0x8000 and 0xFFFE.</span></span> 
  
<span data-ttu-id="c5eeb-112">Jedes Objekt, das die **IMAPIProp** -Schnittstelle implementiert, kann benannte Eigenschaften unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c5eeb-112">Any object that implements the **IMAPIProp** interface can support named properties.</span></span> <span data-ttu-id="c5eeb-113">Adressbuchanbieter, die das Kopieren von Einträgen anderer Anbieter in Ihre Container und Nachrichtenspeicher Anbieter zulassen, die zum Erstellen beliebiger Nachrichtentypen verwendet werden können, sind erforderlich, um diese Unterstützung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c5eeb-113">Address book providers that allow entries from other providers to be copied into their containers and message store providers that can be used to create arbitrary message types are required to supply this support.</span></span> <span data-ttu-id="c5eeb-114">Dies ist eine Option für alle anderen Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="c5eeb-114">It is an option for all other service providers.</span></span> <span data-ttu-id="c5eeb-115">Anbieter, die benannte Eigenschaften nicht unterstützen, geben MAPI_E_NO_SUPPORT aus der **GetIDsFromNames** -und der **GetNamesFromIDs** -Methode zurück und lehnen das Festlegen von Eigenschaften mit Bezeichnern von 0X8000 oder höher ab und geben MAPI_E_UNEXPECTED in der \*\* SPropProblemarray\*\*.</span><span class="sxs-lookup"><span data-stu-id="c5eeb-115">Providers that do not support named properties return MAPI_E_NO_SUPPORT from the **GetIDsFromNames** and **GetNamesFromIDs** methods and refuse to set any properties with identifiers of 0x8000 or greater, returning MAPI_E_UNEXPECTED in the **SPropProblemarray**.</span></span>
  
<span data-ttu-id="c5eeb-116">Das Erstellen von Namen für Eigenschaften ist eine Möglichkeit für Clients, neue Eigenschaften für vorhandene oder benutzerdefinierte Nachrichtenklassen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="c5eeb-116">Creating names for properties is one way for clients to define new properties for existing or custom message classes.</span></span> <span data-ttu-id="c5eeb-117">Dienstanbieter können benannte Eigenschaften verwenden, um eindeutige Features Ihrer Messagingsysteme anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c5eeb-117">Service providers can use named properties to expose unique features of their messaging systems.</span></span> <span data-ttu-id="c5eeb-118">Eine weitere Verwendung für benannte Eigenschaften besteht darin, eine alternative Möglichkeit zum Verweisen auf Eigenschaften mit Bezeichnern unter 0X8000 bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c5eeb-118">Yet another use for named properties is to provide an alternate way of referring to properties with identifiers below 0x8000.</span></span> 
  
<span data-ttu-id="c5eeb-119">Ein Client könnte beispielsweise Code verwenden, der dem folgenden Code ähnelt, um die Namen für alle benannten Eigenschaften eines Objekts abzurufen:</span><span class="sxs-lookup"><span data-stu-id="c5eeb-119">For example, a client could use code similar to the following code to retrieve the names for all of an object's named properties:</span></span>
  
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

<span data-ttu-id="c5eeb-120">Um alle Namen aus dem PS_PUBLIC_STRINGS-Eigenschaftensatz anzufordern, würde ein Client den NULL-Wert im Eigenschaftensatz-Parameter wie folgt in PS_PUBLIC_STRINGS ersetzen:</span><span class="sxs-lookup"><span data-stu-id="c5eeb-120">To request all names from the PS_PUBLIC_STRINGS property set, a client would replace the NULL in the property set parameter to PS_PUBLIC_STRINGS as follows:</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="c5eeb-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5eeb-121">See also</span></span>

- [<span data-ttu-id="c5eeb-122">Übersicht über die MAPI-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c5eeb-122">MAPI Property Overview</span></span>](mapi-property-overview.md)

