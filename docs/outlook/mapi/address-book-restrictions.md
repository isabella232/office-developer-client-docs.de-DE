---
title: Adressbuch Einschränkungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ace8c03-45a7-484b-8c12-516ac0e40dc2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7419c174c1f68653794c2dbd836577e8dd3e596e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432800"
---
# <a name="address-book-restrictions"></a><span data-ttu-id="126f0-103">Adressbuch Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="126f0-103">Address Book Restrictions</span></span>

  
  
<span data-ttu-id="126f0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="126f0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="126f0-105">Adressbuchanbieter müssen drei Arten von Einschränkungen für die Inhaltstabellen ihrer Container unterstützen:</span><span class="sxs-lookup"><span data-stu-id="126f0-105">Address book providers are required to support three types of restrictions on the contents tables of their containers:</span></span>
  
- <span data-ttu-id="126f0-106">Eigenschafteneinschränkungen für mehrdeutige Namen</span><span class="sxs-lookup"><span data-stu-id="126f0-106">Ambiguous name property restrictions</span></span>
    
- <span data-ttu-id="126f0-107">Eigenschafteneinschränkungen für Instanzenschlüssel</span><span class="sxs-lookup"><span data-stu-id="126f0-107">Instance key property restrictions</span></span>
    
- <span data-ttu-id="126f0-108">Inhaltseinschränkungen für vordefinierte Anzeigename</span><span class="sxs-lookup"><span data-stu-id="126f0-108">Prefixed display name content restrictions</span></span>
    
<span data-ttu-id="126f0-109">Einschränkungen bei mehrdeutigen Namen sind Eigenschaftseinschränkungen mithilfe der **PR_ANR** ([pidtaganr (](pidtaganr-canonical-property.md))-Eigenschaft, um Empfängernamen mit Einträgen in Adressbuch Containern abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="126f0-109">Ambiguous name restrictions are property restrictions using the **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property to match recipient names with entries in address book containers.</span></span> <span data-ttu-id="126f0-110">Die **PR_ANR** -Eigenschaftseinschränkung ist ein "Best Guess"-Suchtyp, bei dem Adressbuchanbieter die passende Eigenschaft auswählen können, die für ihren Container am besten geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="126f0-110">The **PR_ANR** property restriction is a "best guess" type of search whereby address book providers can choose the matching property that works best for their container.</span></span> <span data-ttu-id="126f0-111">Beispielsweise kann ein Adressbuchanbieter die **PR_ANR** -Einschränkung implementieren, indem Empfängernamen mit der **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))-Eigenschaft der einzelnen Container Einträge verglichen werden, während ein anderer Anbieter PR_DISPLAY verwenden kann. \*\* _NAME\*\* ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="126f0-111">For example, one address book provider might implement the **PR_ANR** restriction by matching recipient names against the **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) property of each container entry whereas another provider might use **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span>
  
<span data-ttu-id="126f0-112">MAPI empfiehlt, dass Implementierungen der **PR_ANR** -Einschränkung eine Balance zwischen adäquater Leistung und Benutzerzufriedenheit finden.</span><span class="sxs-lookup"><span data-stu-id="126f0-112">MAPI recommends that implementations of the **PR_ANR** restriction strike a balance between adequate performance and user satisfaction.</span></span> <span data-ttu-id="126f0-113">Die Benutzerzufriedenheit kann beeinträchtigt werden, wenn ein Adressbuchanbieter die Einschränkung so implementiert, dass zu wenige oder zu viele Übereinstimmungen gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="126f0-113">User satisfaction can be compromised when an address book provider implements the restriction in such a way that too few or too many matches are found.</span></span> <span data-ttu-id="126f0-114">Einige Adressbuchanbieter unterstützen den Namen Distinguished oder Common, der nicht in einem Dialogfeld angezeigt werden kann, jedoch mit einer Einschränkung für mehrdeutige Namen übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="126f0-114">Some address book providers support what is known as a distinguished, or common, name that is not displayable in a dialog box but can match an ambiguous name restriction.</span></span> 
  
