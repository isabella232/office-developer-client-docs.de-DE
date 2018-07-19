---
title: Eine Nachricht mit TNEF-Codierung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6b86d9a9-6876-4885-ae1e-8571b25b85cc
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2cb5c9a971f95e309f0a91cf477eefe98fe3bd64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791646"
---
# <a name="encoding-a-message-with-tnef"></a><span data-ttu-id="50632-103">Eine Nachricht mit TNEF-Codierung</span><span class="sxs-lookup"><span data-stu-id="50632-103">Encoding a message with TNEF</span></span>

<span data-ttu-id="50632-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="50632-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="50632-105">Wenn eine Nachricht gesendet wird, kann der Adressbuchhierarchie eine Datei erstellen, die verwendet wird, um die Nachricht während der Übertragung enthalten.</span><span class="sxs-lookup"><span data-stu-id="50632-105">When a message is submitted, the transport provider can create a file that is used to contain the message during transmission.</span></span> <span data-ttu-id="50632-106">Im nächsten Schritt wird die Datei eine [IStream](http://msdn.microsoft.com/de-de/library/aa380034%28VS.85%29.aspx) -Schnittstelle umbrochen.</span><span class="sxs-lookup"><span data-stu-id="50632-106">Next, an [IStream](http://msdn.microsoft.com/de-de/library/aa380034%28VS.85%29.aspx) interface is wrapped around the file.</span></span> <span data-ttu-id="50632-107">Der Adressbuchhierarchie verwendet [ITnef](itnefiunknown.md) Methoden, um die Eigenschaften der Nachricht in das Stream-Objekt in einem markierten Format schreiben, mit dem die Eigenschaften, die von der empfangenden Transport-Anbietern auf einfache Weise decodiert werden können.</span><span class="sxs-lookup"><span data-stu-id="50632-107">The transport provider then uses [ITnef](itnefiunknown.md) methods to write the message properties to the stream in a tagged format that enables the properties to be easily decoded by the receiving transport providers.</span></span> 
  
<span data-ttu-id="50632-108">**Gesamte Nachricht in einer einzigen Datei darstellen.**</span><span class="sxs-lookup"><span data-stu-id="50632-108">**To represent an entire message in a single file**</span></span>
  
1. <span data-ttu-id="50632-109">Abrufen eines TNEF-Objekts, indem Sie ein [IStream](http://msdn.microsoft.com/de-de/library/aa380034%28VS.85%29.aspx) -Objekt und eine Nachricht an die Funktion [OpenTnefStreamEx](opentnefstreamex.md) übergeben.</span><span class="sxs-lookup"><span data-stu-id="50632-109">Obtain a TNEF object by passing an [IStream](http://msdn.microsoft.com/de-de/library/aa380034%28VS.85%29.aspx) object and a message into the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
2. <span data-ttu-id="50632-110">Erhalten Sie eine Liste aller definierten Eigenschaften für die Nachricht, durch die [IMAPIProp::GetPropList](imapiprop-getproplist.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="50632-110">Get a list of all defined properties for the message by calling the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> 
    
3. <span data-ttu-id="50632-111">Verwenden Sie [IMAPIProp](imapipropiunknown.md) Methoden, um alle Eigenschaften von messaging-System unterstützt auszuschließen.</span><span class="sxs-lookup"><span data-stu-id="50632-111">Use [IMAPIProp](imapipropiunknown.md) methods to exclude all properties supported by the messaging system.</span></span> <span data-ttu-id="50632-112">Schreiben Sie zu einem geeigneten Zeitpunkt diese Eigenschaften in der messaging-System im Format von messaging-System erforderlich.</span><span class="sxs-lookup"><span data-stu-id="50632-112">At an appropriate time, write those properties to the messaging system in the format required by the messaging system.</span></span> 
    
4. <span data-ttu-id="50632-113">Rufen Sie [ITnef::AddProps](itnef-addprops.md) , um die übrigen Eigenschaften, einschließlich aller Anlagen zu codieren.</span><span class="sxs-lookup"><span data-stu-id="50632-113">Call [ITnef::AddProps](itnef-addprops.md) to encode the remaining properties, including all attachments.</span></span> 
    
5. <span data-ttu-id="50632-114">Rufen Sie die [ITnef::Finish](itnef-finish.md) -Methode, um die Nachricht in der TNEF-Stream codieren, nachdem alle angeforderten Eigenschaften hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="50632-114">Call the [ITnef::Finish](itnef-finish.md) method to encode the message into the TNEF stream after all the requested properties are added.</span></span> 
    
6. <span data-ttu-id="50632-115">Rufen Sie die [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) -Methode, um den markierten Nachrichtentext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="50632-115">Call the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method to obtain the tagged message text.</span></span> <span data-ttu-id="50632-116">Dieser markierte Text wird an die messaging-System mit den Methoden der OLE- [IStream](http://msdn.microsoft.com/de-de/library/aa380034%28VS.85%29.aspx) -Schnittstelle geschrieben.</span><span class="sxs-lookup"><span data-stu-id="50632-116">This tagged text is written out to the messaging system using methods from the OLE [IStream](http://msdn.microsoft.com/de-de/library/aa380034%28VS.85%29.aspx) interface.</span></span> 
    
7. <span data-ttu-id="50632-117">Rufen Sie die [IUnknown](http://msdn.microsoft.com/de-de/library/ms682317%28VS.85%29.aspx) -Methode, um das Objekt **ITnef** freizugeben.</span><span class="sxs-lookup"><span data-stu-id="50632-117">Call the [IUnknown::Release](http://msdn.microsoft.com/de-de/library/ms682317%28VS.85%29.aspx) method to release the **ITnef** object.</span></span> 
    
<span data-ttu-id="50632-118">**An den Prozess eine eingehende TNEF-Nachricht**</span><span class="sxs-lookup"><span data-stu-id="50632-118">**To process an inbound TNEF message**</span></span>
  
1. <span data-ttu-id="50632-119">Entnehmen Sie ein MAPI-Message-Objekt die MAPI-Warteschlange und Schreiben Sie Nachrichtenkopf-Eigenschaften in die neue MAPI-Nachricht zu.</span><span class="sxs-lookup"><span data-stu-id="50632-119">Get a MAPI message object from the MAPI spooler and write message header properties into the new MAPI message.</span></span>
    
2. <span data-ttu-id="50632-120">Erstellen Sie und initialisieren Sie [IStream](http://msdn.microsoft.com/de-de/library/aa380034%28VS.85%29.aspx) -Objekts, um die TNEF-Daten aus der eingehenden Nachricht enthalten.</span><span class="sxs-lookup"><span data-stu-id="50632-120">Create and initialize an [IStream](http://msdn.microsoft.com/de-de/library/aa380034%28VS.85%29.aspx) object to contain the TNEF data from the inbound message.</span></span> 
    
3. <span data-ttu-id="50632-121">Übergeben Sie die MAPI-Nachricht und die [IStream](http://msdn.microsoft.com/de-de/library/aa380034%28VS.85%29.aspx) -Objekt an die [OpenTnefStreamEx](opentnefstreamex.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="50632-121">Pass the MAPI message and the [IStream](http://msdn.microsoft.com/de-de/library/aa380034%28VS.85%29.aspx) object to the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
4. <span data-ttu-id="50632-122">Decodieren Sie die Informationen in die TNEF-Daten durch Aufrufen der Methode [ITnef::ExtractProps](itnef-extractprops.md) .</span><span class="sxs-lookup"><span data-stu-id="50632-122">Decode the information in the TNEF data by calling the [ITnef::ExtractProps](itnef-extractprops.md) method.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="50632-123">Nichts **ExtractProps** decodiert werden Eigenschaften, die von der eingehenden Nachricht Umschlag decodiert überschrieben.</span><span class="sxs-lookup"><span data-stu-id="50632-123">Anything decoded by **ExtractProps** will overwrite properties decoded from the incoming message's envelope.</span></span> <span data-ttu-id="50632-124">D. h., überschreibt extrahierte TNEF-Eigenschaften die vorhandenen Eigenschaften in einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="50632-124">That is, extracted TNEF properties will overwrite the existing properties in a message.</span></span> 
  
5. <span data-ttu-id="50632-125">Den markierten Nachrichtentext durch Aufrufen von [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) verarbeiten und analysiert den Text, um die Anlage Positionen wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="50632-125">Process the tagged message text by calling [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) and parse the text to recover attachment positions.</span></span> 
    
6. <span data-ttu-id="50632-126">Speichern Sie die Nachricht durch Aufrufen von [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="50632-126">Save the message by calling [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span>
    
7. <span data-ttu-id="50632-127">Das TNEF-Objekt wird durch Aufrufen der Methode [IUnknown](http://msdn.microsoft.com/de-de/library/ms682317%28VS.85%29.aspx) frei.</span><span class="sxs-lookup"><span data-stu-id="50632-127">Release the TNEF object by calling the [IUnknown::Release](http://msdn.microsoft.com/de-de/library/ms682317%28VS.85%29.aspx) method.</span></span> 
    

