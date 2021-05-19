---
title: Adressbucheinschränkungen
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
# <a name="address-book-restrictions"></a><span data-ttu-id="8500c-103">Adressbucheinschränkungen</span><span class="sxs-lookup"><span data-stu-id="8500c-103">Address Book Restrictions</span></span>

  
  
<span data-ttu-id="8500c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8500c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8500c-105">Adressbuchanbieter müssen drei Arten von Einschränkungen für die Inhaltstabellen ihrer Container unterstützen:</span><span class="sxs-lookup"><span data-stu-id="8500c-105">Address book providers are required to support three types of restrictions on the contents tables of their containers:</span></span>
  
- <span data-ttu-id="8500c-106">Einschränkungen für mehrdeutige Name-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8500c-106">Ambiguous name property restrictions</span></span>
    
- <span data-ttu-id="8500c-107">Eigenschafteneinschränkungen für Instanzschlüssel</span><span class="sxs-lookup"><span data-stu-id="8500c-107">Instance key property restrictions</span></span>
    
- <span data-ttu-id="8500c-108">Inhaltseinschränkungen für Den Anzeigenamen mit Präfix</span><span class="sxs-lookup"><span data-stu-id="8500c-108">Prefixed display name content restrictions</span></span>
    
<span data-ttu-id="8500c-109">Ambiguous name restrictions are property restrictions using the **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property to match recipient names with entries in address book containers.</span><span class="sxs-lookup"><span data-stu-id="8500c-109">Ambiguous name restrictions are property restrictions using the **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property to match recipient names with entries in address book containers.</span></span> <span data-ttu-id="8500c-110">Die  PR_ANR-Eigenschaftseinschränkung ist eine Art der Suche, bei der Adressbuchanbieter die passende Eigenschaft auswählen können, die für ihren Container am besten funktioniert.</span><span class="sxs-lookup"><span data-stu-id="8500c-110">The **PR_ANR** property restriction is a "best guess" type of search whereby address book providers can choose the matching property that works best for their container.</span></span> <span data-ttu-id="8500c-111">Beispielsweise kann ein Adressbuchanbieter die **PR_ANR-Einschränkung** implementieren, indem empfängernamen mit der **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))-Eigenschaft jedes Containereintrags übereinstimmen, während ein anderer Anbieter **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) verwendet.</span><span class="sxs-lookup"><span data-stu-id="8500c-111">For example, one address book provider might implement the **PR_ANR** restriction by matching recipient names against the **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) property of each container entry whereas another provider might use **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span>
  
<span data-ttu-id="8500c-112">MAPI empfiehlt, dass implementierungen der **PR_ANR** ein Gleichgewicht zwischen ausreichender Leistung und Benutzerzufriedenheit finden.</span><span class="sxs-lookup"><span data-stu-id="8500c-112">MAPI recommends that implementations of the **PR_ANR** restriction strike a balance between adequate performance and user satisfaction.</span></span> <span data-ttu-id="8500c-113">Die Benutzerzufriedenheit kann beeinträchtigt werden, wenn ein Adressbuchanbieter die Einschränkung so implementiert, dass zu wenige oder zu viele Übereinstimmungen gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="8500c-113">User satisfaction can be compromised when an address book provider implements the restriction in such a way that too few or too many matches are found.</span></span> <span data-ttu-id="8500c-114">Einige Adressbuchanbieter unterstützen einen so bezeichneten oder allgemeinen Namen, der in einem Dialogfeld nicht angezeigt werden kann, aber einer mehrdeutigen Namenseinschränkung entsprechen kann.</span><span class="sxs-lookup"><span data-stu-id="8500c-114">Some address book providers support what is known as a distinguished, or common, name that is not displayable in a dialog box but can match an ambiguous name restriction.</span></span> 
  