<span data-ttu-id="126f0-115">Eine typische Implementierung besteht darin, den Anzeigenamen des Empfängers in Wörter zu analysieren, die mit allen Wörtern übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="126f0-115">A typical implementation might be to parse the recipient's display name into words, matching any entry that contains all of the words.</span></span> <span data-ttu-id="126f0-116">Beachten Sie Details wie die Vertraulichkeit der Wortposition, ob nicht aufeinanderfolgende Wörter übereinstimmen, und die Auswahl von Trennzeichen kann variieren.</span><span class="sxs-lookup"><span data-stu-id="126f0-116">Attention to details such as sensitivity to word position, whether nonconsecutive words are matched, and the choice of separator characters can vary.</span></span> <span data-ttu-id="126f0-117">Wenn beispielsweise der zu lösende Name "Bill L" lautet, würde eine typische **PR_ANR** -Einschränkung die folgenden Einträge als Abgleich auswählen:</span><span class="sxs-lookup"><span data-stu-id="126f0-117">For example, if the name to be resolved is "Bill L," a typical **PR_ANR** restriction would select the following entries as matching:</span></span> 
  
- <span data-ttu-id="126f0-118">Billy Larson</span><span class="sxs-lookup"><span data-stu-id="126f0-118">Billy Larson</span></span>
    
- <span data-ttu-id="126f0-119">Bill Lee</span><span class="sxs-lookup"><span data-stu-id="126f0-119">Bill Lee</span></span>
    
- <span data-ttu-id="126f0-120">Bill Logan Jr.</span><span class="sxs-lookup"><span data-stu-id="126f0-120">Bill Logan Jr.</span></span> 
    
- <span data-ttu-id="126f0-121">Sam Bill Lee</span><span class="sxs-lookup"><span data-stu-id="126f0-121">Sam Bill Lee</span></span>
    
<span data-ttu-id="126f0-122">Instanzenschlüssel Einschränkungen oder **PR_INSTANCE_KEY** ([pidtaginstancekey (](pidtaginstancekey-canonical-property.md))-Eigenschaftseinschränkungen werden bei der Implementierung von Listenfeldern verwendet, die in clientANWENDUNGEN zum Anzeigen von MAPI-Tabellen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="126f0-122">Instance key restrictions, or **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property restrictions, are used in the implementation of list boxes that are used in client applications for viewing MAPI tables.</span></span> <span data-ttu-id="126f0-123">In einigen Listenfeld Implementierungen können Benutzer mehrere Optionen auswählen, nach oben oder unten scrollen und zum ersten ausgewählten Element zurückkehren.</span><span class="sxs-lookup"><span data-stu-id="126f0-123">Some list box implementations allow users to make multiple selections, scroll up or down, and return to the first item selected.</span></span> <span data-ttu-id="126f0-124">Um dieses Verhalten zu implementieren, rufen die Clients [IMAPITable:: FindRow](imapitable-findrow.md)auf und übergeben eine Eigenschaftseinschränkung für die **PR_INSTANCE_KEY** -Eigenschaft an die Methode.</span><span class="sxs-lookup"><span data-stu-id="126f0-124">To implement this behavior, clients call [IMAPITable::FindRow](imapitable-findrow.md), passing a property restriction on the **PR_INSTANCE_KEY** property to the method.</span></span> <span data-ttu-id="126f0-125">Adressbuchanbieter sind zur Unterstützung dieser Einschränkung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="126f0-125">Address book providers are required to support this restriction.</span></span> 
  
<span data-ttu-id="126f0-126">Ein weiteres Feature von Listenfeldern, die für die Tabellenanzeige verwendet werden, ist die Möglichkeit, den Cursor auf der Grundlage einer Reihe von Präfixzeichen zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="126f0-126">Another feature of list boxes used for table viewing is the ability to position the cursor based on a set of prefix characters.</span></span> <span data-ttu-id="126f0-127">Wenn der Benutzer mit dem Eingeben von Präfixzeichen beginnt, verschiebt der Client den Cursor auf das erste Element, das mit diesen Zeichen beginnt.</span><span class="sxs-lookup"><span data-stu-id="126f0-127">As the user starts typing prefix characters, the client moves the cursor to the first item that begins with these characters.</span></span> <span data-ttu-id="126f0-128">Clients implementieren dieses Feature mit einer Inhaltseinschränkung, die auf der **PR_DISPLAY_NAME** -Eigenschaft und der FL_PREFIX-Fuzzy-Ebene basiert.</span><span class="sxs-lookup"><span data-stu-id="126f0-128">Clients implement this feature with a content restriction based on the **PR_DISPLAY_NAME** property and the FL_PREFIX fuzzy level.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="126f0-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="126f0-129">See also</span></span>



[<span data-ttu-id="126f0-130">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="126f0-130">MAPI Tables</span></span>](mapi-tables.md)

