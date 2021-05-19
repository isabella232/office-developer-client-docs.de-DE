---
title: Codieren einer Nachricht mit TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6b86d9a9-6876-4885-ae1e-8571b25b85cc
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: cdaa03cfbc0bbd0fcf6a320ecf8fae9f372d5781
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336701"
---
# <a name="encoding-a-message-with-tnef"></a><span data-ttu-id="6abb9-103">Codieren einer Nachricht mit TNEF</span><span class="sxs-lookup"><span data-stu-id="6abb9-103">Encoding a message with TNEF</span></span>

<span data-ttu-id="6abb9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6abb9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6abb9-105">Wenn eine Nachricht übermittelt wird, kann der Transportanbieter eine Datei erstellen, die während der Übertragung verwendet wird, um die Nachricht zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="6abb9-105">When a message is submitted, the transport provider can create a file that is used to contain the message during transmission.</span></span> <span data-ttu-id="6abb9-106">Als Nächstes wird eine [IStream-Schnittstelle](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) um die Datei gepackt.</span><span class="sxs-lookup"><span data-stu-id="6abb9-106">Next, an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface is wrapped around the file.</span></span> <span data-ttu-id="6abb9-107">Der Transportanbieter verwendet dann [ITnef-Methoden,](itnefiunknown.md) um die Nachrichteneigenschaften in einem markierten Format in den Datenstrom zu schreiben, mit dem die Eigenschaften von den empfangenden Transportanbietern problemlos decodiert werden können.</span><span class="sxs-lookup"><span data-stu-id="6abb9-107">The transport provider then uses [ITnef](itnefiunknown.md) methods to write the message properties to the stream in a tagged format that enables the properties to be easily decoded by the receiving transport providers.</span></span> 
  
<span data-ttu-id="6abb9-108">**So stellen Sie eine gesamte Nachricht in einer einzelnen Datei dar**</span><span class="sxs-lookup"><span data-stu-id="6abb9-108">**To represent an entire message in a single file**</span></span>
  