<span data-ttu-id="8500c-115">Eine typische Implementierung kann sein, den Anzeigenamen des Empfängers in Wörter zu analysieren, die mit jedem Eintrag übereinstimmen, der alle Wörter enthält.</span><span class="sxs-lookup"><span data-stu-id="8500c-115">A typical implementation might be to parse the recipient's display name into words, matching any entry that contains all of the words.</span></span> <span data-ttu-id="8500c-116">Achten Sie auf Details wie z. B. vertraulichkeit für die Wortposition, ob nicht übereinstimmende Wörter übereinstimmen und die Auswahl der Trennzeichen variieren kann.</span><span class="sxs-lookup"><span data-stu-id="8500c-116">Attention to details such as sensitivity to word position, whether nonconsecutive words are matched, and the choice of separator characters can vary.</span></span> <span data-ttu-id="8500c-117">Wenn der zu auflösende Name beispielsweise "Bill L"  ist, würde eine typische PR_ANR die folgenden Einträge als übereinstimmend auswählen:</span><span class="sxs-lookup"><span data-stu-id="8500c-117">For example, if the name to be resolved is "Bill L," a typical **PR_ANR** restriction would select the following entries as matching:</span></span> 
  
- <span data-ttu-id="8500c-118">Billy Larson</span><span class="sxs-lookup"><span data-stu-id="8500c-118">Billy Larson</span></span>
    
- <span data-ttu-id="8500c-119">Bill Lee</span><span class="sxs-lookup"><span data-stu-id="8500c-119">Bill Lee</span></span>
    
- <span data-ttu-id="8500c-120">Bill Logan Jr.</span><span class="sxs-lookup"><span data-stu-id="8500c-120">Bill Logan Jr.</span></span> 
    
- <span data-ttu-id="8500c-121">Sam Bill Lee</span><span class="sxs-lookup"><span data-stu-id="8500c-121">Sam Bill Lee</span></span>
    
<span data-ttu-id="8500c-122">Instanzschlüsseleinschränkungen oder **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))-Eigenschaftseinschränkungen werden bei der Implementierung von Listenfeldern verwendet, die in Clientanwendungen zum Anzeigen von #A0 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8500c-122">Instance key restrictions, or **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property restrictions, are used in the implementation of list boxes that are used in client applications for viewing MAPI tables.</span></span> <span data-ttu-id="8500c-123">Bei einigen Listenfeldimplementierungen können Benutzer mehrere Auswahlen treffen, einen Bildlauf nach oben oder unten durchführen und zum ersten ausgewählten Element zurückkehren.</span><span class="sxs-lookup"><span data-stu-id="8500c-123">Some list box implementations allow users to make multiple selections, scroll up or down, and return to the first item selected.</span></span> <span data-ttu-id="8500c-124">Um dieses Verhalten zu implementieren, rufen Clients [IMAPITable::FindRow auf](imapitable-findrow.md)und übergeben eine Eigenschaftseinschränkung für die **PR_INSTANCE_KEY-Eigenschaft** an die -Methode.</span><span class="sxs-lookup"><span data-stu-id="8500c-124">To implement this behavior, clients call [IMAPITable::FindRow](imapitable-findrow.md), passing a property restriction on the **PR_INSTANCE_KEY** property to the method.</span></span> <span data-ttu-id="8500c-125">Adressbuchanbieter müssen diese Einschränkung unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8500c-125">Address book providers are required to support this restriction.</span></span> 
  
<span data-ttu-id="8500c-126">Ein weiteres Feature von Listenfeldern, die für die Tabellenanzeige verwendet werden, ist die Möglichkeit, den Cursor basierend auf einer Reihe von Präfixzeichen zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="8500c-126">Another feature of list boxes used for table viewing is the ability to position the cursor based on a set of prefix characters.</span></span> <span data-ttu-id="8500c-127">Wenn der Benutzer mit der Eingabe von Präfixzeichen beginnt, verschiebt der Client den Cursor zum ersten Element, das mit diesen Zeichen beginnt.</span><span class="sxs-lookup"><span data-stu-id="8500c-127">As the user starts typing prefix characters, the client moves the cursor to the first item that begins with these characters.</span></span> <span data-ttu-id="8500c-128">Clients implementieren dieses Feature mit einer Inhaltseinschränkung, die auf der **PR_DISPLAY_NAME-Eigenschaft** und der FL_PREFIX Fuzzy-Ebene basiert.</span><span class="sxs-lookup"><span data-stu-id="8500c-128">Clients implement this feature with a content restriction based on the **PR_DISPLAY_NAME** property and the FL_PREFIX fuzzy level.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8500c-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8500c-129">See also</span></span>



[<span data-ttu-id="8500c-130">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="8500c-130">MAPI Tables</span></span>](mapi-tables.md)

