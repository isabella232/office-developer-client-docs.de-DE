---
title: Auswählen eines Formulareigenschaftensatzes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5680fed2-b2e7-4c4b-9ba8-2c497b9c433c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d983b71c7c92c395740a8ae6f6d3666a8bc2c0c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407193"
---
# <a name="choosing-a-forms-property-set"></a><span data-ttu-id="a227d-103">Auswählen eines Formulareigenschaftensatzes</span><span class="sxs-lookup"><span data-stu-id="a227d-103">Choosing a form's property set</span></span>

<span data-ttu-id="a227d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a227d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a227d-105">Wenn Sie Ihren Formularserver implementieren, benötigen Sie eine Eigenschaft für jede Information, die die Nachrichtenklasse benötigt.</span><span class="sxs-lookup"><span data-stu-id="a227d-105">When you implement your form server, you need to have a property for each piece of information that your message class needs.</span></span> <span data-ttu-id="a227d-106">Diese Eigenschaften können vordefinierte MAPI-Eigenschaften oder benutzerdefinierte Eigenschaften sein, die Sie definieren.</span><span class="sxs-lookup"><span data-stu-id="a227d-106">These properties can be predefined MAPI properties, or they can be custom properties that you define.</span></span> <span data-ttu-id="a227d-107">Weitere Informationen zum Arbeiten mit Eigenschaften finden Sie unter [Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a227d-107">For more information about working with properties, see [MAPI Property Overview](mapi-property-overview.md).</span></span>
  
<span data-ttu-id="a227d-108">Die Formular Konfigurationsdatei enthält eine Liste der Eigenschaften, die der Formularserver für die Verwendung durch Clientanwendungen verfügbar macht, aber dies muss nicht die gesamte Liste von Eigenschaften sein, die von Ihrem Formularserver verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a227d-108">Your form configuration file will contain a list of properties that your form server exposes for client applications to use, but this does not have to be the entire list of properties used by your form server.</span></span> <span data-ttu-id="a227d-109">Client Anwendungen verwenden in der Regel die verfügbar gemachten Eigenschaften, um Benutzern das Sortieren von Nachrichten in einem Ordner oder das Anpassen ihrer Schnittstellen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="a227d-109">Client applications typically use the exposed properties to enable users to sort messages in a folder or customize their interfaces in some way.</span></span>
  
<span data-ttu-id="a227d-110">MAPI verfügt über eine Reihe vordefinierter Eigenschaften, die für die meisten Anwendungen ausreichen.</span><span class="sxs-lookup"><span data-stu-id="a227d-110">MAPI has a large set of predefined properties that suffice for most applications.</span></span> <span data-ttu-id="a227d-111">Es kann jedoch vorkommen, dass eine benutzerdefinierte Nachrichtenklasse eine Eigenschaft benötigt, die von MAPI nicht definiert wird.</span><span class="sxs-lookup"><span data-stu-id="a227d-111">However, there will be times when a custom message class needs a property that MAPI does not define.</span></span> <span data-ttu-id="a227d-112">Sie können benutzerdefinierte Eigenschaften verwenden, um den MAPI-vordefinierten Satz von Eigenschaften für alle speziellen Informationen zu erweitern, die der Formularserver unterstützen muss.</span><span class="sxs-lookup"><span data-stu-id="a227d-112">You can use custom properties to extend the MAPI predefined set of properties for whatever special information your form server needs to support.</span></span>
  
<span data-ttu-id="a227d-113">Sie können eine der folgenden Methoden verwenden, um benutzerdefinierte Eigenschaften zu definieren:</span><span class="sxs-lookup"><span data-stu-id="a227d-113">You can use either of the following ways to define custom properties:</span></span>
  
- <span data-ttu-id="a227d-114">Wählen Sie einen Namen für die Eigenschaft aus, und verwenden Sie die [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) -Methode, um ein Property-Tag dafür abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a227d-114">Choose a name for the property and use the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method to obtain a property tag for it.</span></span> <span data-ttu-id="a227d-115">Die [IMAPIProp](imapipropiunknown.md) -Schnittstelle, über die Sie diese Methode aufrufen, stammt aus dem [IMessage](imessageimapiprop.md) -Zeiger, der beim Erstellen der Nachricht an den Formularserver übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a227d-115">The [IMAPIProp](imapipropiunknown.md) interface through which you call this method comes from the [IMessage](imessageimapiprop.md) pointer that is passed to the form server when the message is created.</span></span> <span data-ttu-id="a227d-116">Beachten Sie, dass es sich bei dem Eigenschaftsnamen um eine Breitzeichen-Zeichenfolge handeln muss.</span><span class="sxs-lookup"><span data-stu-id="a227d-116">Note that the property name must be a wide-character string.</span></span> 
    
- <span data-ttu-id="a227d-117">Definieren Sie selbst ein benutzerdefiniertes Property-Tag.</span><span class="sxs-lookup"><span data-stu-id="a227d-117">Define a custom property tag yourself.</span></span> <span data-ttu-id="a227d-118">Benutzerdefinierte Eigenschaftstags müssen sich im Range 0x6800 bis 0x7BFF befinden.</span><span class="sxs-lookup"><span data-stu-id="a227d-118">Custom property tags must be in the range 0x6800 through 0x7BFF.</span></span> <span data-ttu-id="a227d-119">Eigenschaften in diesem Bereichen sind Nachrichtenklassen spezifisch.</span><span class="sxs-lookup"><span data-stu-id="a227d-119">Properties in this range are message-class specific.</span></span>
    
<span data-ttu-id="a227d-120">Weitere Informationen zum Definieren von benutzerdefinierten Eigenschaften finden Sie unter [Definieren neuer MAPI-Eigenschaften](defining-new-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="a227d-120">For more information about defining custom properties, see [Defining New MAPI Properties](defining-new-mapi-properties.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="a227d-121">Formularserver mit einem Nachrichtentext verwenden häufig die **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))-Eigenschaft, um Sie zu speichern.</span><span class="sxs-lookup"><span data-stu-id="a227d-121">Form servers that have a message text often use the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property to store it.</span></span> <span data-ttu-id="a227d-122">Wenn in Ihrem Formularserver **PR_RTF_COMPRESSED**verwendet wird, sollte außerdem sichergestellt werden, dass die **PR_BODY** ([pidtagbody (](pidtagbody-canonical-property.md))-Eigenschaft eine nur-Text-Version des Nachrichtentexts enthält, falls die resultierende Nachricht von einem Client gelesen wird, der Rich-Text nicht unterstützt. Format (RTF)-Nachrichtentext.</span><span class="sxs-lookup"><span data-stu-id="a227d-122">If your form server uses **PR_RTF_COMPRESSED**, it should also ensure that the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property contains a text-only version of the message text, in case the resulting message is read by a client that does not support Rich Text Format (RTF) message text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a227d-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a227d-123">See also</span></span>

- [<span data-ttu-id="a227d-124">Entwickeln von MAPI-Formular Servern</span><span class="sxs-lookup"><span data-stu-id="a227d-124">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

