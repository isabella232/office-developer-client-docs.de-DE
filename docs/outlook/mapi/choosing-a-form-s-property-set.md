---
title: Auswählen eines Formulars Eigenschaftensatz
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5680fed2-b2e7-4c4b-9ba8-2c497b9c433c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0ff8d9f1ae25c55d66847b8c0e5e66c406dfdfba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586151"
---
# <a name="choosing-a-forms-property-set"></a><span data-ttu-id="f4005-103">Auswählen eines Formulars Eigenschaftensatz</span><span class="sxs-lookup"><span data-stu-id="f4005-103">Choosing a form's property set</span></span>

<span data-ttu-id="f4005-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4005-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4005-105">Wenn Sie Ihr Formular Server implementieren, müssen Sie eine Eigenschaft für jede Informationseinheit befinden, die die Nachrichtenklasse muss.</span><span class="sxs-lookup"><span data-stu-id="f4005-105">When you implement your form server, you need to have a property for each piece of information that your message class needs.</span></span> <span data-ttu-id="f4005-106">Diese Eigenschaften vordefinierten MAPI-Eigenschaften werden können, oder sie können benutzerdefinierte Eigenschaften, mit denen Sie definiert werden.</span><span class="sxs-lookup"><span data-stu-id="f4005-106">These properties can be predefined MAPI properties, or they can be custom properties that you define.</span></span> <span data-ttu-id="f4005-107">Weitere Informationen über das Arbeiten mit Eigenschaften finden Sie unter [Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f4005-107">For more information about working with properties, see [MAPI Property Overview](mapi-property-overview.md).</span></span>
  
<span data-ttu-id="f4005-108">Die Formular-Konfigurationsdatei enthält eine Liste der Eigenschaften, die für Clientanwendungen mit Ihrem Formular Server verfügbar macht, aber dies ist nicht erforderlich, die gesamte Liste der Eigenschaften, die von Ihrem Formular Server verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f4005-108">Your form configuration file will contain a list of properties that your form server exposes for client applications to use, but this does not have to be the entire list of properties used by your form server.</span></span> <span data-ttu-id="f4005-109">In der Regel verwenden-Clientanwendungen verfügbar gemachte Eigenschaften, damit Benutzer Nachrichten in einem Ordner sortieren oder ihre Schnittstellen in irgendeiner Weise anpassen.</span><span class="sxs-lookup"><span data-stu-id="f4005-109">Client applications typically use the exposed properties to enable users to sort messages in a folder or customize their interfaces in some way.</span></span>
  
<span data-ttu-id="f4005-110">MAPI verfügt über eine Reihe von vordefinierten Eigenschaften, die für die meisten Applikationen ausreichend.</span><span class="sxs-lookup"><span data-stu-id="f4005-110">MAPI has a large set of predefined properties that suffice for most applications.</span></span> <span data-ttu-id="f4005-111">Es werden jedoch Zeiten, wenn eine benutzerdefinierte Nachrichtenklasse eine Eigenschaft benötigt, die MAPI nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="f4005-111">However, there will be times when a custom message class needs a property that MAPI does not define.</span></span> <span data-ttu-id="f4005-112">Benutzerdefinierte Eigenschaften können Sie um die MAPI-vordefinierte Gruppe von Eigenschaften für spezielle Informationen zu erweitern, die der Formular Server unterstützen muss.</span><span class="sxs-lookup"><span data-stu-id="f4005-112">You can use custom properties to extend the MAPI predefined set of properties for whatever special information your form server needs to support.</span></span>
  
<span data-ttu-id="f4005-113">Sie können einen der folgenden Methoden zum Definieren von benutzerdefinierter Eigenschaften verwenden:</span><span class="sxs-lookup"><span data-stu-id="f4005-113">You can use either of the following ways to define custom properties:</span></span>
  
- <span data-ttu-id="f4005-114">Wählen Sie einen Namen für die Eigenschaft, und Verwenden der [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) -Methode, um eine Eigenschaftentag zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f4005-114">Choose a name for the property and use the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method to obtain a property tag for it.</span></span> <span data-ttu-id="f4005-115">Die [IMAPIProp](imapipropiunknown.md) -Schnittstelle, über die Sie diese Methode aufrufen, stammen aus der [IMessage](imessageimapiprop.md) Zeiger, der mit dem Formular Server übergeben wird, wenn die Nachricht erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f4005-115">The [IMAPIProp](imapipropiunknown.md) interface through which you call this method comes from the [IMessage](imessageimapiprop.md) pointer that is passed to the form server when the message is created.</span></span> <span data-ttu-id="f4005-116">Beachten Sie, dass der Name der Eigenschaft eine Zeichenfolge mit Breitzeichen sein muss.</span><span class="sxs-lookup"><span data-stu-id="f4005-116">Note that the property name must be a wide-character string.</span></span> 
    
- <span data-ttu-id="f4005-117">Definieren einer benutzerdefinierten Eigenschaftentag selbst.</span><span class="sxs-lookup"><span data-stu-id="f4005-117">Define a custom property tag yourself.</span></span> <span data-ttu-id="f4005-118">Eigenschaftentags-benutzerdefinierte muss im Bereich 0x6800 bis 0x7BFF.</span><span class="sxs-lookup"><span data-stu-id="f4005-118">Custom property tags must be in the range 0x6800 through 0x7BFF.</span></span> <span data-ttu-id="f4005-119">Eigenschaften in diesem Bereich sind Nachrichtenklasse spezifische.</span><span class="sxs-lookup"><span data-stu-id="f4005-119">Properties in this range are message-class specific.</span></span>
    
<span data-ttu-id="f4005-120">Weitere Informationen zum Definieren von benutzerdefinierter Eigenschaften finden Sie unter [Definieren eines neuen MAPI-Eigenschaften](defining-new-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="f4005-120">For more information about defining custom properties, see [Defining New MAPI Properties](defining-new-mapi-properties.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="f4005-121">Formular Server, auf denen einen Nachrichtentext häufig verwenden Sie die Eigenschaft **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) speichern.</span><span class="sxs-lookup"><span data-stu-id="f4005-121">Form servers that have a message text often use the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property to store it.</span></span> <span data-ttu-id="f4005-122">Wenn Ihr Formular Server **PR_RTF_COMPRESSED**verwendet, sollten sie außerdem sicherstellen, dass die **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))-Eigenschaft eine nur-Text-Version von den Nachrichtentext enthält für den Fall, dass die resultierende Nachricht von einem Client gelesen wird, der Rich-Text nicht unterstützt Nachrichtentext-Format (RTF).</span><span class="sxs-lookup"><span data-stu-id="f4005-122">If your form server uses **PR_RTF_COMPRESSED**, it should also ensure that the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property contains a text-only version of the message text, in case the resulting message is read by a client that does not support Rich Text Format (RTF) message text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f4005-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4005-123">See also</span></span>

- [<span data-ttu-id="f4005-124">Entwickeln von MAPI-Formularservern</span><span class="sxs-lookup"><span data-stu-id="f4005-124">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

