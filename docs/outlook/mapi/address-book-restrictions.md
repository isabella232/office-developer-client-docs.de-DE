---
title: Adressbucheinschränkungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ace8c03-45a7-484b-8c12-516ac0e40dc2
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b8ad765a2bbd3aafd87a7eff79993978816729b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791271"
---
# <a name="address-book-restrictions"></a><span data-ttu-id="aa994-103">Adressbucheinschränkungen</span><span class="sxs-lookup"><span data-stu-id="aa994-103">Address Book Restrictions</span></span>

  
  
<span data-ttu-id="aa994-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="aa994-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="aa994-105">Von adressbuchanbietern implementierte sind zur Unterstützung von drei Arten von Einschränkungen für die Tabellen Inhalt, der ihre Container erforderlich:</span><span class="sxs-lookup"><span data-stu-id="aa994-105">Address book providers are required to support three types of restrictions on the contents tables of their containers:</span></span>
  
- <span data-ttu-id="aa994-106">Mehrdeutiger Name eigenschaftseinschränkungen</span><span class="sxs-lookup"><span data-stu-id="aa994-106">Ambiguous name property restrictions</span></span>
    
- <span data-ttu-id="aa994-107">Wichtige eigenschaftseinschränkungen Instanz</span><span class="sxs-lookup"><span data-stu-id="aa994-107">Instance key property restrictions</span></span>
    
- <span data-ttu-id="aa994-108">Als Präfix Display Name Content Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="aa994-108">Prefixed display name content restrictions</span></span>
    
<span data-ttu-id="aa994-109">Mehrdeutiger Name Einschränkungen sind Suchkriterien in Eigenschaft mithilfe der **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md))-Eigenschaft Empfängernamen mit Einträgen in Address Book Containern übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="aa994-109">Ambiguous name restrictions are property restrictions using the **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property to match recipient names with entries in address book containers.</span></span> <span data-ttu-id="aa994-110">Die Einschränkung der **PR_ANR** -Eigenschaft ist ein "am besten erraten" suchen, bei dem adressbuchanbietern implementierte übereinstimmende Eigenschaft auswählen können, die am besten für ihre Container.</span><span class="sxs-lookup"><span data-stu-id="aa994-110">The **PR_ANR** property restriction is a "best guess" type of search whereby address book providers can choose the matching property that works best for their container.</span></span> <span data-ttu-id="aa994-111">Beispielsweise kann eine Adressbuchanbieter die Einschränkung **PR_ANR** nach übereinstimmenden Empfängernamen anhand der **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))-Eigenschaft jedes Container-Eintrags implementieren, während einen anderen Anbieter **PR_DISPLAY verwenden könnten Dann zur Name** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="aa994-111">For example, one address book provider might implement the **PR_ANR** restriction by matching recipient names against the **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) property of each container entry whereas another provider might use **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span>
  
<span data-ttu-id="aa994-112">MAPI empfiehlt, Implementierungen der Einschränkung **PR_ANR** ein Gleichgewicht zwischen eine angemessene Leistung und Benutzerzufriedenheit hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="aa994-112">MAPI recommends that implementations of the **PR_ANR** restriction strike a balance between adequate performance and user satisfaction.</span></span> <span data-ttu-id="aa994-113">Bei der Adressbuch-Dienstanbieter die Einschränkung wieder in einem solchen implementiert Benutzerzufriedenheit gewährleistet eine Möglichkeit, die zu wenige oder zu viele Treffer gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="aa994-113">User satisfaction can be compromised when an address book provider implements the restriction in such a way that too few or too many matches are found.</span></span> <span data-ttu-id="aa994-114">Einige adressbuchanbietern implementierte unterstützen, was als Name eines definierten oder selten, bekannt ist, die ist nicht in einem Dialogfeld anzeigbaren aber kann eine Einschränkung mehrdeutiger Name übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="aa994-114">Some address book providers support what is known as a distinguished, or common, name that is not displayable in a dialog box but can match an ambiguous name restriction.</span></span> 
  
