---
title: MAPI-Eigenschaftentags
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 380dad4c-7fbf-4c49-b67c-ab612c923499
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8dc37f1b594eeaa199b48f5946d10e60427d4988
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793057"
---
# <a name="mapi-property-tags"></a><span data-ttu-id="e1bbe-103">MAPI-Eigenschaftentags</span><span class="sxs-lookup"><span data-stu-id="e1bbe-103">MAPI property tags</span></span>
  
<span data-ttu-id="e1bbe-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e1bbe-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e1bbe-105">Ein Eigenschaftentag ist eine 32-Bit-Zahl mit dem eindeutigen Bezeichner für eine in Bits 16 bis 31 und einen Eigenschaftentyp in Bits 0 bis 15, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="e1bbe-105">A property tag is a 32-bit number that contains a unique property identifier in bits 16 through 31 and a property type in bits 0 through 15 as shown in the following illustration.</span></span> 
  
<span data-ttu-id="e1bbe-106">**Eigenschaftentags**</span><span class="sxs-lookup"><span data-stu-id="e1bbe-106">**Property tag elements**</span></span>
  
<span data-ttu-id="e1bbe-107">![Eigenschaftentags] (media/amapi_10.gif "Eigenschaftentags")</span><span class="sxs-lookup"><span data-stu-id="e1bbe-107">![Property tag elements](media/amapi_10.gif "Property tag elements")</span></span>
  
<span data-ttu-id="e1bbe-108">Eigenschaftentags dienen zum Identifizieren der MAPI-Eigenschaften und hat jede Eigenschaft, unabhängig davon, ob die Eigenschaft durch MAPI, einen Client oder einem Dienstanbieter definiert ist.</span><span class="sxs-lookup"><span data-stu-id="e1bbe-108">Property tags are used to identify MAPI properties and every property must have one, regardless of whether the property is defined by MAPI, a client, or a service provider.</span></span> <span data-ttu-id="e1bbe-109">MAPI definiert eine Reihe von Konstanten für Tag-Eigenschaft für seine Eigenschaften in der Headerdatei Mapitags.h. Diese Eigenschaften werden als "MAPI-definierte Eigenschaften" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e1bbe-109">MAPI defines a set of property tag constants for its properties in the Mapitags.h header file; these properties are referred to as the "MAPI-defined properties".</span></span> 
  
<span data-ttu-id="e1bbe-110">Konstanten für die Tag-Eigenschaft der Namenskonvention für Konsistenz und Bedienung.</span><span class="sxs-lookup"><span data-stu-id="e1bbe-110">The property tag constants follow a naming convention for consistency and ease of use.</span></span> <span data-ttu-id="e1bbe-111">Es gibt zwei Webparts auf den Namen der einzelnen Eigenschafts-Tag: ein Präfix PR_ und eine oder mehrere Zeichenfolgen, die die Inhalte der Eigenschaft beschreiben.</span><span class="sxs-lookup"><span data-stu-id="e1bbe-111">There are two parts to the name of each property tag: a PR_ prefix and one or more character strings that describe the contents of the property.</span></span> <span data-ttu-id="e1bbe-112">Mehrere Zeichenfolgen werden durch Unterstriche getrennt.</span><span class="sxs-lookup"><span data-stu-id="e1bbe-112">Multiple character strings are separated by underscores.</span></span> <span data-ttu-id="e1bbe-113">Beispielsweise ist das Eigenschafts-Tag für den Adresstyp der Empfänger einer Nachricht **PR\_ADDRTYPE** ([PidTagOrgAddrtype](http://msdn.microsoft.com/library/d40b5707-e4d5-4746-88d4-8616a3789789%28Office.15%29.aspx)) und die Eintrags-ID für den Ordner festgelegt, von der eine Kopie aller ausgehenden Nachrichten erhalten ist **PR_IPM_SENTMAIL_ ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e1bbe-113">For example, the property tag for the address type of a message recipient is **PR\_ADDRTYPE** ([PidTagOrgAddrtype](http://msdn.microsoft.com/library/d40b5707-e4d5-4746-88d4-8616a3789789%28Office.15%29.aspx)) and the entry identifier for the folder designated to receive a copy of every outbound message is **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).</span></span>
  
<span data-ttu-id="e1bbe-114">Einige Makros stehen zum Eigenschaftentags zwischen diesen [PROP_TYPE](prop_type.md), [eigensch_id](prop_id.md)und [PROP_TAG](prop_tag.md)entwickelt.</span><span class="sxs-lookup"><span data-stu-id="e1bbe-114">A few macros are available to help work with property tags, among them [PROP_TYPE](prop_type.md), [PROP_ID](prop_id.md), and [PROP_TAG](prop_tag.md).</span></span> <span data-ttu-id="e1bbe-115">**Eigenschaft\_Typ** extrahiert den Eigenschaftentyp aus das Eigenschafts-Tag **Eigenschaft\_ID** extrahiert den Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="e1bbe-115">**PROP\_TYPE** extracts the property type from the property tag; **PROP\_ID** extracts the identifier.</span></span> <span data-ttu-id="e1bbe-116">**PROP_TAG** erstellt ein Eigenschaftentag über einen Eigenschaftentyp und Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="e1bbe-116">**PROP_TAG** builds a property tag from a property type and identifier.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e1bbe-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e1bbe-117">See also</span></span>

- [<span data-ttu-id="e1bbe-118">�bersicht �ber die MAPI-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e1bbe-118">MAPI Property Overview</span></span>](mapi-property-overview.md)

