---
title: TAGS der MAPI-Eigenschaft
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 380dad4c-7fbf-4c49-b67c-ab612c923499
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 96211d3b6e1e4dfbd4c93a98c8dd04de10eac884
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328235"
---
# <a name="mapi-property-tags"></a><span data-ttu-id="e8705-103">TAGS der MAPI-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e8705-103">MAPI property tags</span></span>
  
<span data-ttu-id="e8705-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8705-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8705-105">Ein Eigenschaftstag ist eine 32-Bit-Zahl, die einen eindeutigen Eigenschaftenbezeichner in den Bits 16 bis 31 und einen Eigenschaftstyp in bits 0 bis 15 enthält, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="e8705-105">A property tag is a 32-bit number that contains a unique property identifier in bits 16 through 31 and a property type in bits 0 through 15 as shown in the following illustration.</span></span> 
  
<span data-ttu-id="e8705-106">**Eigenschafts-Tag-Elemente**</span><span class="sxs-lookup"><span data-stu-id="e8705-106">**Property tag elements**</span></span>
  
<span data-ttu-id="e8705-107">![Eigenschaftstagelemente](media/amapi_10.gif "Eigenschaftentagelemente")</span><span class="sxs-lookup"><span data-stu-id="e8705-107">![Property tag elements](media/amapi_10.gif "Property tag elements")</span></span>
  
<span data-ttu-id="e8705-108">Eigenschaftstags werden verwendet, um MAPI-Eigenschaften zu identifizieren, und jede Eigenschaft muss über eine verfügen, unabhängig davon, ob die Eigenschaft von MAPI, einem Client oder einem Dienstanbieter definiert wird.</span><span class="sxs-lookup"><span data-stu-id="e8705-108">Property tags are used to identify MAPI properties and every property must have one, regardless of whether the property is defined by MAPI, a client, or a service provider.</span></span> <span data-ttu-id="e8705-109">MAPI definiert eine Reihe von Eigenschaftentagkonstante für seine Eigenschaften in der Mapitags.h-Headerdatei. diese Eigenschaften werden als "MAPI-definierte Eigenschaften" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e8705-109">MAPI defines a set of property tag constants for its properties in the Mapitags.h header file; these properties are referred to as the "MAPI-defined properties".</span></span> 
  
<span data-ttu-id="e8705-110">Die Eigenschaftentagkonstante folgen einer Benennungskonvention für Konsistenz und Benutzerfreundlichkeit.</span><span class="sxs-lookup"><span data-stu-id="e8705-110">The property tag constants follow a naming convention for consistency and ease of use.</span></span> <span data-ttu-id="e8705-111">Der Name jedes Eigenschaftstags enthält zwei Teile: ein PR_-Präfix und eine oder mehrere Zeichenzeichenfolgen, die den Inhalt der Eigenschaft beschreiben.</span><span class="sxs-lookup"><span data-stu-id="e8705-111">There are two parts to the name of each property tag: a PR_ prefix and one or more character strings that describe the contents of the property.</span></span> <span data-ttu-id="e8705-112">Zeichenfolgen mit mehreren Zeichen werden durch Unterstriche getrennt.</span><span class="sxs-lookup"><span data-stu-id="e8705-112">Multiple character strings are separated by underscores.</span></span> <span data-ttu-id="e8705-113">Das Eigenschaftstag für den Adresstyp eines Nachrichtenempfängers ist z. B. **PR \_ ADDRTYPE** ([PidTagOrgAddrtype](https://msdn.microsoft.com/library/d40b5707-e4d5-4746-88d4-8616a3789789%28Office.15%29.aspx)) und der Eintragsbezeichner für den Ordner, der für den Empfang einer Kopie jeder ausgehenden Nachricht bestimmt **ist, lautet PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e8705-113">For example, the property tag for the address type of a message recipient is **PR\_ADDRTYPE** ([PidTagOrgAddrtype](https://msdn.microsoft.com/library/d40b5707-e4d5-4746-88d4-8616a3789789%28Office.15%29.aspx)) and the entry identifier for the folder designated to receive a copy of every outbound message is **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).</span></span>
  
<span data-ttu-id="e8705-114">Einige Makros stehen zur Verfügung, um die Arbeit mit Eigenschaftstags zu unterstützen, darunter [PROP_TYPE](prop_type.md), [PROP_ID](prop_id.md)und [PROP_TAG](prop_tag.md).</span><span class="sxs-lookup"><span data-stu-id="e8705-114">A few macros are available to help work with property tags, among them [PROP_TYPE](prop_type.md), [PROP_ID](prop_id.md), and [PROP_TAG](prop_tag.md).</span></span> <span data-ttu-id="e8705-115">**PROP \_ TYPE** extrahiert den Eigenschaftentyp aus dem Eigenschaftstag. **PROP \_ ID** extrahiert den Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="e8705-115">**PROP\_TYPE** extracts the property type from the property tag; **PROP\_ID** extracts the identifier.</span></span> <span data-ttu-id="e8705-116">**PROP_TAG** erstellt ein Eigenschaftentag aus einem Eigenschaftentyp und einem Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="e8705-116">**PROP_TAG** builds a property tag from a property type and identifier.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e8705-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8705-117">See also</span></span>

- [<span data-ttu-id="e8705-118">Übersicht über die MAPI-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e8705-118">MAPI Property Overview</span></span>](mapi-property-overview.md)