<span data-ttu-id="aa994-115">Eine typische Implementierung möglicherweise zum Analysieren der Anzeigename des Empfängers in Wörter, gleicht alle Einträge, die alle Wörter enthält.</span><span class="sxs-lookup"><span data-stu-id="aa994-115">A typical implementation might be to parse the recipient's display name into words, matching any entry that contains all of the words.</span></span> <span data-ttu-id="aa994-116">Aufmerksamkeit auf Details wie etwa Empfindlichkeit gegenüber Word Position, gibt an, ob nicht aufeinander folgende Wörter abgeglichen werden und welche Trennzeichen können variieren.</span><span class="sxs-lookup"><span data-stu-id="aa994-116">Attention to details such as sensitivity to word position, whether nonconsecutive words are matched, and the choice of separator characters can vary.</span></span> <span data-ttu-id="aa994-117">Beispielsweise ist der Name aufgelöst werden "Bill L", würde eine typische **PR_ANR** Einschränkung die folgenden Einträge als Entsprechung aktivieren:</span><span class="sxs-lookup"><span data-stu-id="aa994-117">For example, if the name to be resolved is "Bill L," a typical **PR_ANR** restriction would select the following entries as matching:</span></span> 
  
- <span data-ttu-id="aa994-118">Frank Larson</span><span class="sxs-lookup"><span data-stu-id="aa994-118">Billy Larson</span></span>
    
- <span data-ttu-id="aa994-119">Bill Kelly</span><span class="sxs-lookup"><span data-stu-id="aa994-119">Bill Lee</span></span>
    
- <span data-ttu-id="aa994-120">Bill Logan Jr.</span><span class="sxs-lookup"><span data-stu-id="aa994-120">Bill Logan Jr.</span></span> 
    
- <span data-ttu-id="aa994-121">Sam Bill Lee</span><span class="sxs-lookup"><span data-stu-id="aa994-121">Sam Bill Lee</span></span>
    
<span data-ttu-id="aa994-122">Wichtige Einschränkungen Instanz oder Suchkriterien in Eigenschaft **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), werden in der Implementierung von Listenfeldern verwendet, die in Clientanwendungen für die Anzeige von MAPI-Tabellen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aa994-122">Instance key restrictions, or **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property restrictions, are used in the implementation of list boxes that are used in client applications for viewing MAPI tables.</span></span> <span data-ttu-id="aa994-123">Einige Liste Feld Implementierungen zulassen, dass Benutzer mehrere treffen, einen Bildlauf nach oben oder nach unten und Zurücksetzen auf das erste Element ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="aa994-123">Some list box implementations allow users to make multiple selections, scroll up or down, and return to the first item selected.</span></span> <span data-ttu-id="aa994-124">Um dieses Verhalten zu implementieren, rufen Clients [IMAPITable](imapitable-findrow.md), eine eigenschaftseinschränkung auf die **PR_INSTANCE_KEY** -Eigenschaft der-Methode übergeben.</span><span class="sxs-lookup"><span data-stu-id="aa994-124">To implement this behavior, clients call [IMAPITable::FindRow](imapitable-findrow.md), passing a property restriction on the **PR_INSTANCE_KEY** property to the method.</span></span> <span data-ttu-id="aa994-125">Von adressbuchanbietern implementierte sind erforderlich, um diese Einschränkung zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="aa994-125">Address book providers are required to support this restriction.</span></span> 
  
<span data-ttu-id="aa994-126">Ein weiteres Feature von Listenfeldern verwendet für die Anzeige der Tabelle ist die Möglichkeit zum Positionieren des Cursors basierend auf einem Satz von Anfangszeichen.</span><span class="sxs-lookup"><span data-stu-id="aa994-126">Another feature of list boxes used for table viewing is the ability to position the cursor based on a set of prefix characters.</span></span> <span data-ttu-id="aa994-127">Wie der Benutzer Präfixzeichen eingeben startet, verschiebt der Client den Cursor auf das erste Element, das mit diesen Zeichen beginnt.</span><span class="sxs-lookup"><span data-stu-id="aa994-127">As the user starts typing prefix characters, the client moves the cursor to the first item that begins with these characters.</span></span> <span data-ttu-id="aa994-128">Clients implementieren dieses Feature mit einer Content Einschränkung basierend auf der **PR_DISPLAY_NAME** -Eigenschaft und die FL_PREFIX fuzzy-Ebene.</span><span class="sxs-lookup"><span data-stu-id="aa994-128">Clients implement this feature with a content restriction based on the **PR_DISPLAY_NAME** property and the FL_PREFIX fuzzy level.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="aa994-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa994-129">See also</span></span>



[<span data-ttu-id="aa994-130">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="aa994-130">MAPI Tables</span></span>](mapi-tables.md)