1. <span data-ttu-id="6abb9-109">Rufen Sie ein TNEF-Objekt ab, indem Sie ein [IStream-Objekt](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) und eine Nachricht an die [OpenTnefStreamEx-Funktion](opentnefstreamex.md) übergeben.</span><span class="sxs-lookup"><span data-stu-id="6abb9-109">Obtain a TNEF object by passing an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object and a message into the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
2. <span data-ttu-id="6abb9-110">Rufen Sie eine Liste aller definierten Eigenschaften für die Nachricht ab, indem Sie die [IMAPIProp::GetPropList-Methode](imapiprop-getproplist.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6abb9-110">Get a list of all defined properties for the message by calling the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> 
    
3. <span data-ttu-id="6abb9-111">Verwenden [Sie IMAPIProp-Methoden,](imapipropiunknown.md) um alle vom Messagingsystem unterstützten Eigenschaften auszuschließen.</span><span class="sxs-lookup"><span data-stu-id="6abb9-111">Use [IMAPIProp](imapipropiunknown.md) methods to exclude all properties supported by the messaging system.</span></span> <span data-ttu-id="6abb9-112">Schreiben Sie diese Eigenschaften zu einem geeigneten Zeitpunkt in das Messagingsystem im vom Messagingsystem benötigten Format.</span><span class="sxs-lookup"><span data-stu-id="6abb9-112">At an appropriate time, write those properties to the messaging system in the format required by the messaging system.</span></span> 
    
4. <span data-ttu-id="6abb9-113">Rufen [Sie ITnef::AddProps auf,](itnef-addprops.md) um die verbleibenden Eigenschaften einschließlich aller Anlagen zu codieren.</span><span class="sxs-lookup"><span data-stu-id="6abb9-113">Call [ITnef::AddProps](itnef-addprops.md) to encode the remaining properties, including all attachments.</span></span> 
    
5. <span data-ttu-id="6abb9-114">Rufen Sie die [ITnef::Finish-Methode](itnef-finish.md) auf, um die Nachricht in den TNEF-Stream zu codieren, nachdem alle angeforderten Eigenschaften hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="6abb9-114">Call the [ITnef::Finish](itnef-finish.md) method to encode the message into the TNEF stream after all the requested properties are added.</span></span> 
    
6. <span data-ttu-id="6abb9-115">Rufen Sie [die ITnef::OpenTaggedBody-Methode](itnef-opentaggedbody.md) auf, um den markierten Nachrichtentext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6abb9-115">Call the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method to obtain the tagged message text.</span></span> <span data-ttu-id="6abb9-116">Dieser markierte Text wird mithilfe von Methoden von der OLE IStream-Schnittstelle in das [Messagingsystem geschrieben.](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6abb9-116">This tagged text is written out to the messaging system using methods from the OLE [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface.</span></span> 
    
7. <span data-ttu-id="6abb9-117">Rufen Sie [die IUnknown::Release-Methode auf,](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) um das **ITnef-Objekt frei** zu geben.</span><span class="sxs-lookup"><span data-stu-id="6abb9-117">Call the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) method to release the **ITnef** object.</span></span> 
    
<span data-ttu-id="6abb9-118">**So verarbeiten Sie eine eingehende TNEF-Nachricht**</span><span class="sxs-lookup"><span data-stu-id="6abb9-118">**To process an inbound TNEF message**</span></span>
  
1. <span data-ttu-id="6abb9-119">Get a MAPI message object from the MAPI spooler and write message header properties into the new MAPI message.</span><span class="sxs-lookup"><span data-stu-id="6abb9-119">Get a MAPI message object from the MAPI spooler and write message header properties into the new MAPI message.</span></span>
    
2. <span data-ttu-id="6abb9-120">Erstellen und initialisieren Sie ein [IStream-Objekt,](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) um die TNEF-Daten aus der eingehenden Nachricht zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="6abb9-120">Create and initialize an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object to contain the TNEF data from the inbound message.</span></span> 
    
3. <span data-ttu-id="6abb9-121">Übergeben Sie die MAPI-Nachricht und das [IStream-Objekt](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) an die [OpenTnefStreamEx-Funktion.](opentnefstreamex.md)</span><span class="sxs-lookup"><span data-stu-id="6abb9-121">Pass the MAPI message and the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object to the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
4. <span data-ttu-id="6abb9-122">Decodieren Sie die Informationen in den TNEF-Daten, indem Sie die [ITnef::ExtractProps-Methode](itnef-extractprops.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6abb9-122">Decode the information in the TNEF data by calling the [ITnef::ExtractProps](itnef-extractprops.md) method.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="6abb9-123">Alle von **ExtractProps** decodierten Eigenschaften überschreiben Eigenschaften, die aus dem Umschlag der eingehenden Nachricht decodiert sind.</span><span class="sxs-lookup"><span data-stu-id="6abb9-123">Anything decoded by **ExtractProps** will overwrite properties decoded from the incoming message's envelope.</span></span> <span data-ttu-id="6abb9-124">Das heißt, extrahierte TNEF-Eigenschaften überschreiben die vorhandenen Eigenschaften in einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="6abb9-124">That is, extracted TNEF properties will overwrite the existing properties in a message.</span></span> 
  
5. <span data-ttu-id="6abb9-125">Verarbeiten Sie den markierten Nachrichtentext, indem [Sie ITnef::OpenTaggedBody](itnef-opentaggedbody.md) aufrufen und den Text analysieren, um Anlagenpositionen wiederhergestellt zu werden.</span><span class="sxs-lookup"><span data-stu-id="6abb9-125">Process the tagged message text by calling [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) and parse the text to recover attachment positions.</span></span> 
    
6. <span data-ttu-id="6abb9-126">Speichern Sie die Nachricht, indem Sie [IMAPIProp::SaveChanges aufrufen.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="6abb9-126">Save the message by calling [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span>
    
7. <span data-ttu-id="6abb9-127">Geben Sie das TNEF-Objekt frei, indem Sie die [IUnknown::Release-Methode](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6abb9-127">Release the TNEF object by calling the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) method.</span></span> 
    

